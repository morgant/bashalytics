bashalytics
===========

by Morgan Aldridge <morgant@makkintosshu.com>

OVERVIEW
--------

A bash utility for fetching reports from Google Analytics using the Core Reporting v3 API. Also makes it easy to authenticate & cache an auth token as well as fetching & caching the list of dimensions & metrics.

_While functional, this tool is currently under early development._

	INSTALLATION
------------

Running the following command will install both bashalytics and the required JSON.sh in /usr/local/bin/:

	./install

USAGE
-----

First, authenticate to Google Analytics (this will store an auth token in ~/.bashalytics/auth_token):

    bashalytics auth

You can run reports as follows (specifying the profile ID, followed by the start & end dates, followed by a list of dimensions & metrics):

    bashalytics report <profile_id> 2014-01-01 2014-01-10 ga:visits

It will output the report in TSV (tab separated values) format, with the first row specifying the column names as the dimensions & metrics that were specified, and the following row(s) containing the respective values. (Note: dimensions and metrics are fetched and cached locally once per day when running reports.)

Naturally, you can get further usage instructions as follows:

    bashalytics -h

TO-DO
-----

* An option to override auth token (saving & reading) to support multiple accounts
* Is there a way to look up & list Profile IDs?

ACKNOWLEDGEMENTS
----------------

Original concept based on [this blog post by Adam Buchanan](http://adambuchanan.me/post/19993272813/google-analytics-api-bash-scripts). Uses Google's [Core Reporting API (v3)](https://developers.google.com/analytics/devguides/reporting/core/v3/) and [Metadata API (v3)](https://developers.google.com/analytics/devguides/reporting/metadata/v3/) to fetch Google Analytics metrics, dimensions, and reports data, plus [Dominic Tarr's `JSON.sh`](https://github.com/dominictarr/JSON.sh) to parse JSON results.

LICENSE
-------

Copyright (c) 2014-2015, Morgan Aldridge. All rights reserved.

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the "Software"), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.
