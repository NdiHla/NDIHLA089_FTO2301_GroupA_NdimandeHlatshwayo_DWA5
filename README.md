# NDIHLA089_FTO2301_GroupA_NdimandeHlatshwayo_DWA5

This is a JavaScript code snippet that handles a form submission to perform a division operation. Let's go through the code step by step:

1. The code selects the form element using the attribute selector `[data-form]` and assigns it to the `form` constant.
2. It also selects the result element using the attribute selector `[data-result]` and assigns it to the `result` constant.
3. The code adds an event listener to the form for the "submit" event.
4. When the form is submitted, the event listener callback function is executed.
5. The `event.preventDefault()` method is called to prevent the default form submission behavior, which would cause a page reload.
6. Inside a `try` block, the code creates a new `FormData` object from the submitted form data.
7. The `Object.fromEntries(entries)` method is used to convert the form data entries into an object with key-value pairs.
8. The `dividend` and `divider` variables are destructured from the object, representing the values entered in the form inputs.
9. The code checks if either the `dividend` or `divider` values are missing. If either of them is missing, an error message is displayed in the `result` element, and the function returns to exit further execution.
10. Next, the code checks if the `dividend` is less than 0 or the `divider` is less than or equal to 0. If either condition is true, an error message is displayed, and an `Error` object is thrown to exit the execution.
11. The code then checks if both `dividend` and `divider` are valid numbers using `Number.isNaN()` and `Number()` functions. If either of them is not a valid number, an error message is displayed, and an `Error` object is thrown.
12. If all the input validation checks pass, the code performs the division by calculating `dividend / divider` and displays the result as the floor value in the `result` element.
13. If any error is caught in the `catch` block, an error message is displayed in the `result` element, and the error stack trace is logged to the console.

This code ensures that both the dividend and divider are provided, valid numbers, and performs the division operation when the form is submitted.