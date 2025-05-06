import 'package:flutter/material.dart';

// Reusable BoxDecoration for consistent styling
const BoxDecoration kCardDecoration = BoxDecoration(
  color: Colors.white,
  borderRadius: BorderRadius.all(Radius.circular(12)),
  boxShadow: [
    BoxShadow(
      color: Colors.black12,
      blurRadius: 6,
      offset: Offset(0, 3),
    ),
  ],
);

// Reusable padding or margin constants
const EdgeInsets kContainerPadding = EdgeInsets.all(16.0);
const EdgeInsets kContainerMargin = EdgeInsets.symmetric(vertical: 8.0, horizontal: 12.0);

// Optional reusable Container widget
Widget reusableContainer({required Widget child}) {
  return Container(
    padding: kContainerPadding,
    margin: kContainerMargin,
    decoration: kCardDecoration,
    child: child,
  );
}
import 'package:your_app/constants/container_constants.dart';

...

@override
Widget build(BuildContext context) {
  return Scaffold(
    body: Center(
      child: reusableContainer(
        child: Column(
          children: [
            Text('BMI Result'),
            Text('Your BMI is 23.5'),
          ],
        ),
      ),
    ),
  );
}
