# Steps to create an Alert

1. create an instance of UIAlertController
2. create an alert action
3. add this action to the alert created.
4. present the viewcontroller alert.

``` objective-c
//
//  AppDelegate.h
//  AlertViewControllerExample
//
//  Created by Carlos Santiago Cruz on 4/17/19.
//  Copyright © 2019 Carlos Santiago Cruz. All rights reserved.
//

#import <UIKit/UIKit.h>

@interface AppDelegate : UIResponder <UIApplicationDelegate>

@property (strong, nonatomic) UIWindow *window;


@end
```


```` objective-c
//
//  AppDelegate.m
//  AlertViewControllerExample
//
//  Created by Carlos Santiago Cruz on 4/17/19.
//  Copyright © 2019 Carlos Santiago Cruz. All rights reserved.
//

#import "AppDelegate.h"

@interface AppDelegate ()

@end

@implementation AppDelegate


- (BOOL)application:(UIApplication *)application didFinishLaunchingWithOptions:(NSDictionary *)launchOptions {
    // Override point for customization after application launch.
    return YES;
}


- (void)applicationWillResignActive:(UIApplication *)application {
    // Sent when the application is about to move from active to inactive state. This can occur for certain types of temporary interruptions (such as an incoming phone call or SMS message) or when the user quits the application and it begins the transition to the background state.
    // Use this method to pause ongoing tasks, disable timers, and invalidate graphics rendering callbacks. Games should use this method to pause the game.
}


- (void)applicationDidEnterBackground:(UIApplication *)application {
    // Use this method to release shared resources, save user data, invalidate timers, and store enough application state information to restore your application to its current state in case it is terminated later.
    // If your application supports background execution, this method is called instead of applicationWillTerminate: when the user quits.
}


- (void)applicationWillEnterForeground:(UIApplication *)application {
    // Called as part of the transition from the background to the active state; here you can undo many of the changes made on entering the background.
}


- (void)applicationDidBecomeActive:(UIApplication *)application {
    // Restart any tasks that were paused (or not yet started) while the application was inactive. If the application was previously in the background, optionally refresh the user interface.
}


- (void)applicationWillTerminate:(UIApplication *)application {
    // Called when the application is about to terminate. Save data if appropriate. See also applicationDidEnterBackground:.
}


@end
```


``` objective-c 
//
//  ViewController.h
//  AlertViewControllerExample
//
//  Created by Carlos Santiago Cruz on 4/17/19.
//  Copyright © 2019 Carlos Santiago Cruz. All rights reserved.
//

#import <UIKit/UIKit.h>

@interface ViewController : UIViewController


@end
```


```` objective-c
//
//  ViewController.m
//  AlertViewControllerExample
//
//  Created by Carlos Santiago Cruz on 4/17/19.
//  Copyright © 2019 Carlos Santiago Cruz. All rights reserved.
//

#import "ViewController.h"

@interface ViewController ()
@property (weak, nonatomic) IBOutlet UIButton *buttonAlert; 
@end

@implementation ViewController

- (void)viewDidLoad {
    [super viewDidLoad];
}
- (IBAction)buttonAlertTapped:(id)sender {
    UIAlertController *alert = [UIAlertController alertControllerWithTitle:@"This is my first alert, be nice"
                                                                   message:@"This is simple alert"
                                                            preferredStyle:UIAlertControllerStyleAlert];
    UIAlertAction *oKButton = [UIAlertAction actionWithTitle:@"OK"
                                                       style:UIAlertActionStyleDefault
                                                     handler:nil];
    [alert addAction:oKButton];
    [self presentViewController:alert animated:YES completion:nil];
}
@end
```

