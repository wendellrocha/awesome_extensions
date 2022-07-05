# Awesome Extensions

[![pub package](https://img.shields.io/pub/v/awesome_extensions.svg?label=awesome_extensions&color=blue)](https://pub.dev/packages/awesome_extensions)
[![popularity](https://badges.bar/awesome_extensions/popularity)](https://pub.dev/packages/awesome_extensions/score)
[![likes](https://badges.bar/awesome_extensions/likes)](https://pub.dev/packages/awesome_extensions/score)
[![pub points](https://badges.bar/awesome_extensions/pub%20points)](https://pub.dev/packages/awesome_extensions/score)

![awesome_extensions](https://github.com/jayeshpansheriya/awesome_extensions/blob/main/flutter_extension.png?raw=true)


## Let get started 💪

1. Go to `pubspec.yaml`
2. add a awesome_extensions and replace `[version]` with the latest version:

```dart
dependencies:
 awesome_extensions: ^[version]
 ```

3. click the packages get button or *flutter pub get*

## See [awesome_extensions](https://jayeshpansheriya.github.io/awesome_extensions) for docs & samples

- [About Awesome Extensions](#about)
- [Theme Extensions](#theme-extensions)
  - [TextStyle](#textstyle)
  - [Text](#text)

## About
An extension to the widget helps reduce the boilerplate and adds some helpful methods. and you can make a responsive design.


## Theme Extensions
#### TextStyle
From the `TextStyle` Access properties right in the `context` instance.

```dart
// Before
Text('Hello World',style: Theme.of(context).textTheme.labelSmall),

Text('Hello World', style: TextStyle(color: Colors.grey, fontWeight: FontWeight.bold, fontSize: 40)

// After
Text('Hello World',style: context.labelSmall),
// OR
Text('Hello World',style: context.displaySmall),
// If you want to bold text then 
Text('Hello World',style: context.labelSmall.bold),   
```
Similar fontWeight are:
* `mostThick` The most thick - FontWeight.w900
* `extraBold` Extra-bold - FontWeight.w800
* `bold` Bold - FontWeight.bold - FontWeight.w700
* `semiBold` Semi-bold - FontWeight.w600
* `medium` Medium - FontWeight.w500
* `regular` Regular - FontWeight.w400
* `light` Light - FontWeight.w300
* `extraLight` Extra-light - FontWeight.w200
* `thin` Thin, the least thick - FontWeight.w100


Similar 2021 TextStyle are:
* `context.displayLarge`
* `context.displayMedium`
* `context.displaySmall`
* `context.headlineLarge`
* `context.headlineMedium`
* `context.headlineSmall`
* `context.titleLarge`
* `context.titleMedium`
* `context.titleSmall`
* `context.bodyLarge`
* `context.bodyMedium`
* `context.bodySmall`
* `context.labelLarge`
* `context.labelMedium`
* `context.labelSmall`

#### Text
If you dont want use theme, then we have some other methods:

```dart
Text('Hello World')
    .bold()
    .fontSize(25)
    .italic();
```
Similar methods are:
*`.textScale()`  TextScale
*`.bold()`  Bold Text
*`.italic()`  Italic Text
*`.fontWeight()`  Specific FontWeight
*`.fontSize()`  Specific FontSize
*`.letterSpacing()`  Specific LetterSpacing
*`.wordSpacing()`  Specific WordSpacing
*`.fontFamily()`  Specific FontFamily
*`.textShadow()`  Specific TextShadow
*`.textColor()`   TextColor
*`.textAlignment()`  Specific TextAlignment
*`.withUnderLine()`  TextUnderLine


#### Theme
From the `Theme` class. Access your themes right in the `context` instance.

* `context.theme`
* `context.textTheme`
* `context.primaryTextTheme`
* `context.bottomAppBarTheme`
* `context.bottomSheetTheme`
* `context.appBarTheme`
* `context.backgroundColor`
* `context.primaryColor`
* `context.primaryColorLight`
* `context.primaryColorDark`
* `context.focusColor`
* `context.hoverColor`
* `context.dividerColor`
* `context.scaffoldBackgroundColor`

  
## Media Query Extensions For Responsive Layout
From the `MediaQuery` Access properties right in the `context` instance.
* `context.height`  /// Height of the Screen, Equivalent to : MediaQuery.of(context).size.height,
* `context.width`   // Width of Screen
* `context.mediaQuerySize`
* `context.orientation`
* `context.mediaQueryPadding`
* `context.alwaysUse24HourFormat`
* `context.devicePixelRatio`
* `context.platformBrightness`
* `context.textScaleFactor`
* `context.isLandscape`
* `context.isPortrait`
* `context.mediaQueryViewPadding`
* `context.mediaQueryViewInsets`
* `context.mediaQueryShortestSide`
* `context.showNavbar`    // True if width be larger than 800
* `context.isPhone`       // True if the shortestSide is smaller than 600p
* `context.isTablet`      // True if the current device is Tablet
* `context.isSmallTablet`   // True if the shortestSide is largest than 600p
* `context.isLargeTablet`    // True if the shortestSide is largest than 720p


```dart
//Check in what platform the app is running
MyPlatform.isAndroid
MyPlatform.isIOS
MyPlatform.isMacOS
MyPlatform.isWindows
MyPlatform.isLinux
MyPlatform.isFuchsia

//Check the device type
MyPlatform.isMobile
MyPlatform.isDesktop
//All platforms are supported independently in web!
//You can tell if you are running inside a browser
//on Windows, iOS, OSX, Android, etc.
MyPlatform.isWeb


// Returns a value<T> according to the screen size
// can give value for:
// mobile: if the shortestSide is smaller than 600
// tablet: if the shortestSide is smaller than 1200
// desktop: if width is largest than 1200
context.responsiveValue<T>(
  T? watch,
    T? mobile,
    T? tablet,
    T? desktop,
)
```


## Navigation Extensions
From the `Navigator` Access properties right in the `context` instance.

```dart
// Before
Navigator.push(
    context,
    MaterialPageRoute(builder: (context) => SecondScreen()),
  );

// After

// for push
context.push(SecondScreen());
context.pushNamed('/home');

// for back , you can also add back result data
context.pop();

// for replace
context.pushReplacement(SecondScreen());
context.pushReplacementNamed('/home');

// popUntil
context.popUntil('/login');
```

## Widget Extensions
This extension is reduced more code.
#### SizeBox
```dart
// Before
SizedBox(
    height : 20.0
   )
// After
// make space of 20.0 height
20.0.heightBox

// for width
20.0.widthBox
```

#### Padding

```dart
// Before
Padding(
  padding: const EdgeInsets.all(8.0),
  child: Text("text"),
);

// After
Text("text").paddingAll(8.0),
```

Similar padding extensions are:
* `paddingAll` Creates insets from offsets from all side.
* `paddingOnly` Creates insets with only the given values non-zero.
* `paddingLTRB` Creates insets from offsets from the left, top, right, and bottom.
* `paddingSymmetric` Creates insets with symmetrical vertical and horizontal offsets.
* `paddingFromWindowPadding` Creates insets that match the given window padding.


#### Other
Now we can just add round corners, shadows, align, and added gestures to our Widgets.
```dart
Container(
      height: 100,
       width: 100,)
         .withRoundCorners(backgroundColor: Colors.grey)
         .withShadow()
         .alignAtCenter()
         .toCenter()
         .withTooltip('My Tooltip')
         .paddingOnly(left: 10)
         .paddingAll(20)
         .onTap(() => print('tap'))
         .onLongPress(() => print('long press'))
```
Automatic detect platform and show material and cupertino dialog
```dart
context.showAlertDialog(title: 'title',
                        message: 'message',)
```

#### Shimmer Effect

```dart
Container(height: 50,width: 50,).applyShimmer();
```
you can also change color of shimmer using `Color baseColor`, `Color highlightColor`.

## Date Extensions

```dart
// for check two date are same or not
date.isSameDate(otherdate);    // its return bool (true/false)

// for check date is today's date
date.isToday    // its return bool (true/false)

// for check this date is yesterday's date
date.isYesterday    // its return bool (true/false)
```

## Number Extensions
#### Future & Duration
Utility to delay some callback (or code execution).
```dart
print('+ wait for 2 seconds');
await 2.delay();
print('- 2 seconds completed');
print('+ callback in 1.2sec');
1.delay(() => print('- 1.2sec callback called'));
```
Easy way to make Durations from numbers.
```dart
print(1.seconds + 200.milliseconds);
print(1.hours + 30.minutes);
print(1.5.hours);

5.isLowerThan(4);
5.isGreaterThan(4);
5.isEqual(4);
```

## String Extensions
```dart
//your name => Your Name,
'your name'.capitalize();
//your name => Your name,
'your name'.capitalizeFirst();
//your name => yourname
'your name'.removeAllWhitespace();

// match any RegExp
'dsts'.hasMatch("'r'[A-Z]");
//return bool if match RegExp
'123'.isNumericOnly();
'dsf'.isAlphabetOnly();
'Ajh'.hasCapitalletter();
'true'.isBool();
```

## Url Strategy

With a simple call of `setPathUrlStrategy`, your Flutter web app does not have a leading `#`
in the URL anymore 🚀
```dart
void main() {
// Here we set the URL strategy for our web app.
// It is safe to call this function when running on mobile or desktop as well.
setPathUrlStrategy();
runApp(MyApp());
}
```


## Avatar Image
```dart
AvatarImage(
   backgroundImage: NetworkImage(
    'https://mdbootstrap.com/img/Photos/Avatars/img%20%281%29.jpg'),
     shape: AvatarImageShape.standard,
     size: ImageSize.LARGE,
     child: Text('Lucky'),
          backgroundColor: Colors.red,
      ),

AvatarImage(
    shape: AvatarImageShape.circle,
    child: Text('JP'),
    backgroundColor: Colors.red,
      ),
```
![avatar-image](https://github.com/jayeshpansheriya/awesome_extensions/blob/main/avatar-image.jpeg)
![avatar-image](https://github.com/jayeshpansheriya/awesome_extensions/blob/main/avatar-name.jpeg)

| Properties      | Description                                                                                                |
| --------------- | ---------------------------------------------------------------------------------------------------------- |
| child           | type of [Widget], which can have text , icon etc                                                           |
| backgroundColor | Color to fill the background of avatar                                                                     |
| foregroundColor | Color to change the textColor inside the avatar                                                            |
| radius          | size of the avatar                                                                                         |
| minRadius       | minimum size of the avatar                                                                                 |
| maxRadius       | maximun size of the avatar                                                                                 |
| size            | size of the avatar i.e `ImageSize.large`, `ImageSize.medium`, `ImageSize.small`                            |
| shape           | shape of the avatar i.e, `AvatarImageShape.standard`, `AvatarImageShape.circle`, `AvatarImageShape.square` |
| borderRadius    | extra radius to avatar shapes, not applicable to circular avatar                                           |


## Support
You liked this package? then give it a star. If you want to help then:

* Start this repository
* Send a Pull Request with new features
* Share this package
* Create issues if you find a Bug or want to suggest something

## ❤️❤️❤️

Supported by [JetBrains Open Source](https://www.jetbrains.com/community/opensource/#support)

[<img src="https://raw.githubusercontent.com/nslogx/flutter_easyloading/master/images/jetbrains.png" width=200 height=112/>](https://www.jetbrains.com/?from=FlutterEasyLoading)

