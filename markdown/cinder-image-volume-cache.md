## The Cinder image-volume cache

Note:
This feature is a bit obscure because it is especially useful in a
very specific scenario.

Consider this: as you already know, both Nova and Cinder support
Availability Zones, and they do play rather nicely with one
another. So you could have multiple physical locations, as shown here:


FIXME: insert diagram

Note:
Now there’s one thing in this diagram that *doesn’t* know about AZs,
and that’s Glance. Indeed, we currently have no way of dispersing
Glance across multiple locations, short of having multiple Glance API
endpoints and defining specific regions for them. So suppose this:


FIXME: insert diagram

Note:
Here, we have multiple geographical locations running our cloud. Each
has compute nodes and storage, but only one location, the main one,
has control nodes — and hence, can run Glance. But if an instance is
fired up in one of the remote locations, 
