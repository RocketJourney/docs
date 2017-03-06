---
title: Verifying Members
position: 1.1
---

#### RocketJourney Users need to verify they are Members of the Club they want to connect to in the RocketJourney App.

To be able to verify members, your software has to expose a web service with an endpoint URL accessible to RocketJourney, that accepts a POST request containing a JSON with a member's email address.

#### The web service will receive:

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
curl -X "POST" "http://www.globogym.com/verify" \
     -H "X-RJ-Token: 3f5554b5-13d6-40bd-b0c6-a0095b41b4ed" \
     -H "Content-Type: application/json" \
     -d $'{
  "email": "member@mail.com"
}'
~~~
{: title="Curl" }

#### And the web service should respond:

##### **If email does not exist in Club’s database:**

A `404` response.

##### **If email exist:**

A `200` response, with the following body:

~~~ json
{
  "id": "123456",
  "status": "active / inactive"
}
~~~

id
: *String*
: The web service should respond with the Member’s Unique ID linked to that email.

status
: *String*
: **"active"** if Member is able to pass the Club’s access control.
: **"inactive"** if Member is not able to pass the Club’s access control *(cancelled membership, stopped paying, or some other reason)*.

**About the Authorization Token:** We will be sending your Global Token inside a `X-RJ-Token` header, so you can validate that requests are sent from our systems, if you wish to do so.
{: .info }
