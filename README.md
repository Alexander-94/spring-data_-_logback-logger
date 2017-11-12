# spring-data_and_logback-logger

Spring data and logback logger example.

>**Project provides logging using two loggers: root(ERROR) and second logger(INFO)**

If class for logging is specified (``` LoggerFactory.getLogger(WatchClient.class) ```), then root logger will be connected.
If name of logger is explicitly specified &nbsp;&nbsp;&nbsp;&nbsp;(``` LoggerFactory.getLogger("INFOlogger") ```), then both loggers(INFO and root) will be working.

>**Structure:**
  - WatchClient &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;- uses LoggerFactory.getLogger(WatchClient.class) - root logger
  
  - WatchListController&nbsp;&nbsp;&nbsp;&nbsp;- uses LoggerFactory.getLogger(WatchListController.class) - root logger
 
  - WatchService&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;- uses LoggerFactory.getLogger(WatchService.class) - root logger
  
  - WatchController&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;- uses LoggerFactory.getLogger("INFOLogger") - INFO logger + root logger
