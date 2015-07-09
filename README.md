# 6ygolnik
<html xmlns="http://www.w3.org/1999/xhtml">
 <head>    
 <title>Асунсьон.</title>
<meta http-equiv="Content-Type" content="text/html; charset=utf-8"/>  
    <!--         Подключаем API карт 2.x
         Параметры:
        - load=package.full - полная сборка;
        - lang=ru-RU - язык русский.   
        -->
      <script src="http://api-maps.yandex.ru/2.0/?load=package.full&lang=ru-RU"
             type="text/javascript"></script>
     <script type="text/javascript"> 
        ymaps.ready(init);  
        function init() { 
            var myMap = new ymaps.Map('map', { 
                center: [-25.298, -57.622497], 
                zoom: 10           
 }),            
                 
 myPolygon = new ymaps.Polygon([[
           // Координаты вершин внешней границы шестиугольника.
			[-25.22321,-57.63346],
			[-25.21884,-57.53183],
			[-25.28409,-57.48300],
			[-25.35742,-57.53149],
			[-25.36055,-57.633465],
			[-25.29002,-57.68084]
                ]]);
  
            myMap.geoObjects.add(myPolygon)
                 .add(myPolygon); 
        }     </script> 
</head>  
<body> 
<h2>Добавление прямоугольника на карту</h2>  
<div id="map" style="width:600px;height:400px"></div>
</body>  
</html>
