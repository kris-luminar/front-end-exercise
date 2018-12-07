# Front End Technical Exercise

As part of your interview, we request that you complete a technical exercise. We'll
work with you to determine a good time frame to take this on.

### Instructions

- Complete the problem in the technology of your choosing
  - It must result in a web page that we can run by compiling/running the code on
    our computers (it does not need to be on a public URL)
  - You must use the Masspay.js library that we have provided
  - There is no requirement for you to implement a server side component
- Please upload your solution to your personal Github account, with a new `README.md` file
- Implement a test runner of your choice and provide us instructions on use to show your tests pass

### Your solution will be evaluated on:
- Completeness (does it work?)
- Quality of all code

### Questions
Send any questions to liz@dwolla.com

## What is the end result supposed to do?

Masspay is a feature of Dwolla that helps businesses send payouts to many different
people at one time. Let's imagine you are building a new UI for masspays that
allows a user to enter a list of email addresses belonging to people they'd like
to send funds to, as well as the amount they'd like to send. After the user
enters the list, they can then submit it to Dwolla for processing.

## Mockups

Three different mockup images have been provided in the mocks folder. Some
specific details are provided below so you don't have to guess. Your design
should be responsive.

Please implement these user stories:
- As a user, when I click the plus button another row should be added
- As a user, when I click the "Submit" button my masspay should be processed
  by the `submit()` function of Masspay.js

You do not need to handle removing rows. User authentication and/or the logout
button do not need to be implemented.

## Fonts

The fonts used for this design are one weight of Poppins and two weights of Roboto.
These have already been included for you from Google Fonts in the head tag.

## Colors

orange:
#e98453

pink:
#b45277

purple:
#5e4e76

dark gray:
#8393aa

gray:
#c9d3e0

light gray:
#f4f7fb

white:
#fff

nav bar gradient:
90 degree gradient from orange to pink, as defined above

card shadow:
0 0 2px 0 rgba(53, 65, 83, 0.12), 0 2px 4px 0 rgba(53, 65, 83, 0.12)

## Masspay.js

We have provided a JavaScript file for you that will simulate interacting with a
server in this exercise. It also optionally provides some helper functions that
you may choose to use if you'd like. You should be able to pull this file into
your code using CommonJS (Node), AMD, or in the browser. If you think there is a
bug in this file, please work with us to resolve.

### getKnownReceivers()
Returns a Promise that contains an array of email addresses that are allowed to
receive money from the user.

### isKnownReceiver(email)
Returns a Promise that contains `true` if the user is allowed to send to the
email address provided.

### isEmailAddress(email)
Returns `true` if the email address provided is considered to be valid according
to business rules.

### isValidReceiver(email)
Returns a Promise that contains `true` if the user is allowed to send to the
email address provided.

### isValidAmount(amount)
Returns `true` if the amount is valid according to business rules.

### submit(items)
This function simulates submitting a masspay to a backend server. It takes in
an array of masspay items and returns a Promise that contains a result object.

*items example:*
```
[
  {
    receiver: 'juliana@test.com',
    amount: 1
  },
  {
    receiver: 'kendrick@test.com',
    amount: 42.42
  }
]
```

*response example:*
```
{
  success: false,
  error: 'invalidAmount'
  item: 1
}
```

The item property is zero indexed.

*potential error messages:*
- `empty`
- `invalidReceiver`
- `invalidAmount`
- `unknown`
