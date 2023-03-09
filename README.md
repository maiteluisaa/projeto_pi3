# Controle de irrigação via monitoramento de umidade - Projeto Integrador 3

O objetivo deste projeto é realizar o protótipo de um sistema de controle de irrigação de grandes áreas de plantação. 

Para chegar a esse objetivo será utilizado uma rede de sensores sem fio. Como o nome sugere, uma rede de sensores sem fio é uma rede sem fio de dispositivos autonômos que contém sensores distribuídos espacialmente para o monitoramento de fenômenos físicos. Uma rede de sensor sem fio pode ser encontrada de três formas: Estrela, Cluster e Árvore.

![Topologias](https://github.com/maiteluisaa/projeto_pi3/blob/main/images/Topologias.png)

Para compôr a rede será utilizado o microcontrolador [CC1350 LaunchPad](https://www.ti.com/tool/LAUNCHXL-CC1350), pois o mesmo está disponível para uso no IFSC. Como só há 3 peças disponíveis, a rede será feita na topologia de estrela: 2 transmissores e 1 receptor.

Para a definição do protocolo de comunicação dois pontos devem ser levados em consideração: consumo de energia e alcance de transmissão.

- Bluetooth Low Energy 2.4 GHz
- RF Sub 1GHz
