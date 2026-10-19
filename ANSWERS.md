# Flutter Lab Answers

Name: ILGX3_BUTE_MARCVINCENT
Student ID: 241-01057

## Activity 2 - Build Logs

```text
build() called: 4 glasses
build() called: 5 glasses
build() called: 6 glasses
```
## Activity 2 - Experiment Observation

When I removed setState() from _addGlass() and pressed the + button,
the screen stayed at 0 / 6 glasses. The value changed internally,
but Flutter did not rebuild the screen. After restoring setState(),
the counter and progress bar updated when I pressed +.

## Activity 3 - Experiment Observation

When I removed Expanded from the Humidity box, it became narrower
and only used enough width for its content. The other three boxes
shared the remaining space. Expanded allows the four boxes to
share the available width equally.

## Activity 4 - Grid Layout Observation

I added Ice Cream and Chocolate Cake to the menu and marked
Ice Cream as a best seller. When I changed crossAxisCount
from 2 to 3, the menu showed three cards per row and the cards
became smaller. I changed it back to 2 after the experiment.

## Activity 5 - Theme Customization

I changed the ElevatedButton corner radius from 8 to 20, making
its corners more rounded. I also added an HTML skill chip.
When I turned on dark mode, the background, cards, and text
changed colors. Pressing Save displayed a "Saved!" message
at the bottom of the screen.

## Review Questions

1. What is the difference between a StatelessWidget and a StatefulWidget? Give one example of each from this lab.

   A StatelessWidget is for things that never change once they’re drawn, while a StatefulWidget can hold data that changes and redraw the screen when it does. In this lab, the profile card was our StatelessWidget, and the water tracker was our StatefulWidget.

2. Why is a StatefulWidget written as two classes? What does each class do?

    The first class is the widget itself and just describes what it is. The second is the State class, which stores the data that changes and decides how the screen updates when that data changes.

3. In Activity 2, what happened when you changed _glasses outside setState()? Why?

    The number on the screen stayed the same even though the value had changed. That’s because Flutter didn’t know anything changed, so it never rebuilt the widget. Once I put the change inside setState(), the screen updated right away.

4. Looking at the Debug Console in Activity 2, when is build() called?

    build() runs when the widget is first created, and again every time the state changes and the screen needs to refresh.

5. Explain the main axis and the cross axis of a Row and of a Column.

    In a Row, the main axis runs horizontally and the cross axis runs vertically. A Column is the opposite: the main axis runs vertically and the cross axis runs horizontally.

6. In Activity 3, what happened when you removed Expanded from a StatBox? What does Expanded do?

    The boxes shrank and only took as much space as their content needed. Expanded makes widgets split the available space between them, so they fill the row evenly.

7. Why do we use GridView.builder for the menu instead of a Column with many children?

    GridView.builder lays out the menu items in a grid and scrolls, and it builds items as they’re needed. That makes it a better fit for showing lots of items than a long Column.

8. How do Stack and Positioned create the Best seller badge in Activity 4?

    Stack lets the badge sit on top of the menu card, and Positioned places it exactly where we want it, like in a corner.

9. What is the difference between customizing with ThemeData and with a style on one widget? Give one example of each from Activity 5.

    ThemeData sets the look of the whole app, while a style on a widget only changes that one widget. For example, ThemeData changed the app’s overall theme, while the style on the ElevatedButton changed just that button’s corner radius.

10. When you flip the dark-mode switch in Activity 5, which widget holds the state, and how does the change reach MaterialApp?

    The parent widget, MyApp, holds the dark-mode state. When I flip the switch, setState() updates the value, MyApp rebuilds, and MaterialApp applies the new theme.

## GitHub Repository

https://github.com/marcvincentbute-hue/flutter_basics_lab