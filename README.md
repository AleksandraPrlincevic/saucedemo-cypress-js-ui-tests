</> Markdown
# SauceDemo Cypress Test Automation Project
## Description
End-to-end test automation framework for [SauceDemo](https://www.saucedemo.com/), built with **Cypress** and **JavaScript**, using the Page Object Model (POM) pattern.

This project was built as a portfolio project to practice UI test automation. A companion project testing the same site manually and with **Java + Selenium** 
is available here:  [Java/Selenium version of this project](https://github.com/AleksandraPrlincevic/saucedemo-selenium-java-ui-tests).

## Tech Stack

- Node.js v24.22.2
- Cypress 15.18.0 – end-to-end testing framework
- Mocha – test runner (bundled with Cypress)
- Chai – assertion library (bundled with Cypress)
- JavaScript
- Page Object Model (POM) design pattern
- Run on Windows 11

## Project Structure

```

cypress/
├───e2e/                # Test spec files
├───fixtures/           # Test data (JSONs)
├───pages/              # Page Objects and component classes
└───support/            # Custom commands and global config

```
## How to run

### Prerequisites

- Node.js 20.1 or newer, except odd-numbered versions (tested with v24.22.2)

### Installation

Clone the repository and install dependencies:

```bash
git clone https://github.com/AleksandraPrlincevic/saucedemo-cypress-js-ui-tests.git
cd saucedemo-cypress-js-ui-tests
npm install
```

### Running the tests

Open Cypress in interactive mode:

```bash
npx cypress open
```

Or run all tests headlessly in the terminal:

```bash
npx cypress run
```
## What's Covered

19 automated tests across 5 spec files.

- **Login** – valid/invalid credentials, locked-out user, required-field validation
- **Sorting** – price (low-high, high-low) and name (A-Z, Z-A) sorting on the Inventory page
- **Cart** – adding and removing items from the cart
- **`problem_user` regression suite** – a dedicated set of tests documenting known, existing bugs on the `problem_user` account (e.g. identical product images, non-functional sort/remove buttons). These tests are written to **pass while the bugs exist** and would need to be flipped once/if the underlying bugs are fixed.

## Notes

This is a learning/portfolio project — some scenarios were chosen specifically to practice writing precise assertions and to explore edge cases (e.g. broken user accounts) beyond the standard "happy path".
