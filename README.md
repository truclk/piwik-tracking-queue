piwik-tracking-queue
====================

Piwik need a layer to keep tracking data in queue. So that if the database or server is overload. It won't affect to the statistics (by losing data)

Problem

Piwik depends on piwik.php api for tracking. These requests will be directly go to database. If there are lots of traffic and the database can't handle all of this and we might face with traffic losing.

To deal with this stituation. An additional queue was used to store Tracking data. Redis is a good choice
