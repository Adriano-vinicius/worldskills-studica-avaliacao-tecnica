# ⚡ Checklist Elétrico — WorldSkills AMR Studica Lyon 2024

![Status](https://img.shields.io/badge/status-em%20execu%C3%A7%C3%A3o-yellow)
![WorldSkills](https://img.shields.io/badge/WorldSkills-Autonomous%20Mobile%20Robotics-blue)
![Kit](https://img.shields.io/badge/Kit-Studica%20Lyon%202024-purple)
![Checklist](https://img.shields.io/badge/Checklist-El%C3%A9trico-green)

## 📌 Objetivo da atividade

Executar uma inspeção elétrica no robô da modalidade **Autonomous Mobile Robotics**, utilizando o kit **Studica Robotics WorldSkills Lyon 2024 Mobile Robotics Collection**.

A atividade tem como foco verificar:

- Alimentação acima de **12 VDC**
- Fusíveis
- Power Control Panel
- E-Stop
- Titan Quad Motor Controller
- VMX Robotics Controller
- VMX IO 5V
- Rotas de cabeamento
- Pontos críticos do sistema

---

## 🧰 Kit utilizado

| Item | Part # | Função no sistema |
|---|---:|---|
| 12V 3000mAh NiMH Battery Pack PP45 | 70018 | Alimentação principal |
| Powerpole 45 Extension Cable | 70021 | Extensão da alimentação |
| Power Control Panel | 70170 | Controle de liga/desliga, status e emergência |
| Titan Quad Motor Controller | 70152 | Controle dos motores DC via CAN |
| VMX Robotics Controller | 70176 | Controlador principal do robô |
| VMX Cable Pack | 70160 | Cabos de conexão do VMX |
| Titan Cable Pack CAN/JST-VH | 70162 | Comunicação e alimentação entre módulos |
| Maverick 12V DC Gear Motor w/Encoder | 75001 | Motores de tração |
| Ultrasonic Distance Sensor | 70753 | Sensor de distância |
| 3D Depth Sense Camera | 71044 | Visão/profundidade |
| 360 Degree LiDAR | 70500 | Mapeamento e percepção 360° |

---

## 🔌 Fluxo lógico do sistema elétrico

```mermaid
flowchart LR
    A[Bateria 12V PP45] --> B[Power Control Panel]
    B --> C[E-Stop / Liga-Desliga / Status]
    C --> D[Titan Quad]
    D --> E[Motores Maverick 12V]
    D --> F[Saída 12V para VMX]
    F --> G[VMX Robotics Controller]
    G --> H[VMX IO 5V / 3.3V]
    H --> I[Sensores]
    G <-->|CAN-H / CAN-L| D
