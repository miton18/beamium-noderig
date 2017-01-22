# Monitoring stack

Contains 2 components :
- [Noderig][noderig]
- [Beamium][beamium]

# Setup

Replace 3 parameters in `docker-compose.yaml` :
- hostname
- warp10_endpoint (Ex: https://warp.domain.tld)
- warp10_token

# Start

```
$ docker-compose up -d
```

[noderig]:https://github.com/runabove/noderig
[beamium]:https://github.com/runabove/beamium