var roi = /* color: #d63000 */ee.FeatureCollection(
        [ee.Feature(
            ee.Geometry.Point([91.79922369105515, 22.50875391240585]),
            {
              "system:index": "0"
            }),
        ee.Feature(
            ee.Geometry.Point([91.79963138682541, 22.51117230326509]),
            {
              "system:index": "1"
            }),
        ee.Feature(
            ee.Geometry.Point([91.80184152705368, 22.510617266480327]),
            {
              "system:index": "2"
            }),
        ee.Feature(
            ee.Geometry.Point([91.80267837626633, 22.511271416742176]),
            {
              "system:index": "3"
            }),
        ee.Feature(
            ee.Geometry.Point([91.8019702730864, 22.507405938485157]),
            {
              "system:index": "4"
            })]);

Map.centerObject(roi)
print(roi)

var addedProp = roi.map(function(ft){
  var geo = ft.geometry()
  var addedobj = ee.Feature(geo,{"class":"waterbody", "location":"hathazari"})
  return addedobj
})
print(addedProp)
