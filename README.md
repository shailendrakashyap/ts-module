# to-smooth

[Chaikin's smoothing algorithm](http://www.idav.ucdavis.edu/education/CAGDNotes/Chaikins-Algorithm/Chaikins-Algorithm.html) for polylines of any dimensions.

### from
![image](https://user-images.githubusercontent.com/27716524/123362217-4e04e680-d5ab-11eb-842d-4fe9d586bbe1.png)

### to
![image](https://user-images.githubusercontent.com/27716524/123362234-51986d80-d5ab-11eb-95ec-f748cdb5f822.png)

# Usage
```js
import smooth from 'to-curve'
import geojson from 'geojson.json'


if (geojson.geometry.type === 'LineString')
  geojson.geometry.coordinates = smooth(geojson.geometry.coordinates)
else if (geojson.geometry.type === 'MultiLineString')
  geojson.geometry.coordinates = geojson.geometry.coordinates.map(points => smooth(points))
```

# Docs
export default function
`smooth(points, options: {iteration, factor} = {iteration: 1, factor: 0.75})`


### points
same dimension point array like LineString Coordinates

### options
- iteration
  - default - 1
  - iteration how many algorithm applied
- factor
  - default - 0.75
  - do not have to change or assign



here is [Example usage](https://openlayers.org/en/latest/examples/chaikin.html)



to-smooth is dimension generalized version of [chaikin-smooth](https://github.com/Jam3/chaikin-smooth)
you can use to-smooth instead of 2d only chaikin-smooth


## License

MIT
