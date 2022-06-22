## Questions
**How long a tiny url would be ? Will it ever expire ?**

Assume once a url created it will remain forever in system.

**Can a customer create a tiny url of his/her choice or will it always be service generated? If user is allowed to create customer shortened links, what would be the maximum size of custom url?**

Yes user can create a tiny url of his/her choice. Assume maximum character limit to be 16.

**How many url shortening request expected per month ?**

Assume 100 million new URL shortenings per month

**Do we expect service to provide metrics like most visited links ?**

Yes. Service should also aggregate metrics like number of URL redirections per day and other analytics for targeted advertisements.


## Functional Requirements:

- Service should be able to create shortened url/links against a long url
- Click to the short URL should redirect the user to the original long URL
- Shortened link should be as small as possible
- Users can create custom url with maximum character limit of 16
- Service should collect metrics like most clicked links
- Once a shortened link is generated it should stay in system for lifetime

## Non-Functional Requirements:

- Service should be up and running all the time
- URL redirection should be fast and should not degrade at any point of time (Even during peak loads)
- Service should expose REST API’s so that it can be integrated with third party applications