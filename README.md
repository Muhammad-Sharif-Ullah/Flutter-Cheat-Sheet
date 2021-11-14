# Flutter Cheat Sheet
You need to get started quickly with Flutter? Here are some cheats that will help you get started with developing your next billion dollar app!!

<!-- [![Awesome](https://cdn.rawgit.com/sindresorhus/awesome/d7305f38d29fed78fa85652e3a63e154dd8e8829/media/badge.svg)](https://github.com/sindresorhus/awesome) ![Branch master](https://img.shields.io/badge/branch-master-brightgreen.svg?style=flat-square)
 [![GitHub license](https://img.shields.io/badge/license-MIT-blue.svg)](https://raw.githubusercontent.com/temidtech/flutter-cheat-sheet/master/LICENSE) -->
 
## Table of Contents

- [Installation](#Installation)
- [Layouts](#layouts)
- [Aligning widgets evenly](#aligning-widgets-evenly)
- [Buttons](#buttons)
- [Navigation](#navigation)
- [ActionBar](#actionbar)
- [Swipeable actionbar tabs](#tabs)
- [Form validations](#form-validations)



## Installation

###  A. Windows
#### STEP 1
To get started with Flutter, your dev environment must meet the following requirements

| Operating Systems        | Windows 7 SP1 or later (64-bit)           |
| ------------- |:-------------:|
| Disk Space     | 400 MB (does not include disk space for IDE/tools) |
| Tool    | Windows PowerShell 5.0 or newer      |
| Tool | Git for Windows 2.x     |

You can choose either the first tool or second depending on how comfortable you are with either.

#### STEP 2

- Download an installation bundle [here](https://storage.googleapis.com/flutter_infra/releases/stable/windows/flutter_windows_v1.2.1-stable.zip) to get the latest stable release of the Flutter SDK
- Extract the zip file and place the contained flutter in the desired installation location for the Flutter SDK (eg. C:\src\flutter;  do not install Flutter in a directory like C:\Program Files\ that requires elevated privileges ).
- Locate the file flutter_console.bat inside the flutter directory. Start it by double-clicking.

Congratulations! You are now ready to run Flutter commands in the Flutter Console!

NOTE: Should you at anytime require an ugrade to a latest Flutter version? [Use this link](https://flutter.dev/docs/development/tools/sdk/upgrading)


#### STEP 3 (Optional)

If you wish to run Flutter commands in the regular Windows console, take these steps to add Flutter to the PATH environment variable:
- From the Start search bar, type ‘env’ and select Edit environment variables for your account
- Under User variables check if there is an entry called Path(If it exist append the full path to flutter\bin using ; as a separator from existing values else create a new user variable named Path with the full path to flutter\bin as its value)


#### STEP 4
If at any point you need to check your environment and see a report of the status of your Flutter installation, all you need is the command below. 
```windows
 flutter doctor
 ```
 Here is a sample output:
 ```windows
[-] Android toolchain - develop for Android devices
    • Android SDK at D:\Android\sdk
    ✗ Android SDK is missing command line tools; download from https://goo.gl/XxQghQ
    • Try re-installing or updating your Android SDK,
      visit https://flutter.dev/setup/#android-setup for detailed instructions.
 ```
Ensure you check the output carefully for other software you may need to install or further tasks to perform (shown in bold text).

### Android setup

Wondering why we need android studio setup?Here is why:
Flutter relies on a full installation of Android Studio to supply its Android platform dependencies.You can however write flutter apps on other IDEs such as Visual studio code.

##### Install Android Studio
- Download and install Android Studio from [here](https://developer.android.com/studio/?gclid=Cj0KCQjwsZ3kBRCnARIsAIuAV_RMbMDTLk-O1LOvm7MXD_o2diOYLqz4KPIBrpfUnw_2fAuE44y5K5waAt5EEALw_wcB).

  ![alt text](https://developer.android.com/studio/images/studio-homepage-hero.jpg)
  
- Launch Android Studio, and go through the ‘Android Studio Setup Wizard’. This installs the latest Android SDK, Android SDK Platform-Tools, and Android SDK Build-Tools, which are required by Flutter when developing for Android.


##### Set up your Android device
One of the coolest thing about Flutter is that you can run your Flutter app on android device without writing complex commands. Here is how I did it.

First thing first, to prepare to run and test your Flutter app on an Android device, you’ll need an Android device running **Android 4.1 (API level 16) or higher**.

**Other necessary steps to follow:**

- Enable Developer options and USB debugging on your device. **Go to Settings > Developer options >USB debugging**.
- Windows-only: Install the Google USB Driver
- Using a USB cable, plug your phone into your computer. If prompted on your device, authorize your computer to access your device.
- In your android studio terminal or command prompt, run the ``` flutter devices``` command to verify that Flutter recognizes your connected Android device.

#### Set up the Android emulator
To prepare to run and test your Flutter app on the Android emulator for some reasons :), follow these steps:

- Enable VM acceleration on your machine.
- Launch **Android Studio > Tools > Android > AVD Manager** and select Create Virtual Device. (The Android submenu is only present when inside an Android project.)
- Choose a device definition and select **Next**.
- Select one or more system images for the Android versions you want to emulate, and select **Next**. An x86 or x86_64 image is recommended.
- Under Emulated Performance, select **Hardware - GLES 2.0** to enable hardware acceleration.
- Verify the AVD configuration is correct, and select Finish.


In Android Virtual Device Manager, click **Run** in the toolbar. The emulator starts up and displays the default canvas for your selected OS version and device.

###  B. Mac
#### STEP 1
To get started with Flutter, your dev environment must meet the following requirements

| Operating Systems        | macOS (64-bit)           |
| ------------- |:-------------:|
| Disk Space     | 700 MB (does not include disk space for IDE/tools) |
| Tool    | bash, curl, git 2.x, mkdir, rm, unzip, which|

NOTE: You can pick any tool you are comfortable with.

#### STEP 2

- Download an installation bundle [here](https://storage.googleapis.com/flutter_infra/releases/stable/macos/flutter_macos_v1.2.1-stable.zip) to get the latest stable release of the Flutter SDK
- Extract the file in the desired location.
```windows
 cd ~/development
 unzip ~/Downloads/flutter_macos_v1.2.1-stable.zip
 ```
- Add the flutter tool to your path.
```windows
 export PATH="$PATH:`pwd`/flutter/bin"
 ```
This command sets your PATH variable for the current terminal window only. 

To permanently add Flutter to your path, follow the steps below:

- Determine the directory where you placed the Flutter SDK.
- Open (or create) $HOME/.bash_profile. The file path and filename might be different on your machine.
- Add the following line and change [PATH_TO_FLUTTER_GIT_DIRECTORY] to be the path where you cloned Flutter’s git repo:
```windows
 export PATH="$PATH:[PATH_TO_FLUTTER_GIT_DIRECTORY]/flutter/bin"
 ```
- Run source $HOME/.bash_profile to refresh the current window.
- Verify that the flutter/bin directory is now in your PATH by running:
```windows
 echo $PATH
 ```
Congratulations! You are now ready to run Flutter commands in the Flutter Console!

NOTE: Should you at anytime require an ugrade to a latest Flutter version? [Use this link](https://flutter.dev/docs/development/tools/sdk/upgrading)


#### STEP 3 (Optional)
If at any point you need to check your environment and see a report of the status of your Flutter installation, all you need is the command below. 
```windows
 flutter doctor
 ```
 Here is a sample output:
 ```windows
[-] Android toolchain - develop for Android devices
    • Android SDK at D:\Android\sdk
    ✗ Android SDK is missing command line tools; download from https://goo.gl/XxQghQ
    • Try re-installing or updating your Android SDK,
      visit https://flutter.dev/setup/#android-setup for detailed instructions.
 ```
Ensure you check the output carefully for other software you may need to install or further tasks to perform (shown in bold text).




## Layouts

###   Card Layout

```dart
@override
Widget build(BuildContext context) {
  return Card(
    // Set elevation value here
    elevation: 4.0,
    child: Container(
      color: Palette.White, // set card's color
      padding: EdgeInsets.symmetric(vertical: 8.0), // Set layout padding
      child: Row(
        children: <Widget>[
      Expanded(
      child: Column(
        crossAxisAlignment: CrossAxisAlignment.center,
        children: [
          Text(
            title, // Set the text value
            style: TextStyles.caption, //Set your custom style here
          ),
          Text(
            body, // Set the text value
            style: TextStyle(
              fontSize: 20.0,
              fontWeight: FontWeight.w500, // Set font weight
              color: Colors.black87, // Set text color
            ),
          ),
        ],
      ),
    ),
  ),
 ],
),
),
);
}
  ```
  
## Aligning widgets evenly
  ###   Horizontal MainAxisAlignment
    Setting the main axis alignment to spaceEvenly divides the free horizontal space 
    evenly between, before, and after each image
  ![alt text](https://github.com/Temidtech/Flutter-Cheat-Sheet/blob/master/screenshots/img1.PNG)
   ```dart
   Row(
  mainAxisAlignment: MainAxisAlignment.spaceEvenly,
  children: [
    Image.asset('img/1.jpg'),
    Image.asset('img/2.jpg'),
    Image.asset('img/3.jpg'),
  ],
);
   ```
 ###   Vertical MainAxisAlignment
    Setting the main axis alignment to spaceEvenly divides the free vertical space 
    evenly between, before, and after each image
  ![alt text](https://github.com/Temidtech/Flutter-Cheat-Sheet/blob/master/screenshots/img2.PNG)
   ```dart
   Column(
  mainAxisAlignment: MainAxisAlignment.spaceEvenly,
  children: [
    Image.asset('img/1.jpg'),
    Image.asset('img/2.jpg'),
    Image.asset('img/3.jpg'),
  ],
);
 ```
 ###   Packing Widgets
    By default, a row or column occupies as much space along its main axis as possible,
    but if you want to pack the children closely together, set its mainAxisSize to MainAxisSize.min. 
    The following example uses this property to pack 3 buttons together.
    
 <img src="https://github.com/Temidtech/Flutter-Cheat-Sheet/blob/master/screenshots/Packing-widget.png" width="280"/> 
   
   ```dart
        new Row(
               mainAxisSize: MainAxisSize.min, // This is the magic. :)
                children: <Widget>[
                  new RaisedButton(
                    padding: const EdgeInsets.all(8.0),
                    textColor: Colors.white,
                    color: Colors.blue,
                    onPressed: onClick, // Button onClick function
                    child: new Text("Button 1"),
                  ),
                  new RaisedButton(
                    onPressed: subtractNumbers,
                    textColor: Colors.white,
                    color: Colors.red,
                    padding: const EdgeInsets.all(8.0),
                    child: new Text(
                      "Button 2",
                    ),
                  ),
                  new RaisedButton(
                    onPressed: subtractNumbers,
                    textColor: Colors.white,
                    color: Colors.red,
                    padding: const EdgeInsets.all(8.0),
                    child: new Text(
                      "Button 3",
                    ),
                  ),
                ],
              )
 ```
 
 ## Buttons
 ###  Raised Button Effect
    A Raised button is based on a Material widget whose Material.elevation increases when the button is pressed.
    Do you want to add an elevation effect to your button? Use the snippet below
    Please avoid using elevated buttons on already-elevated content such as dialogs or cards.
    
 <img src="https://github.com/Temidtech/Flutter-Cheat-Sheet/blob/master/screenshots/Raised-button.png" width="280"/> 
   
   ```dart
         new Row(
                mainAxisAlignment: MainAxisAlignment.spaceEvenly,
                children: <Widget>[
                  new RaisedButton(
                    padding: const EdgeInsets.all(8.0),
                    textColor: Colors.white,
                    color: Colors.blue,
                    onPressed: onClick, // Button onClick function
                    child: new Text("Plus"),
                  ),
                  new RaisedButton(
                    onPressed: subtractNumbers,
                    textColor: Colors.white,
                    color: Colors.red,
                    padding: const EdgeInsets.all(8.0),
                    child: new Text(
                      "Minus",
                    ),
                  ),
                ],
              )
 ```
  ###  Toggle Effect
    You can toggle the color of a raised button with few lines. The snippet below shows how you can achieve this.
    
 <img src="https://github.com/Temidtech/Flutter-Cheat-Sheet/blob/master/screenshots/toggle-button.png" width="280"/> 
   
   ```dart
   1. This button will need to be created in the build of a State of a StatefulWidget
   2. The State must have a member variable bool isPressed = false;;
         new Row(
                mainAxisAlignment: MainAxisAlignment.spaceEvenly,
                children: <Widget>[
                  
                  new RaisedButton(
                    child: new Text('Toggle me!'),
                    textColor: Colors.white,
                    shape: new RoundedRectangleBorder(
                      borderRadius: new BorderRadius.circular(30.0),
                    ),
                    color: isPressed ? Colors.grey : Colors.blue,
                    onPressed: () => setState(() => isPressed = !isPressed), // make state changes in a setState
                  )
                ],
              )
 ```
 
  ###  Floating Action Button
    Creating a simple FAB using the code snippet below
    
 <img src="https://github.com/Temidtech/Flutter-Cheat-Sheet/blob/master/screenshots/fab-button.png" width="280"/> 
   
   ```dart
    return new Scaffold(
        appBar: new AppBar(
          title: new Text("FAB Example"),
        ),
        floatingActionButton: FloatingActionButton(
          onPressed: () => {},
          tooltip: 'Add me!',
          child: Icon(Icons.add),
        ),
        body:...
     );
 ```
 ## ActionBar
 You can use flutter's AppBar just with one line of code.
 
  ```dart
    return new Scaffold(
        appBar: new AppBar(
          title: new Text("AppBar Demo"),
        ),);
        
   ```    
 
 ## Navigation
 

### Bottom Navigation Bar
Creating bottom navigation in flutter is fatanstic, truth be told! I thought I'd write some complex code to make this happen. But see how I achieved it!

#### Create a Bottom Navigation Bar without style
<img src="https://github.com/Temidtech/Flutter-Cheat-Sheet/blob/master/screenshots/bottom-bar-1.png" width="280"/> 
   
   ```dart
    return new Scaffold(
        appBar: new AppBar(
          title: new Text("FAB Example"),
        ),
        bottomNavigationBar:BottomNavigationBar(
          currentIndex: 0,   // Set initial state of BottomNavigationBar
          items: [           // Create your BottomNavigationBar items
            BottomNavigationBarItem(
              icon: new Icon(Icons.playlist_add),
              title: new Text("Playlist"),
            ),
            BottomNavigationBarItem(
              icon: new Icon(Icons.person),
              title: new Text("My Profile")
            ),
            BottomNavigationBarItem(
              icon: new Icon(Icons.mail),
              title: new Text("Inbox")
            )
          ],
        ),
        body:...
     );
 ```
 #### Create a Bottom Navigation Bar with custom style
<img src="https://github.com/Temidtech/Flutter-Cheat-Sheet/blob/master/screenshots/bottom-bar-2.png" width="280"/> 
   
   ```dart
    return new Scaffold(
        appBar: new AppBar(
          title: new Text("FAB Example"),
        ),
            bottomNavigationBar: Theme(  // Create your custom style with Flutter Theme
          data: Theme.of(context).copyWith(
              canvasColor: Colors.blueAccent, // Choose your preferred color as the BottomNavigationBar background
              primaryColor: Colors.white30, // Choose your preferred color as the primary color
              textTheme: Theme.of(context) // The text theme goes here
                  .textTheme
                  .copyWith(caption: new TextStyle(color: Colors.white))),
          child: BottomNavigationBar(
            currentIndex: 0, // Set initial state of BottomNavigationBar
            items: [          // Create your BottomNavigationBar items
              BottomNavigationBarItem(
                icon: new Icon(Icons.playlist_add),
                title: new Text("Playlist"),
              ),
              BottomNavigationBarItem(
                  icon: new Icon(Icons.person), title: new Text("My Profile")),
              BottomNavigationBarItem(
                  icon: new Icon(Icons.mail), title: new Text("Inbox"))
            ],
          ),
        ),
        body:...
     );
 ```
 
 ### Prepare for Navigation
 
 You'd definetly want to navigate between multiple pages using bottom navigation bar. Here is how you can do that seamlessly!
 
 ##### Step 1:
      Add two new instance properties to your State class. Something like this:
 ```dart
       class _FreeDemoState extends State<FreeDemo> {
              int _currentIndex = 0;
              final List<Widget> _children = [];
             ...
 ```
 
  ##### Step 2:
      Add children to a list in your State class. Something like this:
 ```dart
    // Declare all the widgets you want to navigate on bottom bar item click
    final List<Widget> _children = [
    PlaceholderWidget(Colors.white), 
    PlaceholderWidget(Colors.green),
    PlaceholderWidget(Colors.blue)
  ];
 ```
  ##### Step 3:
      Create a function that will update the value of _currentIndex in your State class.
      It'd be called when user taps on a bottombar item. Something like this:
 ```dart
    void onTabTapped(int index) {
   setState(() {
     _currentIndex = index;
   });
 }
 ```
 
 ##### Step 4:
     Create a class called PlaceholderWidget.This widget will be displayed when Bottom bar is tapped.
 ```dart
import 'package:flutter/material.dart';

class PlaceholderWidget extends StatelessWidget {
  final Color color;

  PlaceholderWidget(this.color);

  @override
  Widget build(BuildContext context) {
    return Container(
      color: color,
      child: new Center(
        child: new Column(
          mainAxisAlignment: MainAxisAlignment.center,
          children: <Widget>[
            new Text(
              'Try me!',
              style: new TextStyle(
                fontWeight: FontWeight.bold,
                fontSize: 100.0,
                fontFamily: 'Roboto',
              ),
            ),
           ...
          ],
        ),
      ),
    );
  }
}
 ```
  ##### Step 5:
     Create a class called PlaceholderWidget.This widget will be displayed when Bottom bar is tapped.
 ```dart
@override
 Widget build(BuildContext context) {
   return Scaffold(
     appBar: AppBar(
       title: Text('My Flutter App'),
     ),
     bottomNavigationBar: Theme(
          data: Theme.of(context).copyWith(
              canvasColor: Colors.blueAccent,
              primaryColor: Colors.white30,
              textTheme: Theme.of(context)
                  .textTheme
                  .copyWith(caption: new TextStyle(color: Colors.white))),
          child: BottomNavigationBar(
            currentIndex: _currentIndex, // Set the value of _currentIndex to currentIndex
            onTap: onTabTapped,       // Set the onTabTapped function we creatd earlier
            items: [
              BottomNavigationBarItem(
                icon: new Icon(Icons.playlist_add),
                title: new Text("Playlist"),
              ),
              BottomNavigationBarItem(
                  icon: new Icon(Icons.person), title: new Text("My Profile")),
              BottomNavigationBarItem(
                  icon: new Icon(Icons.mail), title: new Text("Inbox"))
            ],
          ),
        ),
        body:_children[_currentIndex] // Change Widget based on item selected
   );
 }
 ```
##### Yaaaaaaaassssss!!!! We just did it! Take a look at the result
<img src="https://github.com/Temidtech/Flutter-Cheat-Sheet/blob/master/screenshots/bottom-tap-1.png" width="280"/> <img src="https://github.com/Temidtech/Flutter-Cheat-Sheet/blob/master/screenshots/bottom-tap-2.png" width="280"/> 
 
 
## Tabs

Working with tabs is a common pattern in apps following the Material Design guidelines. 
Flutter includes a convenient way to create tab layouts as part of the material library.
To quickly implement tabs in your next project, follow these 3 steps:


 ### Step 1
    Create a TabController widget, which allows you to keep a selected tab and content sections in sync.
    
   
   ```dart
 return MaterialApp(
      home: DefaultTabController(
        length: 3, // The number of tabs / content sections we need to display
        child:.. // See next step!
      ),
    );
 ```
  ### Step 2
    Now we can create 3 tabs for the TabController we initialized earlier using TabBar!
    
 <img src="https://github.com/Temidtech/Flutter-Cheat-Sheet/blob/master/screenshots/tabs.gif" width="280"/> 
   
   ```dart
       return MaterialApp(
      home: DefaultTabController(
        length: 3,
        child: Scaffold(
          appBar: AppBar(
            bottom: TabBar(
              tabs: [
                Tab(icon: Icon(Icons.home)),
                Tab(icon: Icon(Icons.people)),
                Tab(icon: Icon(Icons.mail)),
              ],
            ),
            title: Text('Flutter Tabs Example'), // You can declare a title for your tab
          ),
          body: ... // See next step for this!
        ),
      ),
    );
 ```
  ### Step 3
    Now that we have tabs, we’ll want to display content when a tab is selected. 
    For this demo, we’ll employ the TabBarView Widget.
    
 <img src="https://github.com/Temidtech/Flutter-Cheat-Sheet/blob/master/screenshots/tabs.gif" width="280"/> 
   
   ```dart
            return MaterialApp(
      home: DefaultTabController(
        length: 3,
        child: Scaffold(
          appBar: AppBar(
            bottom: TabBar(
              tabs: [
                Tab(icon: Icon(Icons.home)),
                Tab(icon: Icon(Icons.people)),
                Tab(icon: Icon(Icons.mail)),
              ],
            ),
            title: Text('Flutter Tabs Example'),
          ),
          body: TabBarView(
            children: [
              FirstPlaceHolder(), // Create a widget class called FirstPlaceHolder
              SecondPlaceHolder(), // Create a widget class called SecondPlaceHolder
              ThirdPlaceHolder() //// Create a widget class called ThirdPlaceHolder
            ],
          ),
        ),
      ),
    );
 ```
 
 ## Navigation Drawer

There are situations whereby there won't be insufficient space to support tabs. Drawers provide a handy alternative at this point.
In Flutter, we can use the Drawer Widget in combination with a Scaffold to create a layout with a Material Design Drawer.

 <img src="https://github.com/Temidtech/Flutter-Cheat-Sheet/blob/master/screenshots/navigation-drawer.gif" width="280"/> 
 
 The code snippet below shows you how to get this done quickly.
   
 ```dart
import 'package:flutter/material.dart';
import 'package:oamp/app/screens/form_validation.dart';
import 'package:oamp/app/screens/place_holder.dart';

class FreeDemo extends StatefulWidget {
  @override
  State<StatefulWidget> createState() {
    return new FreeDemoState();
  }
}

class FreeDemoState extends State<FreeDemo>
    with SingleTickerProviderStateMixin {
  int _selectedIndex = 0;

  final drawerItems = [
    new DrawerItem("Home", Icons.home),
    new DrawerItem("Menu", Icons.fastfood),
    new DrawerItem("Favorites", Icons.favorite)
  ];
  _getDrawerItemScreen(int pos) {
    return new PlaceholderWidget(Colors.white);
  }

  _onSelectItem(int index) {
    setState(() {
      _selectedIndex = index;
      _getDrawerItemScreen(_selectedIndex);
    });
    Navigator.of(context).pop(); // close the drawer
  }
  @override
  Widget build(BuildContext context) {
    List<Widget> drawerOptions =[];
    for(var i=0; i<drawerItems.length;i++){
      var d=drawerItems[i];
      drawerOptions.add(new ListTile(
        leading: new Icon(d.icon),
        title: new Text(
          d.title,
          style: new TextStyle(fontSize: 19.0, fontWeight: FontWeight.w400),
        ),
        selected: i == _selectedIndex,
        onTap: () =>_onSelectItem(i),
      ));
    }
    return Scaffold(
          appBar: AppBar(
            title: Text('Navigation Drawer Example'),
          ),
          drawer: new Drawer(
            child: ListView(
              // Important: Remove any padding from the ListView.
              padding: EdgeInsets.zero,
              children: <Widget>[
                new UserAccountsDrawerHeader(
                    accountName: new Text(
                      "Temidayo Adefioye",
                      style: new TextStyle(
                        fontWeight: FontWeight.w500, fontSize: 18.0
                      ),
                    ),
                    accountEmail: Text(
                      "temidjoy@gmail.com",
                      style: new TextStyle(
                        fontSize: 18.0, fontWeight: FontWeight.w500
                      ),
                    ),
                currentAccountPicture: CircleAvatar(
                  backgroundColor: Colors.white,
                  child: Text('TA'),
                ),),
                new Column(children: drawerOptions,)
              ],
            ),
          ),
          body: _getDrawerItemScreen(_selectedIndex),
    );
  }
}
class DrawerItem {
  String title;
  IconData icon;

  DrawerItem(this.title, this.icon);
} 
```
 
 
 ## Form Validations

Mobile developers often require users to enter information into a text field. For example, you might be working on an app that requires your users to log in with an email address and password combination. Let's see how we can achieve this without necessarily importing a 3rd party library! Super cool right?

 <img src="https://github.com/Temidtech/Flutter-Cheat-Sheet/blob/master/screenshots/validation.gif" width="280"/> 
 
 You want something like this on your App? Here is how you can achieve this in few lines!
 
  ```dart
  
  class MyApp extends StatelessWidget {
  @override
  Widget build(BuildContext context) {
    final appTitle = 'Form Validation Demo';

    return MaterialApp(
      title: appTitle,
      home: Scaffold(
        appBar: AppBar(
          title: Text(appTitle),
        ),
        body: SingleChildScrollView(
          child: ValidationDemo(),
        )
      ),
    );
  }
}

class ValidationDemo extends StatefulWidget {
  @override
  State<StatefulWidget> createState() {
    return new ValidationDemoState();
  }
}

class ValidationDemoState extends State<ValidationDemo> {
  // Note: This is a GlobalKey<FormState>, not a GlobalKey<ValidationDemoState>!
  final _formKey = GlobalKey<FormState>();
  // Declare a default bool variable isPasswordVisible and initialize to false. 
  // This is the default state of the password visibilty.
  bool isPasswordVisible = false;
  @override
  Widget build(BuildContext context) {
    return new Container(
      margin: new EdgeInsets.all(15.0),
      child: new Form(
        key: _formKey, // Set the _formKey here
        child: formUI(), // Set your custom widget here
      ),
    );
  }
 // Build a custom widget for your app
  Widget formUI() {
    return new Column(
      crossAxisAlignment: CrossAxisAlignment.center,
      children: <Widget>[
        new TextFormField(
          decoration: const InputDecoration(labelText: 'Username'), // Create an optional decoration for your TextFormField
          validator: _validateUsername,
        ),
        new TextFormField(
          decoration: const InputDecoration(labelText: 'Email'),
          validator: _validateEmail,
          keyboardType: TextInputType.emailAddress,
        ),
        new TextFormField(
          keyboardType: TextInputType.text,
          validator: _validatePassword,
          obscureText: isPasswordVisible, //This will obscure text dynamically
          decoration: InputDecoration(
            labelText: 'Password',
            hintText: 'Enter your password',
            // Here is key idea
            suffixIcon: IconButton(
              icon: Icon(
                // Based on passwordVisible state choose the icon
                isPasswordVisible ? Icons.visibility : Icons.visibility_off,
                color: Theme.of(context).primaryColorDark,
              ),
              onPressed: () {
                // Update the state i.e. toogle the state of passwordVisible variable
                setState(() {
                  isPasswordVisible
                      ? isPasswordVisible = false
                      : isPasswordVisible = true;
                });
              },
            ),
          ),
        ),
        Padding(
            padding: const EdgeInsets.symmetric(vertical: 16.0),
            child: RaisedButton(
              onPressed: () {
                if (_formKey.currentState.validate()) {
                  Scaffold.of(context)
                      .showSnackBar(SnackBar(content: Text('Processing data')));
                }
              },
              child: Text('Submit'),
            ))
      ],
    );
  }

  String _validateEmail(String value) {
    if (value.isEmpty) {
      return 'Email field cannot be empty!';
    }
    // Regex for email validation
    String p = "[a-zA-Z0-9\+\.\_\%\-\+]{1,256}" +
        "\\@" +
        "[a-zA-Z0-9][a-zA-Z0-9\\-]{0,64}" +
        "(" +
        "\\." +
        "[a-zA-Z0-9][a-zA-Z0-9\\-]{0,25}" +
        ")+";
    RegExp regExp = new RegExp(p);
    if (regExp.hasMatch(value)) {
      return null;
    }
    return 'Email provided isn\'t valid.Try another email address';
  }
   _validatePassword(String value){
    if(value.isEmpty){
      return 'Password field cannot be empty';
    }

    if(value.length<6){
      return 'Password length must be greater than 6';
    }
  }
   _validateUsername(String value){
    if(value.isEmpty){
      return 'Username  cannot be empty';
    }

    if(value.length<6){
      return 'Username length must be greater than 6';
    }
  }
}

  ```
