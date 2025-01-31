# Direct Access of Private Field in C# Class

This example shows a subtle bug where the private field `_myField` is directly modified in `MyMethod` instead of using the public property `MyProperty`. This can lead to inconsistencies if the property has any additional logic (such as validation, logging, or other side effects).  Good practice dictates always using properties to access and modify the underlying fields.

## Bug
The `bug.cs` file demonstrates direct field access within the class. This violates encapsulation principles and can cause problems if the property's implementation changes in the future.

## Solution
The `bugSolution.cs` shows the corrected approach, always using the property `MyProperty` to interact with the field.