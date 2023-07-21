### Day11 - Cloud Integrations

- There are two pattens of application communication
  - Synchronous -> application to application
  - Asynchronous (or event-based) -> application to queue to application
- Synchronous patterns can be problematic when there is a heavy load on the application. In that case, it's best to decouple the applications from talking to one another in order to streamline communication

##### Amazon Simple Queue Service (SQS)
- One of the first services by AWS.
- Fully managed service used to decouple applications.
- Producers send a message to the an SQS queue, where it's distributed to many consumers.
- Messages are deleted after they're read by consumers.
- Allows for both applications to scale independently.
- SQS follows the FIFO rule (first in first out).

##### Amazon Kinesis
- Used for real-time big data streaming.
- It is a managed service.

##### Amazon Simple Notification Service (SNS)
- Implements a Pub/Sub architecture where the message is sent to an SNS Topic which is smart enough to send it to as many receivers.
- In this model, there is an "event publisher" who sends the message to an SNS topic. There's also many "event subscribers" who listen to the SNS topic notifications.
- Each subscriber will get all the messages.
- Subscribers can be SQS, Lambda, and Kinesis Data Firehose. We can also send emails, SMS, and HTTP endpoints.

##### Amazon MQ
- This is a way to use traditional open protocols such as MQTT, AMQP, etc.. on the cloud.
- It is a managed message broker service for RabbitMQ and ActiveMQ.
- Doesn't "scale" as much as SQS.
- Comes with a queue feature and topic features.

##### Summary
- SQS:
  - queue service in AWS
  - messages are kept up to 14 days
  - multiple producers and multiple consumers.
  - used to decouple applications in AWS.
  - receivers have to pull the messages from the queue to process them and delete them from the queue

- SNS:
  - notification service in AWS
  - no message retention
  - multiple subscribers which can receive the same message from an SNS topic.

- Kineses: real-time big data processing
- Amazon MQ: managed broker service for ActiveMQ and RabbitMQ.

