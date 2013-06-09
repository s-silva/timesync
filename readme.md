#Timesync

Facebook like time display ('a minute ago' etc.) with (UTC) unix timestamps. Including
automatic synchronization with user's time zone.

##Usage

The time elements should be presented in the HTML as:


<abbr class="synctime" data-mode='0' data-ts='1326256773'></abbr>

Where 'data-ts' is the unix timestamp of the UTC time of the event, and 'data-mode' is
the display mode. Which can be either 0, 1, or 2.

In order for these to appear as relative times or to refresh them, you need to call:

For the complete page:


synctime_set();


##Future Development


1. Real-time updating timestamps for most recent events, such as: '2 seconds ago.' need
   to be updated every few seconds/minutes where '2 hours ago' may not need to be updated
   at all.

2. Refresh/set time values of children of a certain element, not the whole document.