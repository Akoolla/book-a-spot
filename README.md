# Book-a-Spot
The goal of this application is to create a self contained event booking application that runs in a web browser.

Events could be things like a seat at a cinema screening, a theater show, a table at a local pre-loved goods sale event or a ticket to a local dance event.

The system should be able to take payments and where applicable print tickets, it would be nice if tickets could include a QR code that could be scanned at an event by a phone which could check validity, mark that ticket as entering the event and perhaps even prompt for payment where payment has not already been taken.

There will need to be some thing for administration of events, i.e. adding, deleting, cancelling bookings, emailing customers of changes to event they are booked in for. This will require a thinh for handling user accounts and restricted access to portions of the application.

## Technologies Chosen
The application will be written in Clojure and ClojureScript, where more complicated UI workflows exist, for instance on a booking page Reagent will be used to make a single page application in those instances.

The database is undecided, for the moment I'll stick with edn files, but in the future may switch to something more robust.

There will be an exposed rest service for returning lists such as events, some methods within the service will need to be secured, i.e list all bookings for an event and as such some security will need to be implemented for the service. OAuth2 seems like a good choice for this.

## Prerequisites
- Java
- You will need [Leiningen][ https://github.com/technomancy/leiningen] 2.0.0 or above installed.

## Current Status
- There is a simple page to allow a screening event to be persisted to a datastore (edn file)
- There is a simple page listing screenings that have been added
- There is a small bit of clojure-script to demonstrate that clojurescript is in place

## Development Plan
- Add figwheel into build - to speed up development of pages
- Be able to make a booking
- Be able to cancel a screening

## License
Copyright © 2018 Akoolla Digital Solutions
