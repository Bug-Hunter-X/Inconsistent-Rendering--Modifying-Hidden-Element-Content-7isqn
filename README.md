# Inconsistent Rendering: Modifying Hidden Element Content

This repository demonstrates an uncommon HTML bug related to modifying the innerHTML of an element after its display style has been set to 'none'.  The behavior is inconsistent across different browsers, and some might not render the added content correctly.

The `bug.html` file showcases the issue.  `bugSolution.html` offers a corrected approach.

## Problem

The bug occurs when attempting to add content to an HTML element after setting its `display` style to `'none'`.  While the behavior might vary, the most likely outcome is that the added content will not be visible or rendered correctly when the element's display is subsequently changed back to `'block'` or `'inline'`.

## Solution

The best practice is to avoid modifying the content of an element after it has been hidden.  If modification is necessary, modify the content *before* setting the display style to `'none'`.  Alternatively, ensure you're only doing so after display has been changed back to `block` or `inline`

## Reproducing the Bug

1. Open `bug.html` in your web browser.
2. Observe that the second paragraph of text is not displayed, even though it's part of the innerHTML.