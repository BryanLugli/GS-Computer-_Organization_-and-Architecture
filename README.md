#  Sistema IoT para Monitoramento de Cápsula Espacial

##  Integrantes

- Bryan Lugli  – RM 571350
- Beckman Lugli  – RM 573442
- Guilherme Xavier – RM 573053

##  Sobre o Projeto

Este projeto foi desenvolvido para o desafio Global Solution FIAP 2026, com o objetivo de criar um sistema IoT capaz de monitorar condições internas de uma cápsula espacial em tempo real.

A solução utiliza sensores para coletar dados de temperatura, luminosidade e vibração, permitindo acompanhar o ambiente da cápsula e identificar situações que possam comprometer a segurança da missão.

---

##  Objetivo

Desenvolver um sistema embarcado capaz de:

- Monitorar temperatura interna da cápsula;
- Monitorar luminosidade do ambiente;
- Detectar vibrações e possíveis impactos;
- Exibir informações em tempo real;
- Emitir alertas quando valores críticos forem detectados.

---

##  Tecnologias Utilizadas

### Hardware Simulado

- Arduino UNO
- Sensor de Temperatura (DHT22)
- Sensor de Luminosidade (LDR)
- Sensor de Vibração
- Display LCD 16x2
- LEDs de alerta
- Buzzer

### Software

- Arduino IDE
- Wokwi
- GitHub

---

##  Funcionamento

O sistema realiza leituras contínuas dos sensores.

### Temperatura

- Faixa normal: 18°C a 30°C
- Acima de 30°C → alerta de superaquecimento

### Luminosidade

- Monitora condições internas da cápsula
- Detecta variações anormais de iluminação

### Vibração

- Detecta impactos e turbulências
- Aciona alerta quando houver vibração excessiva

---

##  Fluxo do Sistema

```text
Sensores
   ↓
Arduino
   ↓
Processamento dos Dados
   ↓
Display LCD
   ↓
Alertas (LED/Buzzer)
```
---

##  Objetivos de Desenvolvimento Sustentável

Este projeto está alinhado com:

- ODS 9 – Indústria, Inovação e Infraestrutura
- ODS 11 – Cidades e Comunidades Sustentáveis
- ODS 13 – Ação Contra a Mudança Global do Clima

##  Licença

Projeto acadêmico desenvolvido para a FIAP – Global Solution 2026.
