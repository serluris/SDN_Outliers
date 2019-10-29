# SDN_largura_banda
Projeto SDN, Openflow, Ryu, Mininet para limites de utilização

Requisitos básicos:
Ubuntu 18.04.3 (5.0.0-29),
Python 3.6.8 (scikit-learn 0.21.3; spicy 1.3.1; statistics 1.0.3.5; statsmodels 0.10.0; weightedstats 0.3),
Ryu 4.32,
Mininet 2.3.0d5,
OpenFlow 0x1:0x5 (ovs-vswitchd 2.9.2; ovs-ofctl 2.9.2).
  
  TUTORIAL SDN TESTE LIMITE DE BANDA: 
  
1 – Abrir terminal no diretório de testes ( em nosso caso Downloads/traffic)

2 – Iniciar terminal  == sudo mn –topo single, 4 –mac –controller ryu, simple_switch_13 –switch ovsk, protocols=OpenFlow13 –link tc, bw=1000 

3 – Executar comando no Mininet == xterm c0 h1 h2 h3 h4

4 – Executar comando em xterm c0 == sudo ryu-manager –verbose wma.py

5 – Executar comando em xterm h1 e h2 == iperf -s -p 5001

6 – Executar comando em xterm h3 ou h4 == iperf -c localhost -p 5001 -i 1 -t 60 -u -b 1M -xc -yc
