# Vision Inspection

Inspeção inline por câmara para defeitos de superfície, qualidade de impressão
e tolerâncias dimensionais.

## Destaques

- Até 1200 peças por minuto com resolução de 5 MP.
- Modelo de classificação de defeitos re-treinável no painel do operador.
- Rejeições registadas com prova de imagem durante 90 dias.

## Configuração

```json
{
  "camera": { "resolution": "2448x2048", "fps": 60 },
  "trigger": "encoder",
  "model": "surface-defect-v4",
  "confidenceThreshold": 0.82
}
```

## Resultados

| Indicador | Antes | Depois |
| --- | --- | --- |
| Defeitos não detetados | 1,8 % | 0,2 % |
| Esforço de inspeção manual | 2 operadores | 0,5 operador |
| Paragem de linha por turno | 22 min | 7 min |

## Limitações

Superfícies transparentes e espelhadas exigem um pacote de iluminação adicional
que não faz parte do âmbito padrão.
