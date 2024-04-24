## Understanding publisher and message broker.

### a. How many data will your publisher program send to the message broker in one run?
The amount of data a publisher program sends to the message broker in one run depends on the implementation of the publisher. Typically, this is defined by either the number of messages the publisher is configured to send per run or the conditions under which it stops sending messages (like a set time limit or a predefined count of messages).

### b. The URL "amqp://guest:guest@localhost:5672" in the subscriber program
This URL is used for connecting to an AMQP message broker. In the context of both a publisher and a subscriber:
- `amqp://` is the scheme indicating the use of AMQP protocol.
- `guest:guest` is the default username and password used for authentication, often used in development environments.
- `localhost:5672` indicates that the message broker is running locally on the default AMQP port 5672.

If both publisher and subscriber use the same URL, it means they are connecting to the same message broker, which allows the subscriber to receive messages sent by the publisher.