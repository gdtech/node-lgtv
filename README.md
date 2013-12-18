node-lgtv
=========

RESTful/JSON server using Node.JS for LG televisions that have serial port control

The server accepts commands using HTTP and a REST API (see below) and returns the result as a JSON or plain text response.

This version currently supports almost all serial port commands found in the TV user manual except channel changing by number.

Server configuration is done in the "config.json" file.  Make sure you adjust the configuration to suit your needs.

KNOWN ISSUES
============

        - the TV serial port can ocassionally lock up and TV needs a manual power reset (no way around this)
        - no support for setting channels using number input yet (working on it)

USAGE
=====

node ./node-lgtv


REST API
========

        /status
                - tv status request that returns the tv status in JSON only format
        /command?<command>=<value>
                - tv command request which returns a JSON or plain text result
                (the result type can be set in the config file)
