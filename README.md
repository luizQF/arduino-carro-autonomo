# 🚗 Carro Autônomo com Desvio de Obstáculos (Arduino + Python)

Um projeto de robótica e automação que combina **Arduino** (para controle físico) e **Python** (para inteligência e decisão).  
O robô é capaz de **andar sozinho e evitar colisões** usando sensores ultrassônicos e algoritmos simples de lógica ou IA.

---

## 🎯 Objetivos do projeto

- Controlar um carro robô de forma **autônoma**.  
- Integrar **hardware (Arduino)** e **software inteligente (Python)**.  
- Aplicar conceitos de **sensoriamento, controle e decisão**.  
- Criar uma base expansível para projetos com **IA ou visão computacional**.

---

## ⚙️ Componentes necessários

| Componente | Quantidade | Função |

| Arduino Uno / Nano | 1 | Unidade principal de controle |
| Módulo Ponte H L298N | 1 | Controle dos motores DC |
| Motores DC com roda | 2 | Movimento do carro |
| Roda boba | 1 | Equilíbrio |
| Sensor ultrassônico HC-SR04 | 1 a 2 | Detecção de obstáculos |
| Bateria 9V ou 18650 (2x) | 1 pack | Alimentação |
| Jumpers e base acrílica | — | Conexões físicas |
| Modulo ESP8266 | 1 | Conexão remota |


---

## 🧩 Fluxo do sistema

### 🔄 Explicação detalhada

1. **Sensores do Arduino** medem continuamente a distância até obstáculos (ultrassônico).  
2. O **Arduino envia essas leituras via serial** para o Python.  
3. O **Python recebe os dados**, analisa e decide a ação mais adequada para o carro:
   - Seguir em frente  
   - Virar à esquerda  
   - Virar à direita  
   - Reduzir velocidade ou parar  
4. O **Python envia o comando** de volta para o Arduino (ex: “F” = frente, “L” = esquerda, “R” = direita).  
5. O **Arduino interpreta o comando** e ajusta a velocidade e direção dos motores.  
6. Esse ciclo se repete continuamente, permitindo que o carro **ande sozinho e evite obstáculos em tempo real**.  

