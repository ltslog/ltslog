# ltslog
Long Term Support version of a stripped down Log4j


ltslog is based on Log4j version 1.2.17.redhat.3.  As of 2021-01-12, it fixes all known security issues. 
In order to reduce the attackable surfaces, it removes features, that are not widely used.

Please report security issue via email to ltslog at arianne-project.org privatly. The Github issue trackker is public.

This is a long term support project. Security issues will be addressed in a timely manner. But there will be no new features. Please use a modern logging framework instead.

## Changes 1.2.19 - released on 2021-01-12

- [CVE-2020-9488](https://nvd.nist.gov/vuln/detail/CVE-2020-9488) - SMTPAppender now checks hostname of SSL certificate
- updated Maven dependencies of javax.mail to 1.6.2

## Changes 1.2.18 - released on 2021-12-16

- Minimum Java version is 8
- [CVE-2021-4104](https://nvd.nist.gov/vuln/detail/CVE-2021-4104): removed JMSAppender (which was vulnerable to an JNDI based exploit in the configuration - as hinted by in the Log4j2-issue)
- removed JDBCAppender
- [CVE-2017-5645](https://nvd.nist.gov/vuln/detail/CVE-2017-5645) and [CVE-2019-17571](https://nvd.nist.gov/vuln/detail/CVE-2019-17571): removed ServerSocket (which accepted log messages from other applications via a network connection)
- removed Chainsaw (a log viewer application)
- removed Log Factor 5 (a log viewer application)
