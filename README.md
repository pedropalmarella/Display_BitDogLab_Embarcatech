# Projeto: Interação com PC, Botões e LEDs no RP2040

Este projeto implementa diversas funcionalidades utilizando o microcontrolador RP2040, explorando **entrada de caracteres via PC**, **interação com botões físicos**, e **controle de LEDs e displays**. As funcionalidades incluem entrada de caracteres pelo **Serial Monitor**, exibição em um **display SSD1306**, controle de **LEDs RGB** e uma matriz **WS2812**. Todas as interações com botões são gerenciadas com interrupções e tratamento de bouncing via software, foram utilizadas as comunicações UART e I2C.

## Funcionalidades

### Entrada de Caracteres via PC
- Os caracteres são digitados pelo **Serial Monitor** do VS Code e enviados ao microcontrolador.
- Cada caractere é exibido no **display SSD1306**.
- Caracteres numéricos (0 a 9) acendem o **símbolo correspondente** na matriz de LEDs **5x5 WS2812**.

### Interação com Botão A
- **Alterna o estado** do LED RGB **Verde** (ligado/desligado).
- Exibe no **display SSD1306** o estado atual do LED.
- Envia uma mensagem descritiva ao **Serial Monitor** indicando a alteração.

### Interação com Botão B
- **Alterna o estado** do LED RGB **Azul** (ligado/desligado).
- Exibe no **display SSD1306** o estado atual do LED.
- Envia uma mensagem descritiva ao **Serial Monitor** indicando a alteração.

### Outros Recursos
- **Controle de LEDs WS2812**: Exibição de padrões simbólicos em resposta a entradas numéricas.
- **Debouncing via Software**: Tratamento eficiente do bouncing dos botões.
- **Comunicação UART**: Envio de informações e mensagens descritivas ao Serial Monitor.
- **Display SSD1306 (I2C)**: Exibição de caracteres e mensagens informativas com suporte a fontes maiúsculas e minúsculas.

## Tecnologias Utilizadas

- **Microcontrolador**: Raspberry Pi Pico (RP2040)
- **Linguagem de Programação**: C (usando o **Pico SDK**)
- **Ambiente de Desenvolvimento**: Visual Studio Code (VSCode) com Pico SDK
- **Hardware**:
  - **Display SSD1306** (128x64 pixels) via protocolo I2C
  - **Matriz de LEDs WS2812** (5x5)
  - **LEDs RGB comuns**
  - **Botões físicos**
  
## Como Usar

Entrada de Caracteres:

- **Abra o Serial Monitor no VS Code**.
- **Digite caracteres individuais**:
- **Eles serão exibidos no display SSD1306(I2C)**.
- **Números (0-9) acenderão símbolos correspondentes na matriz WS2812**.

- **Interação com Botão A**:

Pressione o botão A para alternar o estado do LED RGB Verde.
O estado será exibido no display e enviado ao Serial Monitor.

- **Interação com Botão B**:

Pressione o botão B para alternar o estado do LED RGB Azul.
O estado será exibido no display e enviado ao Serial Monitor.

- **Feedback Visual e Auditivo**:

Observe as mudanças no display, LEDs e mensagens no Serial Monitor durante as interações.
