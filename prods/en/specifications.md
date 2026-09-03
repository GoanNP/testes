# Specifications

## Common platform

All products share the same controller image, which keeps spare-part handling
and firmware updates identical across the catalog.

| Property | Value |
| --- | --- |
| Controller | x86-64 quad core, 16 GB RAM |
| Storage | 256 GB industrial SSD |
| Operating system | Debian 12 (hardened image) |
| Supply voltage | 24 V DC ±10 % |
| Operating temperature | 0 °C to 45 °C |
| Protection class | IP54 (cabinet mounted) |

## Interfaces

- 2 × Gigabit Ethernet (plant network and device network, physically separated)
- 4 × USB 3.0 for cameras, scanners or service tooling
- 1 × isolated digital I/O block, 8 inputs and 8 outputs
- Optional PROFINET or EtherNet/IP add-on card

## Software stack

```yaml
runtime:
  container: podman
  telemetry: opentelemetry
  storage: postgresql
protocols:
  - opc-ua
  - mqtt
  - modbus-tcp
```

## Certification

The hardware carries CE and UKCA marks. Functional safety is not part of the
base product; safety circuits must be provided by the surrounding machine.
