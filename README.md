# CSS `calc()` with Percentage Values: Unexpected Behavior

This repository demonstrates a common issue encountered when using the CSS `calc()` function with percentage values.  The problem arises when the percentage is dependent on a parent element's dimensions, and those dimensions are not yet resolved at the time of calculation. This often leads to unexpected results, such as misaligned or incorrectly sized elements. The `bug.css` file shows the problematic code, while `bugSolution.css` offers a potential solution.

## Problem

The issue is rooted in the order of CSS processing and the way percentages are resolved. Percentages are relative to the parent element's computed dimensions. If the parent's dimensions are not available when `calc()` is evaluated, the calculation may use incorrect values.

## Solution

The solutions often involve ensuring the parent's dimensions are resolved before the calculation is performed. Techniques like setting explicit dimensions on the parent or restructuring the CSS to remove the dependency on the yet-to-be-resolved dimensions are effective strategies.