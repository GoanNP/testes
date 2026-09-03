# Especificações

## Plataforma comum

Todos os produtos partilham a mesma imagem de controlador, o que mantém a
gestão de peças e as atualizações de firmware idênticas em todo o catálogo.

| Propriedade | Valor |
| --- | --- |
| Controlador | x86-64 quad core, 16 GB RAM |
| Armazenamento | SSD industrial de 256 GB |
| Sistema operativo | Debian 12 (imagem endurecida) |
| Tensão de alimentação | 24 V DC ±10 % |
| Temperatura de operação | 0 °C a 45 °C |
| Grau de proteção | IP54 (montagem em armário) |

## Interfaces

- 2 × Gigabit Ethernet (rede fabril e rede de equipamentos, fisicamente separadas)
- 4 × USB 3.0 para câmaras, leitores ou ferramentas de serviço
- 1 × bloco de I/O digital isolado, 8 entradas e 8 saídas
- Placa opcional PROFINET ou EtherNet/IP

## Stack de software

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

## Certificação

O hardware possui marcação CE e UKCA. A segurança funcional não faz parte do
produto base; os circuitos de segurança são da máquina envolvente.
