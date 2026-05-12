# ❤️ CardioIA – Fase 3

Michelle Guedes Cavalari RM564557

## 📌 Sobre o projeto

O projeto **CardioIA – Fase 3** tem como objetivo simular um sistema inteligente de monitoramento cardíaco utilizando conceitos de:

* Internet das Coisas (IoT)
* Edge Computing
* Computação em Nuvem
* MQTT
* Monitoramento de sinais vitais
* Sistemas embarcados com ESP32

Nesta fase, foi desenvolvido um protótipo funcional capaz de:

* Capturar sinais vitais simulados;
* Processar dados localmente;
* Simular resiliência offline;
* Transmitir informações via MQTT;
* Enviar dados para nuvem utilizando HiveMQ Cloud.

O projeto foi desenvolvido utilizando o simulador **Wokwi**, sem necessidade de hardware físico.

---

# 🎯 Objetivo da Fase 3

Desenvolver um sistema vestível de monitoramento cardíaco capaz de:

✅ Simular sensores médicos;

✅ Processar dados localmente (Edge Computing);

✅ Continuar funcionando mesmo sem internet;

✅ Enviar dados para a nuvem via MQTT;

✅ Emitir alertas automáticos para condições críticas.

---

# 🧠 Conceitos aplicados

## 🔹 IoT (Internet das Coisas)

O ESP32 atua como dispositivo IoT responsável por coletar dados dos sensores e transmiti-los para a nuvem.

---

## 🔹 Edge Computing

O processamento inicial dos dados é realizado localmente no ESP32.

Isso permite:

* menor latência;
* funcionamento offline;
* resposta rápida;
* redução do tráfego de rede.

---

## 🔹 MQTT

Foi utilizado o protocolo MQTT para envio dos dados para a nuvem.

O MQTT é um protocolo leve e eficiente, muito utilizado em aplicações IoT.

---

## 🔹 Cloud Computing

Os dados foram enviados para o **HiveMQ Cloud**, funcionando como broker MQTT em nuvem.

---

# 🛠 Tecnologias utilizadas

| Tecnologia    | Função                            |
| ------------- | --------------------------------- |
| ESP32         | Microcontrolador IoT              |
| Wokwi         | Simulador eletrônico              |
| DHT22         | Sensor de temperatura e umidade   |
| Potenciômetro | Simulação de batimentos cardíacos |
| HiveMQ Cloud  | Broker MQTT em nuvem              |
| MQTT          | Protocolo de comunicação          |
| C++           | Linguagem de programação          |
| GitHub        | Versionamento e documentação      |

---

# ⚙️ Estrutura do projeto

```text
CardioIA-Fase3
│
├── codigo
│   ├── cardioia_fase3.ino
│   └── link_wokwi.txt
│
├── prints
│   ├── circuito-wokwi.png
│   ├── serial-monitor.png
│   ├── hivemq-conectado.png
│   └── mqtt-funcionando.png
│
├── videos
│
└── README.md
```

---

# 🔌 Componentes utilizados

## 📍 ESP32

Responsável pelo processamento e envio dos dados.

---

## 📍 DHT22

Sensor utilizado para:

* temperatura;
* umidade.

---

## 📍 Potenciômetro

Utilizado para simular os batimentos cardíacos do paciente.

---

# 🔗 Ligações do circuito

## DHT22

| DHT22 | ESP32   |
| ----- | ------- |
| VCC   | 3V3     |
| DATA  | GPIO 15 |
| GND   | GND     |

---

## Potenciômetro

| Potenciômetro | ESP32   |
| ------------- | ------- |
| VCC           | 3V3     |
| SIG           | GPIO 34 |
| GND           | GND     |

---

# 📡 Fluxo do sistema

```text
Sensores
   ↓
ESP32
   ↓
Processamento Local
   ↓
MQTT
   ↓
HiveMQ Cloud
   ↓
Monitoramento em Nuvem
```

---

# ❤️ Sinais vitais simulados

O sistema gera automaticamente:

| Variável    | Faixa simulada  |
| ----------- | --------------- |
| Temperatura | 36°C até 39.5°C |
| Umidade     | 35% até 80%     |
| BPM         | 45 até 145 bpm  |

---

# 🚨 Sistema de alertas

O sistema emite alertas automáticos quando:

| Condição           | Alerta           |
| ------------------ | ---------------- |
| Temperatura > 38°C | Temperatura alta |
| BPM > 120          | Taquicardia      |
| BPM < 50           | Bradicardia      |

---

# 🌐 MQTT

## Broker utilizado

HiveMQ Cloud

---

## Tópicos MQTT utilizados

```text
cardioia/temperatura
cardioia/umidade
cardioia/bpm
cardioia/alerta
```

---

# ☁️ Resiliência Offline

O projeto simula funcionamento offline utilizando lógica de Edge Computing.

Quando o Wi-Fi está indisponível:

* os dados continuam sendo coletados;
* o sistema mantém o processamento local;
* os dados ficam armazenados temporariamente.

Quando a conexão retorna:

* os dados são sincronizados;
* o envio MQTT é retomado.

---


# ▶️ Como executar

## 1. Abrir o projeto no Wokwi

Acesse o link do simulador.

---

## 2. Executar a simulação

Clique em:

```text
Start Simulation
```

---

## 3. Abrir o Serial Monitor

Visualize:

* conexão Wi-Fi;
* conexão MQTT;
* temperatura;
* umidade;
* BPM;
* alertas.


---

# 📚 Aprendizados

Durante esta fase foram aplicados conceitos importantes de:

* IoT;
* MQTT;
* Edge Computing;
* Computação em Nuvem;
* Sistemas embarcados;
* Monitoramento em saúde;
* Comunicação em tempo real.

---

# 👩‍💻 Autora

Michelle Guedes Cavalari

Graduação em Inteligência Artificial – FIAP

---

# 🚀 Considerações finais

O projeto CardioIA demonstra como tecnologias IoT podem ser aplicadas na área da saúde para monitoramento remoto de pacientes.

Mesmo utilizando um ambiente simulado, foi possível implementar:

* coleta de dados;
* processamento local;
* resiliência offline;
* comunicação MQTT;
* integração com nuvem.

A solução proposta apresenta grande potencial para aplicações reais de telemedicina, monitoramento contínuo e saúde digital.
