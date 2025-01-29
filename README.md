# ddostest

Welcome to DOS Test!

This is a simple CLI tool to generate traffic to aid in testing a WAF's DDOS technologies.
It uses Selenium stealth to bypass WAF bot rules and requires the user to have a valid google driver.

usage: ddosTest [-h] [-rH RHOST] [-i] [-r] [-aP ALTPATH] [-t TITLE] [-T TIME] [-L LOG]

Tool for generating traffic to test WAF DDoS settings.

options:
  -h, --help                                            show this help message and exit
  -rH RHOST, --rHost RHOST                              RHost - Website domain to test.
  -i, --intense                                         Trigger an Intense test - 1 hour of regular requests. Simulates DoS
  -r, --regular                                         Trigger a slower amount of traffic simulating a standard user
  -aP ALTPATH, --altPath ALTPATH                        For when default path of Chromedriver is insufficient. Use this if your driver isn't in the Python environment or isn't located at /usr/bin/google-chrome.
  -t TITLE, --title TITLE                               Insert a title string to match against
  -T TIME, --Time TIME                                  Enter the amount of time you'd like regular checks to run for in minutes. Defaults to 240 minutes
  -L LOG, --Log LOG                                     Enter absolute path and name for log file. Default is ddostest.log in your working directory.


TODO:
* Add variable to alter sleep time between requests for regular scans
* Add multi-threaded support
