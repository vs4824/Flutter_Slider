# Flutter Slider

The Flutter Sliders package is written natively in Dart for creating highly interactive and UI-rich slider widgets for filtering purposes in Flutter applications.

## Overview

This library is used to create three different types of sliders, namely slider, range slider, and range selector. All these sliders have a rich set of features such as support for both numeric and date values, tooltip, labels, and ticks. The range selector latter accepts any kind of child including Charts.

Disclaimer: This is a commercial package. To use this package, you need to have either a Syncfusion Commercial License or Free Syncfusion Community license. For more details, please check the LICENSE file.

## Slider features

1. Numeric and date support - Select numeric and date value. For date, support is provided up to the 'Seconds' interval.

2. Labels - Render labels for the date and numeric ranges with an option to customize formats based on the requirement. 

3. Ticks and dividers - Show ticks and dividers based on the interval. Also, enable minor ticks between the ticks to indicate the selected values. These options show the selected range in a more intuitive way for the end users. 

4. Tooltip - Render tooltip to show the selected value clearly. It is also possible to customize the format of the text shown in the tooltip. 

5. Thumb icon support - Accepts custom widgets like icon or text inside the thumb. 

6. Discrete selection - Provides an option for selecting only discrete numeric and date values.

7. Highly customizable - In addition to the built-in rich set of features, fully customize the control easily using the wide range of provided options. 

8. Orientation - Supports both horizontal and vertical orientations. 

9. Inversed vertical slider - Provides an option to change the minimum and maximum positions of the vertical slider.

## Range slider features

Range slider supports all the above-mentioned features of the slider in addition to:

1. Orientation - Supports both horizontal and vertical orientations. 

2. Inversed vertical range slider - Provides an option to change the minimum and maximum positions of the vertical range slider.

3. Drag mode - Various dragging options are available to control thumb dragging. The available options are onThumb, betweenThumbs, and both.

4. Interval selection - Allows users to select a particular interval by tapping or clicking in it. Both thumbs will be moved to the current interval with animation.

## Range selector features

Range selector supports all the above-mentioned features(except orientation and inversed slider) of the range slider in addition to:

1. Child support - Add a child of any type inside the range selector. It is also possible to add Charts. With the built-in integration, range selector is smart enough to handle features like segment selection or zooming of a chart based on the selected range in the range selector. Similar to the range slider, it also supports both numeric and date values.

2. Deferred update - Provides an option to defer range updates, allowing you to control when dependent components are updated while thumbs are being dragged continuously. 

## Installation

Install the latest version from pub.

## Slider getting started

Import the following package.

   ```
   import 'package:syncfusion_flutter_sliders/sliders.dart';
   ```

### Add slider to the widget tree

Add the slider widget as a child of any widget. Here, the slider widget is added as a child of the center widget.

   ```
   @override
Widget build(BuildContext context) {
    return MaterialApp(
        home: Scaffold(
            body: Center(
                child: SfSlider(),
              ),
          ),
      );
}
   ```

### Add slider elements 

Add the slider elements such as ticks, labels, and tooltip to show the current position of the slider thumb.

Horizontal slider

   ```
   double _value = 40.0;

@override
Widget build(BuildContext context) {
  return Scaffold(
     appBar: AppBar(
       title: const Text('Syncfusion Flutter Slider'),
     ),
     body: SfSlider(
       min: 0.0,
       max: 100.0,
       value: _value,
       interval: 20,
       showTicks: true,
       showLabels: true,
       enableTooltip: true,
       minorTicksPerInterval: 1,
       onChanged: (dynamic value){
         setState(() {
           _value = value;
         });
       },
     ),
   );
}
   ```

Vertical slider

   ```
   double _value = 40.0;

@override
Widget build(BuildContext context) {
  return Scaffold(
    appBar: AppBar(
      title: const Text('Syncfusion Flutter Vertical Slider'),
    ),
    body: SfSlider.vertical(
      min: 0.0,
      max: 100.0,
      value: _value,
      interval: 20,
      showTicks: true,
      showLabels: true,
      enableTooltip: true,
      minorTicksPerInterval: 1,
      onChanged: (dynamic value) {
        setState(() {
          _value = value;
        });
      },
    ),
  );
}
   ```

## Range slider getting started

Import the following package.

   ```
   import 'package:syncfusion_flutter_sliders/sliders.dart';
   ```

### Add range slider to the widget tree

Add the range slider widget as a child of any widget. Here, the range slider widget is added as a child of the center widget.

   ```
   @override
Widget build(BuildContext context) {
    return MaterialApp(
        home: Scaffold(
            body: Center(
                child: SfRangeSlider(),
              ),
          ),
      );
}
   ```

### Add range slider elements

Add the range slider elements such as ticks, labels, and tooltips to show the current position of the range slider thumb.

Horizontal range slider

   ```
   SfRangeValues _values = SfRangeValues(40.0, 80.0);

@override
Widget build(BuildContext context) {
   return Scaffold(
     appBar: AppBar(
       title: const Text('Syncfusion Flutter Range Slider'),
     ),
     body: SfRangeSlider(
        min: 0.0,
        max: 100.0,
        values: _values,
        interval: 20,
        showTicks: true,
        showLabels: true,
        enableTooltip: true,
        minorTicksPerInterval: 1,
        onChanged: (SfRangeValues values){
          setState(() {
            _values = values;
          });
        },
      ),
   );
}
   ```

Vertical range slider

   ```
   SfRangeValues _values = SfRangeValues(40.0, 80.0);

@override
Widget build(BuildContext context) {
  return Scaffold(
    appBar: AppBar(
      title: const Text('Syncfusion Flutter Vertical Range Slider'),
    ),
    body: SfRangeSlider.vertical(
      min: 0.0,
      max: 100.0,
      values: _values,
      interval: 20,
      showTicks: true,
      showLabels: true,
      enableTooltip: true,
      minorTicksPerInterval: 1,
      onChanged: (SfRangeValues values) {
        setState(() {
          _values = values;
        });
      },
    ),
  );
}
   ```