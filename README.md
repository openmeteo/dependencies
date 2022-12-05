# dependencies
A chart with the dependencies between software pieces of openmeteo

```mermaid
graph TD;
enhydris-autoprocess-->haggregate
enhydris-autoprocess-->rocc
enhydris-autoprocess-->enhydris

enhydris-synoptic-->rocc
enhydris-synoptic-->enhydris
enhydris-openhi-gis-->enhydris


enhydris-->htimeseries

rocc-->htimeseries
haggregate-->htimeseries
enhydris-api-client-.->enhydris
enhydris-api-client-->htimeseries
loggertodb-->enhydris-api-client

hspatial-->htimeseries
evaporation-->hspatial
enhydris-cache-->enhydris-api-client

aira-->hspatial
aira-->swb
```

## Legend
```mermaid
graph TD;
A-->|Direct dependency|B
C-.->|Dependency via API|D
```
