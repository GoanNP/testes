# Suporte

## Níveis de serviço

| Nível | Tempo de resposta | Cobertura |
| --- | --- | --- |
| Padrão | 8 horas úteis | Seg–Sex, 08:00–17:00 |
| Alargado | 4 horas | Seg–Sáb, 06:00–22:00 |
| Linha crítica | 1 hora | 24 / 7 |

## Pacote de diagnóstico

Recolha o pacote de diagnóstico antes de abrir um pedido:

```bash
productctl diagnostics collect --since 24h --output /tmp/bundle.tar.gz
```

O pacote contém configuração, logs e os últimos 500 eventos. As imagens só são
incluídas com `--include-images`.

## Problemas frequentes

**O uplink permanece desligado.** Verifique se o certificado do equipamento
expirou e se a porta de saída 8883 está aberta.

**O tempo de ciclo degrada-se.** Normalmente causado por um buffer local cheio.
Verifique o espaço livre em disco e a definição de retenção.

**O painel do operador mostra valores antigos.** Reinicie o serviço do painel;
o pipeline subjacente continua a correr durante o reinício.

## Peças de substituição

Os controladores de substituição são fornecidos já com imagem. Após a troca do
controlador, o certificado do equipamento tem de ser reemitido.
