# Integração

## Topologia de rede

Cada produto usa duas interfaces de rede separadas. A interface de equipamento
permanece na rede da máquina; a interface fabril transporta apenas dados
agregados.

```
[ Rede da máquina 192.168.10.0/24 ]---( eth1 )  Produto  ( eth0 )---[ Rede fabril ]
```

## Serviços necessários na fábrica

| Serviço | Finalidade | Porta |
| --- | --- | --- |
| Broker MQTT | Envio de telemetria | 8883 |
| NTP | Sincronização horária | 123 |
| Coletor Syslog | Auditoria e diagnóstico | 6514 |

## Exemplo de configuração de uplink

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

## Lista de verificação de comissionamento

- [ ] Endereços IP estáticos atribuídos nas duas interfaces
- [ ] Certificado do equipamento instalado e validado
- [ ] Fonte horária acessível e desvio inferior a 50 ms
- [ ] Execução em modo sombra concluída durante um turno completo
