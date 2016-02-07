# Creating Redirects

> This guide explains how to set up server redirects for specific endpoints.  These can be useful when migrating from another service or creating non-canonical aliases for other endpoints.

Redirects require two things with a third option.  

First, they require a requested endpoint.  This endpoing cannot be the same as an existing stream endpoint.  For example, if you have an Events stream with an /events endpoint, adding a redirect will always resolve to your /events endpoint.  Redirects only come into play upon error. 

Next, they require a destination.  Let's say you add /eventz and wish to route it - the second option would be /events

Finally, you may add a query parameter mapping, whch allows you to translate requested parameters to others.