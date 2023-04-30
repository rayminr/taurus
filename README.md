# Taurus 

Quick links: [Taurus Documentation](http://gettaurus.org/docs/) | [Knowledge Base](http://gettaurus.org/kb/) | [Support Forum](https://groups.google.com/forum/#!forum/codename-taurus)

## Purpose
Hides the complexity of performance and functional tests with an automation-friendly convenience wrapper. Taurus relies on JMeter, Gatling, Locust.io, and Selenium WebDriver as its underlying tools. Free and open source under Apache 2.0 License.


## Installation or Upgrade

Just install it using PyPi:

```bash
pip install bzt
```

More detailed instructions for Linux, Mac OS and Windows available [here](http://gettaurus.org/docs/Installation.md).

## Getting Started

Create a file named `test.yml` with following contents:

```yaml
---
execution:
- concurrency: 10
  ramp-up: 1m
  hold-for: 1m30s
  scenario: simple
  
scenarios:
  simple:
    think-time: 0.75
    requests:
    - http://blazedemo.com/
    - http://blazedemo.com/vacation.html
```

Then run `bzt test.yml`. After the tool finishes, observe resulting summary stats in console log (more reporting options [here](http://gettaurus.org/docs/Reporting.md)). All artifact files from the run will be placed in the directory mentioned in console log. Read more on command-line tool usage [here](http://gettaurus.org/docs/CommandLine.md).

![Analytics](https://ga-beacon.appspot.com/UA-63369152-1/taurus/readme)


配置report
https://a.blazemeter.com上注册一个用户，到下面的页面产生自己的API Key Id和API Key Secret
https://a.blazemeter.com/app/#/settings/api-keys
$ curl https://a.blazemeter.com/api/v4/user --user '741b76d7794fac6eaecf8330:4e63d0732f654fac5eef8b3617af0b325d8f751ff86fa6a8d28fca5b250f2abb7803a301'

参照以下配置：
https://gettaurus.org/docs/BlazemeterReporter/
