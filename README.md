# Steps to create an Alert

1. create an instance of UIAlertController
2. create an alert action
3. add this action to the alert created.
4. present the viewcontroller alert.

# In AppDelegate

```objective-c
self.window = [[UIWindow alloc] initWithFrame:[UIScreen mainScreen].bounds];
viewController = [[ViewController alloc] initWithNibName:@"ViewController" bundle:nil];
self.window.rootViewController = viewController;
[self.window makeKeyAndVisible];
return YES;
```

# 1. create an instance of UIAlertController

```swift
UIAlertController *alertController = [UIAlertController alertControllerWithTitle:@"This is my first alert, be nice"
                                                                   message:@"This is a simple alert"
                                                            preferredStyle:UIAlertControllerStyleAlert];
```

# 2. create an alert action

```swift
UIAlertAction *okAlertAction = [UIAlertAction actionWithTitle:@"OK"
                                                       style:UIAlertActionStyleDefault
                                                     handler:nil];
```

# 3. add this action to the alert created.

```swift
[alertController addAction:okAlertAction];
```

# 4. present the alert controller

```swift
[self presentViewController:alertController animated:YES completion:nil];
```


# In ViewController

```objective-c
- (IBAction)buttonAlertTapped:(id)sender {
    UIAlertController *alert = [UIAlertController alertControllerWithTitle:@"This is my first alert, be nice"
                                                                   message:@"This is a simple alert"
                                                            preferredStyle:UIAlertControllerStyleAlert];
    UIAlertAction *oKButton = [UIAlertAction actionWithTitle:@"OK"
                                                       style:UIAlertActionStyleDefault
                                                     handler:nil];
    [alert addAction:oKButton];
    [self presentViewController:alert animated:YES completion:nil];
}
```


![Captura de Pantalla 2019-04-28 a la(s) 19 51 31](https://user-images.githubusercontent.com/24994818/56872466-be714680-69e6-11e9-8408-3313c7d3c4c7.png)

![Captura de Pantalla 2019-04-28 a la(s) 18 50 30](https://user-images.githubusercontent.com/24994818/56871684-5b7bb180-69de-11e9-8585-34e8909a1ec3.png)

# set a value for an image to the alert

this methods work but I dont know why

``` objective-c
- (void)buttonTapped
{
    UIAlertController *alert = [UIAlertController alertControllerWithTitle:@"This is my first alert, be nice"
                                                                   message:@"This is simple alert"
                                                            preferredStyle:UIAlertControllerStyleAlert];
    UIAlertAction *oKButton = [UIAlertAction actionWithTitle:@"OK"
                                                       style:UIAlertActionStyleDefault
                                                     handler:nil];
    [alert addAction:oKButton];
    UIAlertAction *noButton = [UIAlertAction actionWithTitle:@"NO"
                                                       style:UIAlertActionStyleDefault
                                                     handler:nil];
    [alert addAction:noButton];
    UIAlertAction *siButton = [UIAlertAction actionWithTitle:@"SI"
                                                       style:UIAlertActionStyleDefault
                                                     handler:nil];
    [alert addAction:siButton];
    [siButton setValue:[[UIImage imageNamed:@"mic.jpg"] imageWithRenderingMode:UIImageRenderingModeAlwaysTemplate] forKey:@"image"];
    [self presentViewController:alert animated:YES completion:^{
        [self->button setBackgroundColor:[UIColor redColor]];
    }];
}
```




