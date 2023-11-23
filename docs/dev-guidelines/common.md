# Common Guidelines for all language
Irrespective of programming language, it is important to write consistent and aesthetically pleasing code

## Naming Conventions
Follow the below naming conventions (unless specefically defined for the specefic language)

#### Use lowerCamelCase for variables, properties and function names

Variables, properties and function names should use `lowerCamelCase`. They should also be descriptive. Single character variables and uncommon abbreviations should generally be avoided.

_Right Usage_

`const adminUser = db.query('SELECT * FROM users ...');`

_Avoid_

`const admin_user = db.query('SELECT * FROM users ...');`

#### Use UpperCamelCase for class names
Class names should be capitalized using `UpperCamelCase`.

_Right Usage_

`class CustomerAccount {}`

_Avoid_

`class customer_Account {}`

#### Upper Case for Constants
Constants should be declared as regular variables or static class properties, using all uppercase letters.

_Right Usage_

`const SECOND = 1 * 1000;`

_Avoid_

`const second = 1 * 1000;`


## Code Comments
Writing code comments is mandatory. Don't be a 'miser' when it comes to writing code comments.

Every method / function (specially if it has business logic) must have code comments that explains the business logic.

_Right Usage_

```
function calculateCashback() {
    /*
    * On invoice paid event, we create payment(s) in obno with status as `Successful`
    * Check if invoice is created for the order, if created then update the status as `PAID`, else create a new invoice and update the status
    * Award cashback to the customer for the order
    * Award cashback to the referrer if the customer has been referred and has ordered for the first time
    * */
}
```

_Avoid_

```
function calculateCashback() {
    // This method calculates cashback.
}
```

