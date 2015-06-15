# Javascript Timer
Javascript Timer with the feature to keep running even if page refresh or browser close, 
also have start, pause, reset features.


[Demo](http://thebestcoders.com/javascript-timer)


**Dependencies:** This javascript plugin uses browser's cookies.

**Uses:**

```HTML
<!DOCTYPE html>
<html>
<head>
	<title>Javascript Timer - TheBestCoders</title>
	<script type="text/javascript" src="timer.js"></script>
</head>
<body>
  <div id="mytimer"></div>

  <button onclick="timer.start();">Start</button>
  <button onclick="timer.pause();">Pause</button>
  <button onclick="timer.reset();">Reset</button>

  <script type="text/javascript">
  window.onload = function()
  {
  	timer.init();
  }

  document.addEventListener('updateTimer', function(e){
  	document.getElementById('mytimer').innerHTML = e.detail.time;
  });
  </script>
</body>
</html>
```
