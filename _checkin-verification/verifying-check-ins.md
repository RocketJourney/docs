---
title: Veryfing Check-Ins
position: 1.1
---

#### To verify Check-Ins, your software has to send **Check-In** information to RocketJourney in real time as Members check in at the Club.

A POST request has to be sent to `rocketjourney.com/api/v1/check` with the following information:

~~~ http
POST /check HTTP/1.1
Content-Type: application/json
X-RJ-Token: 3f5554b5-13d6-40bd-b0c6-a0095b41b4ed

{
  "member_id": "541",
  "location_id": "44",
  "check_in_date": "1488423886"
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
