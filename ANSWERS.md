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