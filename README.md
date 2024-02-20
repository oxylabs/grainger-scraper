# Grainger Scraper API

[![Oxylabs promo code](https://user-images.githubusercontent.com/129506779/250792357-8289e25e-9c36-4dc0-a5e2-2706db797bb5.png)](https://oxylabs.go2cloud.org/aff_c?offer_id=7&aff_id=877&url_id=112)

Oxylabs' [Grainger Scraper](https://oxylabs.io/products/scraper-api/ecommerce/grainger?utm_source=github&utm_medium=repositories&utm_campaign=product) is a data gathering solution allowing you to extract real-time information from an Grainger website effortlessly. This brief guide showcases how Grainger Scraper works, along with code examples to help you better understand how to use it hassle-free.

### How it works

You can get Grainger results by providing your own URLs to our service. We can return the HTML for any page you like.

#### Python code example

The example below illustrates how you can get HTML of Grainger page.

```python
import requests
from pprint import pprint

# Structure payload.
payload = {
    'source': 'universal_ecommerce',
    'url': 'https://www.grainger.com/category/electronics-batteries'
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
Find code examples for other programming languages [**here**](https://github.com/oxylabs/grainger-scraper/tree/main/code%20examples)

#### Output Example
```json
{
  "results": [
    {
      "content": "\n            <!doctype html>\n            <html lang=\"en\">\n              <head>\n                <meta ... </html>",
      "created_at": "2024-02-20 12:36:43",
      "updated_at": "2024-02-20 12:36:44",
      "page": 1,
      "url": "https://www.grainger.com/category/electronics-batteries",
      "job_id": "7165685703475501057",
      "status_code": 200
    }
  ]
}
```
With our Grainger Scraper, you can seamlessly pull essential public data from any Grainger web page. Gather crucial product details, like model numbers, specifications, or inventory levels, to keep your database updated and monitor the market trends efficiently. If you need any help or have queries, feel free to reach out to our dedicated support team via live chat or shoot an email to us at hello@oxylabs.io.