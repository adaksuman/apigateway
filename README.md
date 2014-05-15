apigateway
==========

API gateway for API service written with nginx and lua
API services need centralized API gateway to authentication and metrics before dispatching.APIgateway helps to monitor and authenticate once API service are registered with it.APIgateway is build using openresty(nginx) with lua module and redis. For all authentication and monitoring, redis can be used as data channel. Once  API is publishing with web based GUI or cli, all API rules will be published with redis. Ngnix would check rules before dispatching back-end API service. All API monitoring logs goes with redis ->logstash-> elasticsearch->kibana . Later kibana based dashboard will be used for visualization of API traffic or statistics. This approach might save a round trip with API gateway server for authentication and metrics collection.
