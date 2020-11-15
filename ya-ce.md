```
$ ab -n 400 http://localhost:8080/1.php
This is ApacheBench, Version 2.3 <$Revision: 1843412 $>
Copyright 1996 Adam Twiss, Zeus Technology Ltd, http://www.zeustech.net/
Licensed to The Apache Software Foundation, http://www.apache.org/

Benchmarking localhost (be patient)

Test aborted after 10 failures

apr_socket_connect(): Invalid argument (22)
$ ab -c 100 -n 200 http://127.0.0.1:8080/1.php
This is ApacheBench, Version 2.3 <$Revision: 1843412 $>
Copyright 1996 Adam Twiss, Zeus Technology Ltd, http://www.zeustech.net/
Licensed to The Apache Software Foundation, http://www.apache.org/

Benchmarking 127.0.0.1 (be patient)
Completed 100 requests
Completed 200 requests
Finished 200 requests


Server Software:        nginx/1.19.4
Server Hostname:        127.0.0.1
Server Port:            8080

Document Path:          /1.php
Document Length:        15 bytes

Concurrency Level:      100
Time taken for tests:   0.056 seconds
Complete requests:      200
Failed requests:        0
Total transferred:      35600 bytes
HTML transferred:       3000 bytes
Requests per second:    3542.02 [#/sec] (mean)
Time per request:       28.233 [ms] (mean)
Time per request:       0.282 [ms] (mean, across all concurrent requests)
Transfer rate:          615.70 [Kbytes/sec] received

Connection Times (ms)
              min  mean[+/-sd] median   max
Connect:        0    1   1.2      1       4
Processing:     3   21   6.7     23      32
Waiting:        1   20   6.8     23      32
Total:          5   22   5.8     24      34

Percentage of the requests served within a certain time (ms)
  50%     24
  66%     25
  75%     26
  80%     26
  90%     28
  95%     29
  98%     30
  99%     32
 100%     34 (longest request)
```



