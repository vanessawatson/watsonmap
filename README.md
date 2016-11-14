# watsonmap
https://fusiontables.google.com/embedviz?q=select+col11%3E%3E1+from+1KDmamjXPzuNCcHMflASVu6Fejk_9ggfK7uVse9p4&viz=MAP&h=false&lat=36.96227582175109&lng=-79.1143745&t=1&z=7&l=col11%3E%3E1&y=2&tmplt=2&hml=KML
<iframe width="500" height="300" scrolling="no" frameborder="no" src="https://fusiontables.google.com/embedviz?q=select+col11%3E%3E1+from+1KDmamjXPzuNCcHMflASVu6Fejk_9ggfK7uVse9p4&amp;viz=MAP&amp;h=false&amp;lat=36.96227582175109&amp;lng=-79.1143745&amp;t=1&amp;z=7&amp;l=col11%3E%3E1&amp;y=2&amp;tmplt=2&amp;hml=KML"></iframe>

<!DOCTYPE html>
<html>
<head>
<meta name="viewport"></meta>
<title>Merge of McCroryDonations-bycity and cb_2015_37_place_500k - Google Fusion Tables</title>
<style type="text/css">
html, body, #googft-mapCanvas {
  height: 300px;
  margin: 0;
  padding: 0;
  width: 500px;
}
</style>

<script type="text/javascript" src="https://maps.google.com/maps/api/js?v=3"></script>

<script type="text/javascript">
  function initialize() {
    google.maps.visualRefresh = true;
    var isMobile = (navigator.userAgent.toLowerCase().indexOf('android') > -1) ||
      (navigator.userAgent.match(/(iPod|iPhone|iPad|BlackBerry|Windows Phone|iemobile)/));
    if (isMobile) {
      var viewport = document.querySelector("meta[name=viewport]");
      viewport.setAttribute('content', 'initial-scale=1.0, user-scalable=no');
    }
    var mapDiv = document.getElementById('googft-mapCanvas');
    mapDiv.style.width = isMobile ? '100%' : '500px';
    mapDiv.style.height = isMobile ? '100%' : '300px';
    var map = new google.maps.Map(mapDiv, {
      center: new google.maps.LatLng(36.96227582175109, -79.1143745),
      zoom: 7,
      mapTypeId: google.maps.MapTypeId.ROADMAP
    });
    map.controls[google.maps.ControlPosition.RIGHT_BOTTOM].push(document.getElementById('googft-legend-open'));
    map.controls[google.maps.ControlPosition.RIGHT_BOTTOM].push(document.getElementById('googft-legend'));

    layer = new google.maps.FusionTablesLayer({
      map: map,
      heatmap: { enabled: false },
      query: {
        select: "col11\x3e\x3e1",
        from: "1KDmamjXPzuNCcHMflASVu6Fejk_9ggfK7uVse9p4",
        where: ""
      },
      options: {
        styleId: 2,
        templateId: 2
      }
    });

    if (isMobile) {
      var legend = document.getElementById('googft-legend');
      var legendOpenButton = document.getElementById('googft-legend-open');
      var legendCloseButton = document.getElementById('googft-legend-close');
      legend.style.display = 'none';
      legendOpenButton.style.display = 'block';
      legendCloseButton.style.display = 'block';
      legendOpenButton.onclick = function() {
        legend.style.display = 'block';
        legendOpenButton.style.display = 'none';
      }
      legendCloseButton.onclick = function() {
        legend.style.display = 'none';
        legendOpenButton.style.display = 'block';
      }
    }
  }

  google.maps.event.addDomListener(window, 'load', initialize);
</script>
</head>

<body>
  <div id="googft-mapCanvas"></div>
</body>
</html>
