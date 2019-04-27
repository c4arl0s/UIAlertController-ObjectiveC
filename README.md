# steps to create an Alert

1.- create an instance of UIAlertController
2.- create an alert action
3.- add this action to the alert created.
4.- present the viewcontroller alert.

# UIAlertController-ObjectiveC
UIAlertController-ObjectiveC

``` objective-c
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
    UIAlertController *alert = [UIAlertController alertControllerWithTitle:@"Alert"
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


