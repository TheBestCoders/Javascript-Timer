# Javascript Timer
Javascript Timer with the feature to keep running even if page refresh or browser close, 
also have start, pause, reset features.


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
  <button onclick="setTime();">Set Time</button>

  <script type="text/javascript">
  window.onload = function()
  {
  	timer.init();
  }

  document.addEventListener('updateTimer', function(e){
  	document.getElementById('mytimer').innerHTML = e.detail.time;
  });

  function setTime()
  {
    var t = parseInt(prompt("Enter time in seconds to start.", 0));
    if(!isNaN(t))
      timer.setStartTime(t);
    else
      alert("Enter only numeric digits");
  }
  </script>
</body>
</html>
```
