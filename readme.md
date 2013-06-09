#Timesync

Facebook like time display ('a minute ago' etc.) with (UTC) unix timestamps. Including
automatic synchronization with user's time zone.

##Usage

The time elements should be presented in the HTML as:

```html
<abbr class="synctime" data-mode='0' data-ts='1326256773'></abbr>
```

Where 'data-ts' is the unix timestamp of the UTC time of the event, and 'data-mode' is
the display mode. Which can be either 0, 1, or 2.

In order for these to appear as relative times or to refresh them, you need to call:

For the complete page:

```javascript
synctime_set();
```


##Example

A page which gets updated on loading.

```html

<html><head>

	<title>Time Sync</title>
	<script type="text/javascript" src="timesync.js"></script>

</head><body onload="javascript: synctime_set();">

	<p><abbr class="synctime" data-mode='0' data-ts='1326256773'></abbr></p>
	<p><abbr class="synctime" data-mode='1' data-ts='1324546623'></abbr></p>
	<p><abbr class="synctime" data-mode='2' data-ts='1324624773'></abbr></p>
	<p><abbr class="synctime" data-mode='0' data-ts='1319206773'></abbr></p>
	<p><abbr class="synctime" data-mode='1' data-ts='1321637773'></abbr></p>
	<p><abbr class="synctime" data-mode='2' data-ts='1313646473'></abbr></p>

</body></html>

```



##Future Development


1. Real-time updating timestamps for most recent events, such as: '2 seconds ago.' need
   to be updated every few seconds/minutes where '2 hours ago' may not need to be updated
   at all.

2. Refresh/set time values of children of a certain element, not the whole document.