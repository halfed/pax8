# Pax8 Front-end Developer Homework

#### Install Dependencies
```
npm install
```

#### Run app
```
npm run serve
```

## Homework Instructions

You are free to use any Vue plugin or npm module to complete the homework. Style the app using the [Bulma](https://bulma.io/documentation/) framework. It has already been imported for you.

Please email back within 4 hours of receiving (csmoak@pax8.com). Zip the app folder without the `node_modules` folder.

----

Using the `CompanyService.js` (fake company data):

1. Display a list of companies
   1. Include `id` and `name` values in list
   2. Also include an edit button.
2. Build an edit company page
   1. Display a form to edit company details
   2. Upon submitting the form, alert with new details.
3. Build a view company page
   1. Display all company details.
   2. Also display total subscriptions for that company. 
   2. Build a component that takes the company `numberOfEmployees` property and allows a user to increase/decrease that amount. When user is confident in the `numberOfEmployees` change and submits change, the component should be able to notify the page its included in with the new value. The view company page should update with new property value. This needs to be a component because we are going to use it on multiple pages.


