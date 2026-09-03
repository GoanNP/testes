# Support

## Service levels

| Level | Response time | Coverage |
| --- | --- | --- |
| Standard | 8 business hours | Mon–Fri, 08:00–17:00 |
| Extended | 4 hours | Mon–Sat, 06:00–22:00 |
| Critical line | 1 hour | 24 / 7 |

## Diagnostics bundle

Collect the diagnostics bundle before opening a ticket:

```bash
productctl diagnostics collect --since 24h --output /tmp/bundle.tar.gz
```

The bundle contains configuration, logs and the last 500 events. Image data is
excluded unless `--include-images` is passed.

## Common issues

**Uplink stays disconnected.** Check that the device certificate has not
expired and that outbound port 8883 is open.

**Cycle time degrades over time.** Usually caused by a full local buffer.
Verify free disk space and the retention setting.

**Operator panel shows stale values.** Restart the panel service; the
underlying pipeline keeps running during the restart.

## Spare parts

Spare controllers are shipped pre-imaged. The device certificate must be
re-issued after a controller swap.
