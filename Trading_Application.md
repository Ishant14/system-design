### Design high throughput trading application? Application is hosted in NY and we have traders all over the world accessing this application.What things we need to take care on designing this application.

1) We should use high concurrent Atomic package instead of synchronisation.
2) We should use concrrent hashmap instead of hashtable.
3) Need to do proper garbage collection instead to prevent gc.
4) Since we are doing trading all over the world we may need to do currency conversion.
5) Proper load balancing 
6) Using kubernetes we can implement auto scaling in case needed .
7) We should follow rest architecture.
8) In case needed asynchronous operation using ActiveMQ.


