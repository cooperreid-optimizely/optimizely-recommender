# Optimizely Recommender Wrapper

> Wrapper for Optimizely recommendation API

E.g. - Attempt to display 15 total recommendations // Load 10 Co-browse recommendations as primary // Backfill with popular recommendations
```
 RecService.init({serviceId: 8425370334, log: true})
  .addRecommender({max: 10, id: 8420784679, type: 'cobrowse', target:'ST100478'})    
  .addRecommender({max: 15, id: 8415788430, type: 'popular'})    
  .run({max: 15})
  .then(function(recs) {
    console.log(recs);
    // render the recs in the extension/webpage
  });
```

---

> Create a new Recommender Service

``` RecService.init({serviceId: 123456789, log: true})```

### init
```
.find({Object} config)
```
Returns a ```RecService``` instance

##### config parameters:

| parameter | type   | details                                            | required | default |
|-----------|--------|----------------------------------------------------|----------|---------|
| serviceId       | integer | The recommender service ID configured in Optimizely | yes      |     undefined    |
| log      | boolean  | Will log debug messages to the console                      | no      |    false    |

