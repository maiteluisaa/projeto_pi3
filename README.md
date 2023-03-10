# Controle de irrigação via monitoramento de umidade - Projeto Integrador 3

O objetivo deste projeto é realizar o protótipo de um sistema de controle de irrigação de grandes áreas de plantação. 

Para chegar a esse objetivo será utilizado uma rede de sensores sem fio. Como o nome sugere, uma rede de sensores sem fio é uma rede sem fio de dispositivos autonômos que contém sensores distribuídos espacialmente para o monitoramento de fenômenos físicos. Uma rede de sensor sem fio pode ser encontrada de três formas: Estrela, Cluster e Árvore.

![Topologias](https://github.com/maiteluisaa/projeto_pi3/blob/main/images/Topologias.png)

Para compôr a rede será utilizado o microcontrolador [CC1350 LaunchPad](https://www.ti.com/tool/LAUNCHXL-CC1350), pois o mesmo está disponível para uso no IFSC. Como só há 3 peças disponíveis, a rede será feita na topologia de estrela: 2 transmissores e 1 receptor.

Para a definição do protocolo de comunicação dois pontos devem ser levados em consideração: consumo de energia e alcance de transmissão. Dois protocolos disponíveis no microcontrolador foram cogitados:

- Bluetooth Low Energy 2.4 GHz
- RF Sub 1GHz

O bluetooth foi descartado devido ao seu curto alcance. Um teste de alcance foi realizado com a rede sub 1 GHZ, chegando em torno de 90m (próximo dos 100m que constam no datasheet):

![Alcance](https://github.com/maiteluisaa/projeto_pi3/blob/main/images/alcance.png)

Para a aquisição de dados de humidade e temperatura foi adquirido o sensor FS200-SHT20, o mesmo possui precisão de humidade de 3% e de temperatura de 0,3°C.

![Esquemático](https://github.com/maiteluisaa/projeto_pi3/blob/main/images/ESQUEMA.png)

De forma resumida, os dados serão coletados pelos nós transmissores e enviados a nó receptor. O nó receptor enviará os dados via serial para um computador que fará o processamento da informação e o computador enviará os dados para a internet. A ideia é apresentar os dados numa dashboard e ter disponível o histórico da informação dos meses anteriores.

![Dashboard](https://github.com/maiteluisaa/projeto_pi3/blob/main/images/dashboard.png)
