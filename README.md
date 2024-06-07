# EDGE-GS

# Integrantes
- Djalma Moreira de Andrade Filho, RM 555530
- Felipe Paes de Barros Muller Carioba, RM 558447
- Carlos Eduardo dos Santos Ribeiro Filho, RM 556785

# Visão Geral do Projeto

 Decidimos desenvolver uma embarcação robô controlada por Inteligência Artificial e parcialmente autônoma, denominada, temporariamente, Projeto Poseidon.
 Utilizaremos dados fornecidos pelas pesquisas de Institutos parceiros, analisaremos sua fonte e estudo, e assim, vamos aplicar nossa Inteligência Artificial para a análise completa dos dados, e aplicaremos nossa solução embasada em tais informações.
 Para o desenvolvimento sustentável do Projeto Poseidon que visa tornar o oceano mais saudável, utilizaremos recursos fornecidos pelas empresas parceiras.
  A Inteligência Artificial também será responsável por analisar dados e identificar as regiões mais poluídas do nosso oceano. Ela irá traçar uma rota ideal para conseguir efetuar a maior coleta de lixo marinho possível, e leva-lo para zonas recicláveis, reduzindo a carga de resíduos e objetos poluentes.
Também, ao coletar os resíduos, para casos em que ocorra, sem intuito, a captura de alguma forma de vida, nossa I.A, através de uma análise de objetos, alertará em nosso sistema que captou tal, e, assim, iremos filtrar nossa coleta, até que tal forma de vida vá um outro compartimento, onde liberaremos tal vida marinha, novamente, para as águas.
 Após a realização de nosso projeto, primeiramente desenvolvido para o Oceano Atlântico, buscaremos, posteriormente, ampliá-lo para outros oceanos, e, assim, controlaremos e monitoraremos nossas embarcações através do sistema cloud, que não utiliza servidores, sendo totalmente sustentável. Além disso, o sistema cloud também armazenará dados de nossas coletas, que serão enviados para a cátedra UNESCO para análise e pesquisas.


# Visão Geral

Este projeto implementa um sistema de coleta de resíduos e monitoramento de temperatura usando um servo motor, um sensor ultrassônico, um sensor de temperatura e umidade (DHT22), um display LCD e um buzzer. O sistema alterna entre medir a distância de objetos (para detecção de resíduos) e a temperatura ambiente, acionando mecanismos de coleta e alertas sonoros conforme necessário.

## Componentes Utilizados

- Arduino Uno ou qualquer microcontrolador compatível
- Servo Motor (SG90)
- Sensor Ultrassônico (HC-SR04)
- Sensor de Temperatura e Umidade (DHT22)
- Display LCD I2C (16x2)
- Buzzer
- LEDs (Verde e Vermelho)
- Resistores e Jumpers

## Conexões dos Componentes

- Trigger do Sensor Ultrassônico: Pino 2 do Arduino
- Echo do Sensor Ultrassônico: Pino 3 do Arduino
- Servo Motor: Pino 9 do Arduino
- LED Verde: Pino 10 do Arduino
- LED Vermelho: Pino 11 do Arduino
- Buzzer: Pino 12 do Arduino
- DHT22: Pino 7 do Arduino
- Display LCD I2C: Conectado via barramento I2C

## Funcionalidades do Código

### Inicialização:

- Configuração dos pinos.
- Inicialização do display LCD e do sensor DHT22.
- Posicionamento inicial do servo motor.

### Alternância de Modos:

- O sistema alterna entre modo de medição de distância e modo de medição de temperatura a cada 2 segundos.

### Medição de Distância:

- Utiliza o sensor ultrassônico para medir a distância até um objeto.
- Exibe a distância no display LCD.
- Se a distância for menor que 50 cm, ativa o servo motor, o LED verde e o buzzer para indicar coleta de resíduos.

### Medição de Temperatura:

- Utiliza o sensor DHT22 para medir a temperatura ambiente.
- Exibe a temperatura no display LCD.
- Se a temperatura for igual ou superior a 60°C, ativa o buzzer.

### Controle do Buzzer:

- O buzzer é ativado tanto para a coleta de resíduos quanto para alertar sobre alta temperatura.

## Como Utilizar

### Montagem do Circuito:

- Conecte todos os componentes conforme a seção de conexões.

### Upload do Código:

- Carregue o código fornecido no Arduino usando a IDE do Arduino.

### Operação:

- Após o upload e a inicialização, o sistema começará a alternar entre os modos de medição de distância e temperatura.
- Observe as ações do servo motor, LEDs e buzzer conforme as condições de distância e temperatura.

## Links:

- [Projeto no Wokwi](https://wokwi.com/projects/399997878789051393)
- [Vídeo de Explicação](https://youtu.be/tlACNckX74Q)
