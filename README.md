# 🚀 Sistema IoT — Monitoramento de Cápsula Espacial

> **FIAP — Global Solution 2026 · 1º Semestre**  
> Ciência da Computação — Desafio: Indústria Espacial

---

## 📡 Sobre o Projeto

Sistema embarcado baseado em **ESP32** que monitora em tempo real as condições físicas internas de uma cápsula espacial, simulando aplicações reais utilizadas em missões aeroespaciais.

O sistema coleta, processa e exibe continuamente três grandezas físicas essenciais para a segurança operacional do módulo:

| Grandeza | Sensor | Pino | Faixa Segura |
|---|---|---|---|
| 🌡️ Temperatura interna | DHT22 | GPIO 4 | 18°C a 35°C |
| 💡 Luminosidade | LDR / Fotoresistor | GPIO 34 | > 15% |
| 📳 Vibração / Impacto | Potenciômetro (simulado) | GPIO 35 | < 600 ADC |

---

## 🛰️ Conexão com a Indústria Espacial

- **ODS 9** — Inovação e infraestrutura tecnológica
- **ODS 13** — Ação climática e monitoramento ambiental

Sistemas IoT embarcados são o núcleo das missões modernas: o Perseverance opera com 200 milhões de linhas de instruções; o Falcon 9 roda em Linux em tempo real. Este projeto simula a camada de aquisição de dados que garante a sobrevivência de astronautas em ambientes extremos.

---

## 🔧 Hardware & Componentes

```
ESP32 DevKit V1
├── DHT22          — temperatura e umidade (GPIO 4)
├── LDR Sensor     — luminosidade analógica (GPIO 34)
├── Potenciômetro  — vibração simulada (GPIO 35)
├── LCD 16x2 I2C   — display de dados (SDA: GPIO 21 / SCL: GPIO 22)
├── LED Verde       — status normal (GPIO 25)
├── LED Amarelo     — atenção (GPIO 26)
├── LED Vermelho    — alerta crítico (GPIO 27)
└── Buzzer         — alarme sonoro (GPIO 14)
```

---

## ⚙️ Funcionalidades

- ✅ Leitura contínua dos 3 sensores a cada 2 segundos
- ✅ Display LCD 16x2 com rotação automática entre 3 telas
- ✅ Sistema de LEDs tricolor (verde / amarelo / vermelho)
- ✅ Buzzer com padrão de alerta (3 bipes)
- ✅ Log formatado no Serial Monitor com timestamps
- ✅ Contador de alertas acumulados
- ✅ Barra visual de luminosidade no LCD
- ✅ Sequência de boot animada nos LEDs
- ✅ Tela de splash com nome do projeto

### Telas do LCD

| Tela | Linha 1 | Linha 2 |
|------|---------|---------|
| 1 | Temperatura (°C) | Umidade (%) |
| 2 | Luminosidade (%) | Barra visual |
| 3 | Vibração (ADC) | Alertas acumulados + status |

---

## 🖥️ Simulação no Wokwi

Acesse a simulação completa:  
**🔗 [Link do Wokwi — adicionar após criar o projeto]**

### Como importar no Wokwi:
1. Acesse [wokwi.com](https://wokwi.com) e crie uma conta gratuita
2. Clique em **"New Project"** → **ESP32**
3. Substitua o conteúdo do `sketch.ino` pelo arquivo `src/capsula_monitor.ino`
4. Clique no botão `+` e importe o `wokwi/diagram.json`
5. Clique em **▶ Start Simulation**

---

## 📁 Estrutura do Repositório

```
capsula-espacial/
├── src/
│   └── capsula_monitor.ino     ← Código principal ESP32
├── wokwi/
│   ├── diagram.json            ← Circuito completo
│   ├── libraries.txt           ← Bibliotecas necessárias
│   └── wokwi.toml              ← Configuração do projeto Wokwi
├── docs/
│   └── relatorio_tecnico.pdf   ← Relatório técnico (a gerar)
├── assets/
│   └── (imagens do circuito e prints da simulação)
└── README.md
```

---

## 📦 Bibliotecas Arduino

Instale via Arduino IDE → *Gerenciador de Bibliotecas*:

```
LiquidCrystal I2C  (by Frank de Brabander)
DHT sensor library  (by Adafruit)
Adafruit Unified Sensor
```

---

## 🚨 Sistema de Alertas

```
🟢 LED VERDE    — Todos os parâmetros dentro da faixa segura
🟡 LED AMARELO  — Valores próximos ao limite (zona de atenção)
🔴 LED VERMELHO — Parâmetro fora da faixa crítica + BUZZER
```

**Condições que disparam alerta crítico:**
- Temperatura < 18°C ou > 35°C
- Luminosidade < 15%
- Vibração > 600 (ADC)

---

## 📊 Serial Monitor — Formato de Log

```
Timestamp(ms) | Temp(C) | Umid(%) | Luz(%) | Vibr(ADC) | Status
-------------|---------|---------|--------|-----------|--------
2000         | 24.50   | 55.30   | 72     | 312       | normal
4000         | 24.60   | 55.10   | 10     | 315       | ALERTA!
```

---

## 🎥 Vídeo Demonstrativo

**🔗 [Link do YouTube — adicionar após gravar]**

---

## 👥 Integrantes

| Nome | RM |
|------|----|
| [Nome 1] | RM XXXXX |
| [Nome 2] | RM XXXXX |
| [Nome 3] | RM XXXXX |
| [Nome 4] | RM XXXXX |

---

## 📄 Licença

Projeto acadêmico desenvolvido para a FIAP — Global Solution 2026.
