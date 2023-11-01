### Objetivo do Projeto:
O objetivo do projeto é criar um sistema de automação residencial ou monitoramento ambiental usando um dispositivo baseado no ESP8266. O projeto pode ser usado para controlar dispositivos elétricos (como lâmpadas ou aparelhos) remotamente e monitorar a temperatura e a umidade em um ambiente. Ele também é capaz de se comunicar com um servidor MQTT para enviar e receber comandos e dados.

### Funcionalidade do Projeto:

Controle de Relés: O projeto permite ligar ou desligar dispositivos elétricos conectados aos relés remotamente por meio de mensagens MQTT. Quando uma mensagem MQTT é recebida em um tópico específico, o código do ESP8266 interpreta a mensagem e controla o estado dos relés.

Leitura de Sensores: O sensor DHT11 é usado para medir a temperatura e a umidade no ambiente. Os dados coletados são publicados em tópicos MQTT, permitindo o monitoramento desses valores a partir de um aplicativo ou outro dispositivo MQTT.

Comunicação MQTT: O dispositivo se conecta a um servidor MQTT e assina tópicos específicos para receber comandos de controle e envia dados de sensores. Isso permite a integração com outros dispositivos e sistemas MQTT.

### Arquitetura do Projeto :
A arquitetura do projeto pode ser resumida da seguinte forma:

Dispositivo ESP8266:

O dispositivo baseado no ESP8266 é o núcleo do projeto. Ele se conecta à rede Wi-Fi local e utiliza a biblioteca PubSubClient para se comunicar com um servidor MQTT.
Controla relés para ligar/desligar dispositivos elétricos conectados.
Lê dados de sensores (temperatura e umidade) do sensor DHT11.
Publica os dados dos sensores em tópicos MQTT específicos e assina tópicos para receber comandos.
Servidor MQTT:

Um servidor MQTT (geralmente um Raspberry Pi ou um servidor em nuvem) é usado para facilitar a comunicação entre dispositivos.
O servidor MQTT gerencia os tópicos, permite que dispositivos publiquem dados e assinem tópicos para receber comandos.
Aplicativo ou Outro Dispositivo MQTT:

Um aplicativo de automação residencial ou outro dispositivo MQTT pode se conectar ao servidor MQTT para enviar comandos de controle e receber dados dos sensores do dispositivo ESP8266.
O projeto cria uma plataforma de automação e monitoramento que permite controlar dispositivos elétricos e coletar informações ambientais usando um dispositivo IoT conectado à rede Wi-Fi e à infraestrutura MQTT. Isso possibilita a criação de soluções de automação residencial personalizadas e sistemas de monitoramento ambiental.



### Sensores:

PIR Motion Sensor (sensor de movimento por infravermelho passivo) - Detecta movimento e é geralmente usado para segurança ou automação residencial.
DHT11 Temperature & Humidity Sensor (sensor de temperatura e umidade) - Mede a temperatura e a umidade do ambiente.
Proximity Sensor (sensor de proximidade) - Detecta objetos próximos e é frequentemente usado em aplicações de detecção de presença ou proximidade.
MQ135 Gas Sensor (sensor de gás) - Detecta a presença de gases específicos no ambiente, como CO2 e amônia.
LDR Light Sensor (sensor de luz) - Detecta a intensidade de luz no ambiente e é comumente usado para controle de luminosidade.

## Atuadores:

ESP32 Board - Um microcontrolador que pode ser programado para controlar dispositivos e processar dados de sensores.
NodeMCU - Outro microcontrolador baseado no ESP8266, que pode ser usado para a automação e controle de dispositivos.
5V Relay (relé) - É usado para controlar dispositivos de alta tensão ou corrente com sinais de baixa tensão, como um microcontrolador.
BC547 Transistor - Pode ser usado como um interruptor eletrônico para controlar corrente em circuitos.
9V 2A Adapter (adaptador de energia) - Fornecerá energia ao sistema, mas não é estritamente um atuador no sentido tradicional.
7805 IC (regulador de tensão) - É usado para fornecer uma tensão regulada a partir de uma entrada não regulada.
2-Pin Terminal Connectors (conectores terminais de 2 pinos) - São usados para fazer conexões elétricas.
Componentes passivos:

1N4007 Diode (diodo) - É usado para direcionar o fluxo de corrente em um circuito.
330 ohm Resistors (resistores de 330 ohms) - São componentes passivos que podem ser usados para limitar a corrente ou dividir a tensão em um circuito.