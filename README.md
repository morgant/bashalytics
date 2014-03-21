bashalytics
===========

by Morgan Aldridge <morgant@makkintosshu.com>

OVERVIEW
--------

A bash utility for fetching reports from Google Analytics using the Core Reporting v3 API. Also makes it easy to authenticate & save auth token.

_Currently under development._

TO-DO
-----

* Add command to list metrics & dimensions
* An option to override auth token (saving & reading) to support multiple accounts
* Is there a way to look up & list Profile IDs?

ACKNOWLEDGEMENTS
----------------

Original concept based on [this blog post by Adam Buchanan](http://adambuchanan.me/post/19993272813/google-analytics-api-bash-scripts). Uses Google's [Core Reporting API (v3)](https://developers.google.com/analytics/devguides/reporting/core/v3/) and [Metadata API (v3)](https://developers.google.com/analytics/devguides/reporting/metadata/v3/) to fetch Google Analytics metrics, dimensions, and reports data, plus [Dominic Tarr's `JSON.sh`](https://github.com/dominictarr/JSON.sh) to parse JSON results.

LICENSE
-------

Copyright (c) 2014, Morgan Aldridge. All rights reserved.

_TBD_
