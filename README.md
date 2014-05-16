apigateway
==========


The API Gateway integrates, accelerates, governs, and secures Web API and SOA-based systems. For example, it can perform application networking by routing traffic based on content and sender, and by performing message content screening. The API Gateway applies policies to incoming messages by running message filters on requests.This project aims to deliver server side module call API gateway manager.It is build using openresty(nginx) with lua module and redis. For all authentication and authorization policies,redis will be used as a publisher to manager. Manager will check policies dispatching back-end API service. All API monitoring logs and metrices goes with redis ->logstash-> elasticsearch->kibana .kibana based dashboard will be used for visualization of API traffic or statistics. This approach might save a round trip with API gateway server for authentication and metrics collection.
