---
title: UI Examples
position: 1
description: Some description below the title mothefucka
---

Note tips:

You'll succeed if you do this.
{: .success }

Here's some useful information.
{: .info }

Something may not happen if you try and do this.
{: .warning }

Something bad will happen if you do this.
{: .error }

Table:

| Code | Name        | Description                      |
|------|-------------|----------------------------------|
| 200  | OK          | Success                          |
| 201  | Created     | Creation Successful              |
| 400  | Bad Request | We could not process that action |
| 403  | Forbidden   | We couldn't authenticate you     |

Code Block:

~~~ json
{
  "error": true,
  "message": "error message here"
}
~~~
{: title="JSON"}

~~~ javascript
$.get("http://api.myapp.com/books/", { "token": "YOUR_APP_KEY"}, function(data) {
  alert(data);
});
~~~
{: title="jQuery" }

~~~ python
r = requests.get("http://api.myapp.com/books/", token="YOUR_APP_KEY")
print r.text
~~~
{: title="Python" }

~~~ javascript
var request = require("request");
request("http://api.myapp.com/books?token=YOUR_APP_KEY", function (error, response, body) {
  if (!error && response.statusCode == 200) {
    console.log(body);
  }
});
~~~
{: title="Node.js" }

~~~ bash
curl http://sampleapi.readme.com/orders?key=YOUR_APP_KEY
~~~
{: title="Curl" }

parameter1
: Theres no title in this mothafucka

paramter2
: what about putting a lot lot lot lot lot lot lot lot lot lot lot lot lot lot lot lot lot lot lot lot lot of text here.
