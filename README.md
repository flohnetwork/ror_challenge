## Ruby On Rails Coding Challenge

We will design a simple rails app that exposes an API allowing patients to book appointments with doctors. We expect you to have models and rails migrations for the following entities only:
* Patient
* Doctor
* Appointment

Use your best judgement for the fields of each table, but you must ensure data integrity as far as possible using indexes (unique where necessary), foreign keys, constraints, etc

The app should expose 2 JSON endpoints:
1. List all available slots for a doctor in a given day (pagination not required)
2. Book an appointment on a free slot

For the above endpoints use your best judgements on the HTTP method and use query params as you deem suitable.

### Important Assumptions:

* Authentication mechanism is not required for the app
* Every doctor is working 24/7
* Slots can only be booked for exact duration of 1 hour starting at the hour mark. This means you cannot book an appointment for 07.30 - 10.00, or 10.00 - 10.15 hours. You can only book slots like 08.00 - 09.00 or 09.00 - 10.00
* No Patient can book the same slot with 2 different doctors
* No Doctor can be assigned the same slot with 2 different patients
* You are free to add rubygems as required

### We evaluate the code based on the following criteria:

* Strong database design and modelling
* Good REST API practices
* Good usage of model level constraints, validations, etc
* Good usage of Service objects where required
* Good coding practices, we follow https://github.com/rubocop-hq/ruby-style-guide as far as possible at Floh
* Test cases (rspec or other) for controller and model methods

### Bonus points for

* Additional Web Frontend to view and book slots
* Heroku deployable button in the README file (based on https://devcenter.heroku.com/articles/heroku-button)

### To get started:

* Fork this repo
* Add your changes/commits (the more the commits, the easier for us to review coding patterns)
* Create a pull request
