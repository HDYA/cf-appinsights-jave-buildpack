# Application Insights Java Buildpack

A script-based command-line tool instrumenting maven / gradle applications with Application Insights.

## Overview

This project implements a script-based buildpack to perform the instrumentation of Application Insights for maven or gradle applications.

Scripts other than `bin/supply` contains no actual content and are supposed to be ignored.

Detailed manual steps can be found in document [here](https://docs.microsoft.com/en-us/azure/application-insights/app-insights-java-get-started).

## Usage

As key features are all bundled in script `bin/supply`, this project shall be used with command:

```bash
    /path/to/this/project/bin/supply /path/to/this/project /path/to/source/code/to/instrument
```

As introduced in the document mentioned earlier, this script will automatically detect maven / gradle dependencies files, insert dependencies for Application Insights, add configuration files for Application Insights and class of interceptor.
