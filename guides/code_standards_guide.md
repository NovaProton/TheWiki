# Code Standards Guide

This guide outlines the coding standards we follow to ensure consistency, readability, and maintainability across our projects. Please adhere to these standards whenever working on our codebase.

## General Principles

1. **Consistency**: Maintain consistency in style, formatting, and naming conventions across all files.
2. **Readability**: Write code that is easy to understand, with meaningful comments where needed.
3. **Simplicity**: Avoid over-engineering. Strive for simplicity without sacrificing functionality.
4. **Document**: Ensure that complex logic is documented clearly, either with comments or supporting documentation.

## Naming Conventions

- **Variables**: Use camelCase for variable names (`exampleVariableName`). Avoid abbreviations unless they are widely understood.
- **Constants**: Use ALL_CAPS with underscores (`MAX_BUFFER_SIZE`).
- **Functions**: Use descriptive names in camelCase (`calculateAverage`). Start with a verb that indicates action.
- **Classes**: Use PascalCase for class names (`UserAccount`).
- **Files**: Use descriptive, lowercase names with underscores for file names (`data_processor.cpp`).

## Code Formatting

1. **Indentation**: Use 4 spaces for indentation. Avoid tabs.
2. **Line Length**: Keep lines to a maximum of 80 characters, where possible, to improve readability.
3. **Braces**: Always use braces `{}` for conditionals and loops, even for single-line statements.
   ```cpp
   if (condition) {
       doSomething();
   }
   ```
4. **Spacing**: Place a space after commas, and around operators (`=`, `+`, `-`, etc.).
5. **Blank Lines**: Use blank lines to separate logical blocks of code, such as between functions or class methods.

## Comments

1. **Inline Comments**: Use inline comments sparingly to clarify non-obvious code. Avoid redundant comments.
   ```cpp
   int speed = calculateSpeed(); // Get the current speed based on input values
   ```
2. **Block Comments**: Use block comments to describe complex logic or non-trivial methods.
   ```cpp
   /*
    * Calculate the final price by applying discounts and taxes.
    * This method assumes that all inputs are validated.
    */
   double calculateFinalPrice(double basePrice, double discountRate, double taxRate);
   ```
3. **Documentation Comments**: Use Doxygen-style comments for functions, classes, and methods.
   ```cpp
   /**
    * @brief Calculates the average of an array of numbers.
    *
    * @param numbers Array of double values.
    * @param count Number of elements in the array.
    * @return The average value as a double.
    */
   double calculateAverage(const double numbers[], int count);
   ```

## Error Handling

- **Check for Errors**: Always validate inputs and handle potential errors. Avoid silent failures.
- **Use Assertions**: Use `assert()` for conditions that should never happen, but ensure these checks are only in debug builds.
- **Return Meaningful Errors**: When returning error codes, use descriptive enumerations rather than simple integers.

## File Organisation

1. **Headers and Implementation**: Separate declaration (`.h`) and implementation (`.cpp`) files.
2. **Include Guards**: Use `#ifndef`, `#define`, and `#endif` to prevent multiple inclusions in header files.
   ```cpp
   #ifndef DATA_PROCESSOR_H
   #define DATA_PROCESSOR_H

   class DataProcessor {
       // Class declaration here
   };

   #endif // DATA_PROCESSOR_H
   ```
3. **Include Order**: Include standard libraries first, followed by third-party libraries, and then project headers.

## Testing and Quality

- **Unit Tests**: Write unit tests for functions that perform non-trivial logic. Use a testing framework, like Google Test.
- **Code Review**: Always have at least one other team member review your code before merging.
- **Static Analysis**: Run static analysis tools to catch potential issues early.S