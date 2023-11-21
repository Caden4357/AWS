# Introduction:
    - When deploying multiple applications they will inevitably need to communicate with each other 
    - there are 2 patterns to application communication: 1.) synchronous commumication (app to app) 2.) async or event based (app to que to app)
# SQS simple que service 
    - producers send messages to a que consumers will poll messages from the que when they are done with the task the task will be deleted from the que 
    - fully managed (serverless) used to DECOUPLE applications
    - scales 
    - default retention of messages: 4 days with a maximum of 14 days
    - no limit to # of messages messages are deleted after theyre read by consumers 
    - low latency 
    - scales horizontally
    - messages can be ordered with FIFO model (first in first out)
# Amazon Kinesis:
    - For exam all you need to know is Kinesis = real time big data streaming
## Beyond that for Kinesis 
    - Managed service to collect, process and analyze real time streaming data at any scale
    - More in Slides from lecture 253
# SNS: simple notification service 
    - If you want to send one message to many receivers use this 
    - it uses whats called a pub/sub to automatically do this will even send to a Que 
