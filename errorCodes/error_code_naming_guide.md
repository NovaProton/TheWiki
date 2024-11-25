# Error Code Naming Guide

This guide describes the conventions for assigning and naming error codes in our projects. Consistent error code conventions help in troubleshooting issues effectively and communicating problems clearly across teams. The following rules apply to error codes based on their source and the nature of the issue.

## General Format for Error Codes

The format of an error code is:

**Sortcode-TheFunction/ErrorContext-ErrorMessage**

- **Sortcode**: Indicates the type of error, starting with one of the prefixes defined below.
- **TheFunction/ErrorContext**: Refers to the function, API, or context where the error occurred.
- **ErrorMessage**: Describes the error, if applicable, for more clarity.

Example: `E9123-GoogleMapsApi-InvalidKeyMapError`

## Error Code Prefixes

### 1. External Errors (`E9`)
Errors that originate from systems or components external to our application (e.g., third-party APIs) should start with **E9**. This helps distinguish between issues that are out of our control.

- **Format**: `E9<UniqueID>-<FunctionName>-<ErrorDescription>`
- **Example**: `E9123-GoogleMapsApi-InvalidKeyMapError`
  - This means there was an error with the Google Maps API, specifically due to an invalid key.

### 2. Internal Dependency Errors (`I8`)
Errors that occur in components we use internally but are not directly part of our written code should start with **I8**. These can include issues within modules, libraries, or services that we depend on internally.

- **Format**: `I8<UniqueID>-<FunctionName>-<ErrorDescription>`
- **Example**: `I8121-DatabaseConnector-ConnectionTimeout`
  - This error relates to a timeout while attempting to connect using an internal database connector.

### 3. Internal Code Errors (`D7`)
Errors that are due to issues within our own codebase should start with **D7**. These are problems arising from bugs or flaws in our implemented logic.

- **Format**: `D7<UniqueID>-<FunctionName>-<ErrorDescription>`
- **Example**: `D7025-DataParser-NullReferenceError`
  - This indicates an error in the `DataParser` function due to a null reference.

## Guidelines for Assigning Error Codes

1. **Unique Identifier (`<UniqueID>`)**:
   - Each error should have a unique identifier following the sortcode prefix. This identifier can be numeric and incremented for each new error type.
2. **Descriptive Context (`<FunctionName>`)**:
   - Use a meaningful name for the function, API, or component where the error occurred to aid in locating the issue quickly.
3. **Clear Error Message (`<ErrorDescription>`)**:
   - Provide a concise description of the problem. This should be consistent with any returned error messages for easy cross-referencing.

## Example Error Codes

- **External Error**: `E9123-PaymentGateway-UnauthorizedAccess`
  - This error code indicates that a third-party payment gateway is rejecting access due to unauthorized credentials.

- **Internal Dependency Error**: `I8112-CacheManager-CacheMiss`
  - This code signals that an internal caching system could not find a requested item.

- **Internal Code Error**: `D7034-UserAuth-InvalidTokenFormat`
  - This error indicates that the token format provided to `UserAuth` is incorrect or malformed.

## Best Practices for Error Codes

1. **Clarity**: Ensure the error message is descriptive enough to provide an idea of what went wrong and why.
2. **Consistency**: Always use the predefined prefixes (`E9`, `I8`, `D7`) to maintain uniformity across projects.
3. **Avoid Reuse**: Each error should have a unique identifier. Avoid reusing error codes, as it can lead to confusion during debugging.
4. **Cross-Reference Documentation**: Maintain an internal document or table listing all error codes, their meanings, and potential resolutions. This can act as a quick reference guide during development or support.
5. **Include in Logs**: Always include the complete error code in application logs to assist with debugging and tracing issues.