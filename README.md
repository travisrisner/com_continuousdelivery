# Continuous Delivery Component

This component allows you to deploy packages from various sources to your Joomla! installation.

## System Requirements

Joomla! Version: 5 or 6
Minimum PHP version: 8.0
Recommended PHP version: 8.3

## Installation

Click `Clone or download` > `Download ZIP` and then upload the archive 
to your Joomla site.

## Usage

You can install a package by running the follow command:

```bash
curl --form 'deployKey=DEPLOY_KEY_HERE' --form 'package=@/path/to/file' \
  https://example.org/index.php?option=com_continuousdelivery
```

The deploy key can be found in the Global Configuration section of 
Joomla after this component is installed.

The installation process should return a JSON encoded object as a 
response. This object will contain an `error` key (string) on failure or 
a `success` key (bool) on success.
