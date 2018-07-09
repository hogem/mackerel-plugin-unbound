mackerel-plugin-unbound
===

## Description

Get unbound stats (unbound-control stats) metrics for Mackerel

## Usage

config.yaml

```yaml
---
unbound_control: /usr/sbin/unbound-control
metrics_prefix: unbound
stats:
  - ^total.num

```

```
$ sudo ./mackerel-plugin-unbound
unbound.total.num.queries       762108  1531125546
unbound.total.num.cachehits     687451  1531125546
unbound.total.num.cachemiss     74657   1531125546
unbound.total.num.prefetch      4128    1531125546
unbound.total.num.recursivereplies      74656   1531125546
```

### mackerel-agent.conf
```
[plugin.metrics.unbound]
command = "/path/to/mackerel-plugin-unbound"
```

## Requirements

- Python 3
- pyyaml
