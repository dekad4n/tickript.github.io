# Connection to Backend
Connection to backend is handled with classes we call Services.
Every [Route](/Workflows/Backend/Routes/) of backend has its own Service in the mobile part. The corresponding services basically handles get, put, post requests with function that returns Future values of specific type or a dynamic type. 

The services are very estimatable. However, since some constraints, we did not use any **form data** to handle data from services. Instead, in services we use Map<String, dynamic> (commonly Map<String, String>) to send data with Post requests.

We used the built-in libraries of Flutter to handle JSON data or Requests.