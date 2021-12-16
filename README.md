# ltslog
Long Term Support version of a stripped down Log4j


ltslog is based on Log4j version 1.2.17.redhat.3.  As of 2021-12-16, it fixes all known security issues. 
In order to reduce the attackable surfaces, it removes features, that are not widely used.


## Changes 1.2.18 - released on 2021-12-16

- Minimum Java version is 8
- removed JMSAppender (which was vulnerable to an JNDI based exploit in the configuration - as hinted by in the Log4j2-issue)
- removed JDBCAppender
- removed ServerSocket (which accepted log messages from other applications via a network connection)
- removed Chainsaw (a log viewer application)
- removed Log Factor 5 (a log viewer application)
