# Tracking Travel

## Summary

Project that was born with the purpose to study the concept and also to implement a Service Mesh with Sidecar. The business part is super simple, I have a service that reads a file in X format and generates a message to send to a queue that has a consumer listening and taking the data to keep in a database to carry out queries by document, name of the customer or card number.

## Flow to loader the file

Basically a Job is triggered by a scheduling tool (I haven't chosen yet) that will read a file from a server (in this case, a directory on the machine) and do a loading process, these data already registered will be saved in a database. The data model will still be defined and the bank that will treat the information as Log.

![Flow](https://github.com/ander-f-silva/tracking-travel/blob/master/flow_tracking_travel_1.png)

## Architecture design

The applications will be docker images running on Kubernates, but design represents a solution that could run on traditional infrastructure, this image will be improved in the future.

![Architecture](https://github.com/ander-f-silva/tracking-travel/blob/master/architecture.png)
