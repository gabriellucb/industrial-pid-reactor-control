# Industrial PID Reactor Control (SCL/ST)

Implementação de um algoritmo de controle lógico para um reator químico industrial, desenvolvido em **Structured Control Language (SCL/ST)** conforme a norma IEC 61131-3. Este projeto demonstra a aplicação de conceitos matemáticos (Cálculo Diferencial e Integral) aplicados à automação de processos.

## 🧠 Lógica de Controle
O sistema utiliza uma Máquina de Estados Finita para gerenciar o ciclo de vida do processo e um controlador **PID (Proporcional-Integral-Derivativo)** implementado manualmente para o controle térmico.

### Estados do Processo:
1.  **Filling:** Controle de válvulas e sensores de nível.
2.  **Heating & Mixing:**
    * Implementação algorítmica da fórmula PID: `u(t) = Kp*e(t) + Ki*∫e(t)dt + Kd*de(t)/dt`.
    * Conversão da saída contínua do PID para sinal PWM (Pulse Width Modulation) para controle de resistências.
3.  **Draining:** Esvaziamento seguro do tanque.
4.  **Safety Interlock:** Rotina prioritária de parada de emergência.

## 💻 Stack Tecnológica
* **Linguagem:** Structured Text (ST) / SCL.
* **Ambiente Alvo:** Siemens TIA Portal / Rockwell Studio 5000.
* **Conceitos:** Closed-loop Control, Finite State Machine (FSM), PWM Modulation.

---
*Desenvolvido por [Gabriel Lucas Barbosa]*
