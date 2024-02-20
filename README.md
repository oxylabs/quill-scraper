# Quill Scraper API

[![Oxylabs promo code](https://user-images.githubusercontent.com/129506779/250792357-8289e25e-9c36-4dc0-a5e2-2706db797bb5.png)](https://oxylabs.go2cloud.org/aff_c?offer_id=7&aff_id=877&url_id=112)

Oxylabs' [Quill Scraper](https://oxylabs.io/products/scraper-api/ecommerce/quill?utm_source=github&utm_medium=repositories&utm_campaign=product) is a data gathering solution allowing you to extract real-time information from an Quill website effortlessly. This brief guide showcases how Quill Scraper works, along with code examples to help you better understand how to use it hassle-free.

### How it works

You can get Quill results by providing your own URLs to our service. We can return the HTML for any page you like.

#### Python code example

The example below illustrates how you can get HTML of Quill page.

```python
import requests
from pprint import pprint

# Structure payload.
payload = {
    'source': 'universal_ecommerce',
    'url': 'https://www.quill.com/office-desks/cbl/22137.html'
}

# Get response.
response = requests.request(
    'POST',
    'https://realtime.oxylabs.io/v1/queries',
    auth=('user', 'pass1'),
    json=payload,
)

# Instead of response with job status and results url, this will return the
# JSON response with the result.
pprint(response.json())
```
Find code examples for other programming languages [**here**](https://github.com/oxylabs/quill-scraper/tree/main/code%20examples)

#### Output Example
```json
{
  "results": [
    {
      "content": "\r\n\r\n\r\n<!DOCTYPE html>\r\n<html lang=\"en\">\r\n<head>\r\n    <meta name=\"viewport\" content=\"width=device-wid ... </html>",
      "created_at": "2024-02-20 12:57:02",
      "updated_at": "2024-02-20 12:57:05",
      "page": 1,
      "url": "https://www.quill.com/office-desks/cbl/22137.html",
      "job_id": "7165690816554353665",
      "status_code": 200
    }
  ]
}
```
With our Quill Scraper, you can efficiently extract public data from any Quill document. Gather the necessary text-based information, like themes, key points, or facts, to stay informed and ahead of your peers. If you require any assistance, feel free to reach our support team via live chat or email us at hello@oxylabs.io.