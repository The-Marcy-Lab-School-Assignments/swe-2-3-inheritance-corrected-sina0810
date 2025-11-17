# Technical Coding Feedback

## Overview Takeaways

Your code demonstrates good understanding of JavaScript inheritance, `extends`, and `super()`. Most classes are correctly implemented, but there are several issues that need attention: inconsistent formatting and indentation, missing semicolons, redundant code in the DVD constructor (duplicating `this.title` and setting `this.isCheckedOut` without a value), and the Square class doesn't set the type.

## Inline Feedback

### Problem Set 1: Shapes

**Lines 3-10 (shapes.js)**: The `Shape` class is correctly implemented, but formatting needs improvement.

**Line 4**: Missing space after `constructor` - should be `constructor(type) {` not `constructor(type){`

**Lines 12-20 (shapes.js)**: The `Circle` class is correctly implemented with proper use of `extends Shape` and `super("Circle")`.

**Lines 22-31 (shapes.js)**: The `Rectangle` class is correctly implemented. Good inheritance pattern.

**Lines 33-38 (shapes.js)**: The `Square` class is correctly implemented.

**Line 35**: The Square class doesn't set `this.type = 'Square'`. While this may work if the tests don't check the type, it's good practice to set it explicitly. However, since Rectangle calls `super('Rectangle')` with a hardcoded type, you might need to manually set it.

**Lines 4-5, 14-15, 23-26, 35**: Missing semicolons throughout, though JavaScript's automatic semicolon insertion will handle this.

### Problem Set 2: Library Items

**Lines 3-20 (library-items.js)**: The `LibraryItem` class is correctly implemented. Note: Your implementation uses `year` instead of `author` as the second parameter, and includes `checkOut()` and `returnItem()` methods. This may be a different version of the assignment - verify against your README requirements.

**Lines 22-32 (library-items.js)**: The `Book` class is correctly implemented with proper use of `extends LibraryItem` and `super()`. Excellent use of `super.getDescription()` in the override!

**Line 23**: Missing space after comma: `author,pages` → `author, pages`

**Lines 34-46 (library-items.js)**: The `DVD` class has some issues.

**Line 37**: Redundant - `this.title = title` is already set by the parent constructor via `super(title, year)`. You don't need to set it again.

**Line 40**: `this.isCheckedOut;` doesn't do anything - it's just a statement that doesn't assign a value. This is unnecessary since `isCheckedOut` is already initialized in the parent class.

**Lines 48-57 (library-items.js)**: The `Magazine` class is correctly implemented. Good inheritance pattern.

**Lines 4-6, 9-11, 13-15, 17-18, 24-26, 28-29, 35-39, 42-43, 49-51, 53-54**: Missing semicolons throughout.

## Code Quality Observations

### Strengths

1. **Good Inheritance**: Proper use of `extends` keyword throughout.
2. **Proper Use of super()**: Correctly calling `super()` in constructors and `super.methodName()` in overridden methods.
3. **Method Overriding**: Good understanding of when and how to override methods, and excellent use of `super.getDescription()` to avoid code duplication.

### Areas for Improvement

1. **Formatting**: Improve indentation and spacing for consistency (e.g., `constructor(type){` should be `constructor(type) {`)
2. **Semicolons**: Add semicolons consistently throughout the code.
3. **Remove Redundant Code**: Remove `this.title = title` and `this.isCheckedOut;` from DVD constructor.
4. **Square Type**: Consider setting `this.type = 'Square'` in the Square constructor.

## Summary

Your code demonstrates good understanding of inheritance, and your use of `super.getDescription()` is excellent! The main issues are formatting consistency and some redundant code. Once these are addressed, your code should pass all tests. Great work on the overall structure and inheritance implementation!

