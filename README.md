# CSS Specificity Issue with Hover Effect

This repository demonstrates a subtle issue related to CSS specificity and the `:hover` pseudo-class. The problem occurs when trying to override a hover style using a seemingly more specific selector that, in fact, is less specific due to the way specificity rules operate in CSS.

## Problem

The provided CSS has unexpected behavior. The `hover` effect applied to the class selector `.container.inner` is not being overridden by the seemingly more specific `hover` effect on the descendant selector `.container .inner:hover`.  The second hover style should, logically, be applied, but CSS specificity is preventing this.

## Solution

The solution involves restructuring the CSS to ensure the desired selector has higher specificity. This can be achieved by adjusting the selectors or by using `!important` (generally discouraged).