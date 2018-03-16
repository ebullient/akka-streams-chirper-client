# Akk Streams Chirper Client

This is a demonstration project that introduces some of the features of
[Akka Streams](https://doc.akka.io/docs/akka/current/stream/index.html?language=java)
and [Akka HTTP](https://doc.akka.io/docs/akka-http/current/index.html?language=java).

The project contains two runnable source files, `ChirperClientSimulator` and `ChirperWebSocketExamples`.
`ChirperClientSimulator` simulates the activities of a Chirper application client.
`ChirperWebSocketExamples` implements a few examples of accessing streams via WebSockets.

This project requires that the Chirper application is running in the background when you run either
`ChirperClientSimulator` or `ChirperWebSocketExamples`.
The Chirper application is a chat app. Users can register with the app, add friends to their network,
and create chirps - chat messages.

## Installation

Clone this project and the Chirper project.
~~~~
git clone https://github.com/lagom/lagom-java-chirper-example.git
git clone https://github.com/mckeeh3/akka-streams-chirper-client.git
~~~~

Run the Chirper application.
~~~~
cd lagom-java-chirper-example
mvn lagom:runAll
~~~~

Once the Chirper application is running run the `ChirperClientSimulator`.
~~~~
cd akka-streams-chirper-client
mvn exec:java@producer
~~~~
This will create some Chirper users, add some friends to each user, and then it will create a continous series of random user chirps.
