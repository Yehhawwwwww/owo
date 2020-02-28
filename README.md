<!doctype html>
<html>
  <head>
    <meta http-equiv="refresh" content="3;url="file:///D:\wwadfwafwafawf\www\yehaww\index.html"/>
    <title></title>
    <a href="Script.js" type="Javascript/text"/>
  </head>
  <body onload="init()">
<div id="main">
  <div id="updateMe">
    <h2></h2>
    <h1 id="guwiiFavouriteNumber"></h1>
  </div>
</div>
    <img src="Snip_Artwork.jpg" height="200" width="200"/>
    <p><iframe src="Snip.txt" frameborder="0" height="400"
        width="95%"></iframe></p>
  </body>
  <script type="text/javascript">
function refresh() {
  var req = new XMLHttpRequest();
  console.log("Grabbing Value");
  req.onreadystatechange = function () {
    if (req.readyState == 4 && req.status == 200) {
      document.getElementById('guwiiFavouriteNumber').innerText = req.responseText;
    }
  }
  req.open("GET", 'reload.txt', true); // Grabs whatever you've written in this file
  req.send(null);
}

function init() // This is the function the browser first runs when it's loaded.
{
  refresh() // Then runs the refresh function for the first time.
  var int = self.setInterval(function () {
    refresh()
  }, 10000); // Set the refresh() function to run every 10 seconds. [1 second would be 1000, and 1/10th of a second would be 100 etc.
}
</script>
</html>
