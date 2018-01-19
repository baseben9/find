<html>

  <body>

   <h1>
   find
   </h1>
<h3>
a game about searching
</h3>

    <p id="demo"></p>

    <script>
      var x = document.getElementById("demo");
      function getLocation() {
        if (navigator.geolocation) {
          navigator.geolocation.getCurrentPosition(showPosition);
        } else {
          x.innerHTML = "Geolocation is not supported by this browser.";
        }
        }
        
      

      function showPosition(position) {
        var lat = position.coords.latitude;
        var lon = position.coords.longitude;
        var actlat = 0;
        var actlon = 0;
        var dist = Math.round((Math.abs(lat - actlat) + Math.abs(lon - actlon)) * 10000);
        x.innerHTML = "DISTANCE:" + dist; 
      }
setInterval(getLocation, 50)
    </script>

  </body>

</html>
