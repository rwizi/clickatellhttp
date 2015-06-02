#ris.clickatellhttp

Python implementation of the Clickatell HTTP/HTTPS API for sending SMS messages using the Clickatell SMS Gateway as 
specified in v2.5.3 - https://www.clickatell.com/downloads/http/Clickatell_HTTP.pdf

This package enables you to easily integrate SMS messaging into your Python application.

##Installation

You can install this package via PIP

```bash
sudo pip install ris.clickatell
```

##Basic Usage

To use this package, you need to first register for a Developer Central account at https://www.clickatell.com. From the
Developer Central portal you will be provided with an API ID, username, and password which are required to use the 
client.

```python
from ris.clickatell import ClickatellClient, ClickatellException
 
# Clickatell settings
CLICKATELL_API_ID = 'XXXXXX'
CLICKATELL_USERNAME = 'username'
CLICKATELL_PASSWORD = 'password'
 
# Message details
message = 'Hello world!'
recipients = ['0000000000', '0000000000']
 
client = ClickatellClient(CLICKATELL_API_ID, CLICKATELL_USERNAME, CLICKATELL_PASSWORD)
client.send(message, recipients)
```
