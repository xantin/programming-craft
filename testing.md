# testing

## traffic (load) test

#### types

* Repetitive load generation
* Simulated traffic patterns
* Real traffic

#### Before running test good to know

* Average throughput in requests per second
* Peak throughput (What is the most traffic that you get over a certain period?)
* Throughput distribution by API endpoint (Do you have any endpoint that gets substantially more traffic than any others?)
* Throughput distribution by users (A few generate most traffic, or is it more evenly distributed?)

## Tools for testing

* https://github.com/tsenart/vegeta

sources:

* [how-to-load-test-and-tune-performance-on-your-api-part-i](https://www.3scale.net/2015/04/how-to-load-test-and-tune-performance-on-your-api-part-i/)
