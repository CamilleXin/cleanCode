# cleanCode


```
// Bad practice
let d; // Non-descriptive variable name
let elapsedDays; // Unnecessary context
let theUsers; // Unnecessary "the" prefix

// Good practice
let users: User[]; // Use meaningful and pronounceable variable names
let isActiveUser: boolean; // Use names that reveal intent
let maxAllowedUsers: number = 100; // Use searchable names

// Function that uses default arguments instead of short circuiting or conditionals
function createMenu(title: string, body: string, buttonText: string = 'OK', cancellable: boolean = true) {
    // ...
}
```

In this example:

1. Use meaningful and pronounceable variable names: users, isActiveUser, and maxAllowedUsers are all examples of meaningful and pronounceable variable names. They clearly indicate what values they hold.

2. Use names that reveal intent: isActiveUser is a good example of a variable name that reveals intent. It's clear that this variable is expected to be a boolean value that indicates whether a user is active.

3. Use searchable names: maxAllowedUsers is a searchable name. If someone wants to find all places in the code where the maximum number of allowed users is used, they can simply search for maxAllowedUsers.

4. Use default arguments instead of short circuiting or conditionals: The createMenu function uses default arguments for buttonText and cancellable. This is clearer and cleaner than using short circuiting or conditionals to assign default values.

5. Avoid adding unnecessary context: In the bad practice example, elapsedDays has unnecessary context. If we are working within a class or module named UserActivity, it's clear that days would refer to the number of days of user activity.

6. Avoid mental mapping: In the bad practice example, d is a poor choice for a variable name because it requires mental mapping. It's not clear what d stands for unless you keep a mental note that d stands for "days".

7. Don't add unneeded prefixes: In the bad practice example, theUsers has an unneeded prefix "the". Just users is clear and sufficient.

Remember, the goal of these principles is to make the code as clear and easy to understand as possible.


```
// Bad practice
function a(n: string, e: string, a: string = 'OK', c: boolean = true) {
    // Non-descriptive function name and parameters
    // ...
}

// Good practice
function createDialogBox(title: string, body: string, buttonText: string = 'OK', cancellable: boolean = true) {
    // Use descriptive function names and default arguments
    // ...
}

// Function that does one thing
function validateUser(user: User): boolean { // Use names that reveal intent
    return user.age >= 18 && user.isActive; // Avoids unnecessary temporary variables
}


interface MenuOptions {
    title: string;
    body: string;
    buttonText?: string;
    cancellable?: boolean;
}

// Good practice
function createMenu(options: MenuOptions) {
    const { title, body, buttonText = 'OK', cancellable = true } = options;
    // ...
}

```
1. Use descriptive function names: createDialogBox and validateUser are examples of descriptive function names. They clearly indicate what the function does.

2. Functions should do one thing: validateUser is a good example of a function that does one thing. It validates whether a user is at least 18 years old and active.

3. Use default arguments instead of short circuiting or conditionals: The createDialogBox function uses default arguments for buttonText and cancellable. This is clearer and cleaner than using short circuiting or conditionals to assign default values.

4. Use names that reveal intent: validateUser is a good example of a function name that reveals intent. It's clear that this function is expected to validate a user based on certain criteria.
