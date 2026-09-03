# Integration

## Network layout

Each product uses two separated network interfaces. The device interface stays
inside the machine network, the plant interface carries only aggregated data.

```
[ Machine network 192.168.10.0/24 ]---( eth1 )  Product  ( eth0 )---[ Plant network ]
```

## Required plant services

| Service | Purpose | Port |
| --- | --- | --- |
| MQTT broker | Telemetry uplink | 8883 |
| NTP | Time synchronization | 123 |
| Syslog collector | Audit and diagnostics | 6514 |

## Example uplink configuration

```yaml
uplink:
  broker: mqtts://broker.plant.internal:8883
  clientId: line-04-vision
  topicPrefix: plant/line-04/vision
  qos: 1
credentials:
  method: client-certificate
  certPath: /etc/product/certs/device.pem
```

## Commissioning checklist

- [ ] Static IP addresses assigned on both interfaces
- [ ] Device certificate installed and validated
- [ ] Time source reachable and drift under 50 ms
- [ ] Shadow-mode run completed for one full shift
