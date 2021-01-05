## Credit Card Checker_Codecademy Project

### Purpose

Credit Card Checker allows for an array of card numbers to entered and validated. 

Outputs the names of all the companies issuing invalid cards.

### _Function Roles_  

#### ValidateCred (Checks if Card Number is Invalid)  

* Iterate from the far right of the Array excluding the last element (check digit) which is stored in __checkDigit__
    * Every other element from the right is multipled by 2
        * These elements will be stored in __doubled__
        * If the result is >= 9, 9 is subtracted from the result.
    * every other element is added and stored into __single__
    * Total Sums the above variables and Module 10
        * if 0;
            * Returns *True*
        * if remainder
            * Returns *False*

#### FindInvalidCards  

* Iterates over a nested array of card numbers
    * __credNum__ stores the value from ValidateCred Function (True/False)
        * If False, that array is pushed into __invalidCards__ 
* Function returns the new nested array of Invalid Cards Only in __invalidCards__

#### idInvalidCompanies  

* Higher Order Function which takes in callback function __findInvalidCards__
* Returned array __invalidCards__ are stored in __K__
* __K__ is itterated over, checked the first element (0) of each nested Array (i) using a loop. 
* Stores the corresponding names into __invalidCompanies__

* __companyName__ uses new Set function to remove all duplicate company names from __invalidCompanies__
* __finalCompanies__ lists the company names from which the invalid cards originated.
* returns __finalCompanies__

### Call

console.log(idInvalidCompanies(findInvalidCards(batch)));

### Future Updates

* Accept a string (card number) from the user.
* Output the actual invalid card numbers

