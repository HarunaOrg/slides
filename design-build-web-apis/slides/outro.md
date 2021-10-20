# Tools: python json.tool

Human-friendly JSON

```
{"project":"LOTOS2021","profiler":"iss1","profiles":[{"snrw":11.012911796569824,"wdir"
:24.575668334960938,"wspd":1.4364817142486572,"wvert":0.004620365798473358,"height":20
0.0,"time":1634665500.0,"humanTime":"2021-10-19T17:45:00.000+00:00"}...]}
```

`curl http://... | python -mjson.tool`

```
{
    "profiler": "iss1",
    "profiles": [
        {
            "height": 200.0,
            "humanTime": "2021-10-19T17:45:00.000+00:00",
            "snrw": 11.012911796569824,
            "time": 1634665500.0,
            "wdir": 24.575668334960938,
            "wspd": 1.4364817142486572,
            "wvert": 0.004620365798473358
        },
        ...
    ]
}
```

!SLIDE

# Tools: Apache Bench

Load testing and benchmarking

Apache Bench: `ab`


```
$ ab -n 100 -c 4 http://localhost:3000/projects

Connection Times (ms)
              min  mean[+/-sd] median   max
Connect:        0    0   0.1      0       1
Processing:    99  345  55.1    342     483
Waiting:       98  342  54.8    338     480
Total:         99  345  55.1    342     483
```

!SLIDE

# References

<!--<div style="font-size: 0.5em;">-->

<table><tbody><tr><td>

[Design and Build Great Web APIs](https://pragprog.com/titles/maapis/design-and-build-great-web-apis/)

[WebSequence Diagram editor](https://www.websequencediagrams.com/)

[OpenAPI Specification](https://swagger.io/specification/)

[Swagger UI](https://swagger.io/tools/swagger-ui/)

</td>
<td>

EOL ISF

[dv2-api docs](https://ncar.github.io/dv2-api/api/swagger-ui/)

[Profiler time-height-plot](http://datavis.eol.ucar.edu/time-height-plot/)

Tools

[Python `json.tool`](https://docs.python.org/3/library/json.html#module-json.tool)

[`ab` - Apache HTTP server benchmarking tool](https://httpd.apache.org/docs/2.4/programs/ab.html)

</td></tr></tbody></table>

<!--</div>-->

!SLIDE

# Discussion

- HTTP APIs developed or in consideration @ NCAR?
- Other tools & techniques for designing and building APIs?
- HTTP APIs in use?
- Experience w/ OPenDAP?