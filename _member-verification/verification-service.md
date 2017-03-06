---
title: Verification Service
type: post
position: 1.2
---

To be able to verify members, your software has to expose a web service with an endpoint URL accessible to RocketJourney, that accepts a POST request containing a JSON with a member's email address.

**About the Authorization Token:** We will be sending your Global Token inside a `X-RJ-Token` header, so you can validate that requests are sent from our systems, if you wish to do so.
{: .info }

~~~ http
POST /verify HTTP/1.1
Content-Type: application/json
X-RJ-Token: 3f5554b5-13d6-40bd-b0c6-a0095b41b4ed

{
  "email": "fitness.user@gmail.com"
}
~~~
{: title="HTTP" }

~~~ bash
curl -X "POST" "http://www.awsomegym.com/verify" \
     -H "X-RJ-Token: 3f5554b5-13d6-40bd-b0c6-a0095b41b4ed" \
     -H "Content-Type: application/json" \
     -d $'{
  "email": "member@mail.com"
}'
~~~
{: title="Curl" }
