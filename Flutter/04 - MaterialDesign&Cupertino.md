## Material Design Widgets

Material Design is a design language developed by Google, widely used in Android applications. Flutter provides a set of widgets that follow Material Design guidelines.

Material widgets provide a consistent look and feel across different platforms, including Android, iOS, and the web.

```dart
import 'package:flutter/material.dart';

class MaterialScreen extends StatelessWidget {
  @override
  Widget build(BuildContext context) {
    return Scaffold(
      appBar: AppBar(
        title: Text('Material Design'),
      ),
      body: Center(
        child: Column(
          mainAxisAlignment: MainAxisAlignment.center,
          children: [
            RaisedButton(
              onPressed: () {},
              child: Text('Raised Button'),
            ),
            SizedBox(height: 20),
            FloatingActionButton(
              onPressed: () {},
              child: Icon(Icons.add),
            ),
            SizedBox(height: 20),
            Card(
              child: Padding(
                padding: EdgeInsets.all(16.0),
                child: Text('This is a Material Card'),
              ),
            ),
          ],
        ),
      ),
    );
  }
}

```

In this example, we use various Material widgets such as AppBar, RaisedButton, FloatingActionButton, and Card to create a Material Design-based screen. These widgets provide a consistent and visually appealing user interface.

## Cupertino Widgets

Cupertino is the design language developed by Apple for iOS applications. Flutter provides a set of widgets that follow Cupertino design guidelines.

Cupertino widgets provide the iOS-style look and feel, allowing you to build applications that match the native iOS experience.

```dart
import 'package:flutter/cupertino.dart';

class CupertinoScreen extends StatelessWidget {
  @override
  Widget build(BuildContext context) {
    return CupertinoPageScaffold(
      navigationBar: CupertinoNavigationBar(
        middle: Text('Cupertino Widgets'),
      ),
      child: Center(
        child: Column(
          mainAxisAlignment: MainAxisAlignment.center,
          children: [
            CupertinoButton(
              onPressed: () {},
              child: Text('Cupertino Button'),
            ),
            SizedBox(height: 20),
            CupertinoActivityIndicator(),
            SizedBox(height: 20),
            CupertinoTextField(
              placeholder: 'Enter text',
            ),
          ],
        ),
      ),
    );
  }
}

```

In this example, we use various Cupertino widgets such as CupertinoPageScaffold, CupertinoNavigationBar, CupertinoButton, CupertinoActivityIndicator, and CupertinoTextField to create an iOS-style screen. These widgets provide the familiar iOS design elements and interactions.

## Adaptive Widgets

Flutter also provides adaptive widgets that automatically adapt to the platform-specific design guidelines.

These widgets allow you to build applications that look and feel native on both Android and iOS platforms.

```dart
import 'package:flutter/cupertino.dart';
import 'package:flutter/material.dart';

class AdaptiveScreen extends StatelessWidget {
  @override
  Widget build(BuildContext context) {
    return Scaffold(
      appBar: AppBar(
        title: Text('Adaptive Widgets'),
      ),
      body: Center(
        child: Column(
          mainAxisAlignment: MainAxisAlignment.center,
          children: [
            Platform.isAndroid
                ? RaisedButton(
                    onPressed: () {},
                    child: Text('Raised Button (Android)'),
                  )
                : CupertinoButton(
                    onPressed: () {},
                    child: Text('Cupertino Button (iOS)'),
                  ),
            SizedBox(height: 20),
            Platform.isAndroid
                ? CircularProgressIndicator()
                : CupertinoActivityIndicator(),
            SizedBox(height: 20),
            Platform.isAndroid
                ? TextField(
                    decoration: InputDecoration(
                      hintText: 'Enter text',
                    ),
                  )
                : CupertinoTextField(
                    placeholder: 'Enter text',
                  ),
          ],
        ),
      ),
    );
  }
}

```

In this example, we use adaptive widgets such as RaisedButton and CupertinoButton, CircularProgressIndicator, and TextField and CupertinoTextField. The widgets used will adapt to the respective platform (Android or iOS) based on the condition.