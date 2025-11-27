# REST API Design Homework

## Objective

## Instructions

You must fork the REST API Design Homework repository to your private GitLab
subgroup of the CS 343 01 02 Fall 2025 group. It will look something like
`Worcester State University / Computer Science Department / CS 343 01 02 Fall 2025 / Students/ username`

**You will be writing all of your answers here in the `REST API Design Homework.md` file.**

---

You will also need your copy of the GuestInfoBackend from your own copy of the `Microservices - Theas Pantry` to try out your tests.

**You will not be committing any of your answers there.**

## *Base Assignment*

**Everyone must complete this portion of the assignment in a *Meets Specification* fashion.**

### Design and Write Manual Tests for POST /guests

1. Design tests for each of the possible responses for `POST /guests`. For each specify the Setup calls, Test(s) call(s), and what you expect for a response (code and returned data.) *You cannot test the 500 responses this way.*

   You do not need to write full, syntactically correct API calls - only enough to know what is needed.

   If you want to create a new UUID for a test - you can generate a *Version
   4 UUID* with this [page](https://www.uuidgenerator.net/version4).

   **Write your answers in this file in the space below:**

   * 201
      * Setup
      * Tests
      * Expected response
   * 400
      * Setup
      * Tests
      * Expected response
   * 409
      * Setup
      * Tests
      * Expected response
2. Translate your tests for `POST /guests` into actual API calls. Add your
   tests to `base.http` **in this repository**. 
3. Copy the `base.http` file to your `guestinfobackend` repository and run
   the tests to verify that the backend works correctly. **You should not commit your `base.http` file to your `guestinfobackend` repository.**

## *Intermediate Add-On*

## Complete this portion in an Acceptable fashion to apply towards base course grades of C or higher

* See the the Course Grade Determination table in the syllabus to see how many Intermediate Add-Ons you need to submit for a particular letter grade.
* See My Grades in Blackboard to see how many you have submitted and received an Acceptable grade on.
* You may not need to submit one for this assignment.

### Design and Write Manual Tests for PUT /guests/{UUID}

1. Design tests for each of the possible responses for `PUT /guests/{UUID}`. For each specify the Setup calls, Test(s) call(s), and what you expect for a response (code and returned data.) *You cannot test the 500 responses this way.*

   You do not need to write full, syntactically correct API calls - only enough to know what is needed.

   If you want to create a new UUID for a test - you can generate a *Version
   4 UUID* with this [page](https://www.uuidgenerator.net/version4).

   **Write your answers in this file in the space below:**

   * 200
      * Setup
      * Tests
      * Expected response
   * 400
      * Setup
      * Tests
      * Expected response
   * 404
      * Setup
      * Tests
      * Expected response
2. Translate your tests for `PUT /guests/{UUID}` into actual API calls. Add 
   your tests to `intermediate-put.http` **in this repository**. 
3. Copy the `intermediate-put.http` file to your `guestinfobackend`
   repository and run the tests to verify that the backend works correctly. **You should not commit your `intermediate-put.http` file to your `guestinfobackend` repository.**

### Design and Write Manual Tests for DELETE /guests/{UUID}

1. Design tests for each of the possible responses for `DELETE /guests/{UUID}`. For each specify the Setup calls, Test(s) call(s), and what you expect for a response (code and returned data.) *You cannot test the 500 responses this way.*

   You do not need to write full, syntactically correct API calls - only enough to know what is needed.

   If you want to create a new UUID for a test - you can generate a *Version
   4 UUID* with this [page](https://www.uuidgenerator.net/version4).

   **Write your answers in this file in the space below:**

   * 200
      * Setup
      * Tests
      * Expected response
   * 400
      * Setup
      * Tests
      * Expected response
   * 404
      * Setup
      * Tests
      * Expected response
2. Translate your tests for `DELETE /guests/{UUID}` into actual API calls. Add 
   your tests to `intermediate-delete.http` **in this repository**. 
3. Copy the `intermediate-delete.http` file to your `guestinfobackend`
   repository and run the tests to verify that the backend works correctly. **You should not commit your `intermediate-put.http` file to your `guestinfobackend` repository.**

## *Advanced Add-On*

### Complete this portion in an Acceptable fashion to apply towards base course grades of B or higher

* See the the Course Grade Determination table in the syllabus to see how many Intermediate Add-Ons you need to submit for a particular letter grade.
* See My Grades in Blackboard to see how many you have submitted and received an Acceptable grade on.
* You may not need to submit one for this assignment.

### Design New Filtering Endpoints

**Write your answers in this file in the space below:**

We would like to have filtering endpoints in the current API, i.e. instead of getting all guests, or just a specific guest (by UUD), we would like to get a subset of guests based on some key/value pair.

The format for such an end point is: `GET /guests?`*key*`=`*value*

1. Add a filtering endpoint design to get all guests who are residents.
    * What would the endpoint look like?
    * What would be the type for the value?
2. Add a filtering endpoint design for `numberInHousehold`.
    1. Filter for all guests with exactly the given number of people in their household.
        * What would the endpoint look like?
        * What would be the type for the value?
    2. Filter for all guests with less than the given number of people in their household.
        * What would the endpoint look like? (You cannot use `<` or `>` instead of the `=` in the query string. The `=` must be there). See the [FHIR prefixes](https://www.hl7.org/fhir/stu3/search.html#prefix) for a possible format.
    3. Filter for all guests with less than or equal to the given number of people in their household.
        * What would the endpoint look like?
    4. Filter for all guests with greater than the given number of people in their household.
        * What would the endpoint look like?
    5. Filter for all guests with greater than or equal to the given number of people in their household.
        * What would the endpoint look like?
3. Add a filtering endpoint design for `assistance`.
    1. You are allowed to have multiple query strings in a request. You separate key/value pairs with an ampersand (`&`).
        * What would the endpoint look like for checking all of the `assistance` values?
        * Discuss the advantages of allowing the user to specify only some of the `assistance` values. What would you handle values of the
        `assistance` keys that are not listed? Why?
    2. You could do this with no query strings, but instead use a request body.
        * What would the request body look like?
        Would it use one of the schemas that are already defined?
        * Would you have to specify every value? If not, why not and what would have to be changed to allow for not specifying every value?
    3. Which would be easier to implement in the backend code if you can compare objects to each other in Javascript?

### Deliverables

The instructor will pull your REST API Design Homework from your GitLab repository to grade it. Make sure:

1. You have pushed all changes to your private repository. (I can’t access local changes on your computer.)

---

&copy; 2025 Karl R. Wurst <karl@w-sts.com>

<!-- markdownlint-disable MD033 -->
<img src="https://mirrors.creativecommons.org/presskit/buttons/88x31/png/by-sa.png" width=100px/>This work is licensed under the Creative Commons Attribution-ShareAlike 4.0 International License. To view a copy of this license, visit [http://creativecommons.org/licenses/by-sa/4.0/](http://creativecommons.org/licenses/by-sa/4.0/) or send a letter to Creative Commons, 444 Castro Street, Suite 900, Mountain View, California, 94041, USA.
