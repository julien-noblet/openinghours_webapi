# openinghours_webapi
Simple WebAPI that parse openinghours format 

    http://API-URL/?oh=Mo-Fr 10:00-20:00; PH off&now=2015-07-03 12:00:00 GMT+0100

Return 
```json
{
  "openinghours_webapi_version": 1,
  "parse":true,
  "query": {
    "oh": "Mo-Fr 10:00-20:00; PH off",
    "now": "2015-07-03 12:00 GMT+0100",
    "timezone": "GTM+1",
    "responseFormat": "json"
  },
  "errors": {},
  "open": true,
  "nextOpen" : "2d 22h 0m 0s",
  "nextClose" : "0d 8h 0m 0s"
}
```

Options
* ```now``` default: curent time in ```timezone``` 
* ```timezone``` default: GTM
* ```responseFormat``` default json (currently only json format is supported)


