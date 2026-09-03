# Vision Inspection

Camera-based inline inspection for surface defects, print quality and
dimensional tolerances.

## Highlights

- Up to 1200 parts per minute at 5 MP resolution.
- Defect classification model retrainable from the operator panel.
- Rejects are logged with image evidence for 90 days.

## Configuration

```json
{
  "camera": { "resolution": "2448x2048", "fps": 60 },
  "trigger": "encoder",
  "model": "surface-defect-v4",
  "confidenceThreshold": 0.82
}
```

## Outcomes

| Metric | Before | After |
| --- | --- | --- |
| Escaped defects | 1.8 % | 0.2 % |
| Manual inspection effort | 2 operators | 0.5 operator |
| Line stop time per shift | 22 min | 7 min |

## Limitations

Transparent and mirrored surfaces require an additional lighting package that
is not part of the standard scope.
