A digital ghost has breached my defenses, and my sensitive data has been stolen! 😱💻 Your mission is to uncover how this phantom intruder infiltrated my system and retrieve the hidden flag. To solve this challenge, you'll need to analyze the provided PCAP file and track down the attack method. The attacker has cleverly concealed his moves in well timely manner. Dive into the network traffic, apply the right filters and show off your forensic prowess and unmask the digital intruder! Find the PCAP file here [Network Traffic PCAP file](https://challenge-files.picoctf.net/c_verbal_sleep/b6fbb3a5560749f838cdc6db4950985767c4691db3a7b34a220e5654ee39e700/myNetworkTraffic.pcap) and try to get the flag.
Hints:
- Filter your packets to narrow down your search.
- Attacks were done in timely manner.
- Time is essential
# Solución
El archivo es un pcap asi que se utiliza wireshark para analizarlo. Al inspeccionar el tráfico, habia pequeños fragmentos de codigo en base 64 dentro de los paquetes de datos. Esto indicaba que algunos paquetes contenian parte de la bandera. Se miran todas las partes que tenian == ya que eso es un posible identificador de base64 y se colocan en cyberchef, despues se acomodan de tal forma que la bandera tenga coherencia. Finalmente queda:
cGljb0NURg==
ezF0X3c0cw==
bnRfdGg0dA==
XzM0c3lfdA==
YmhfNHJfMw==
NmY0YTY2Ng==
fQ==
Y al decodificarlo se obtiene la bandera
picoCTF{1t_w4snt_th4t_34sy_tbh_4r_36f4a666}

# Referencias
- https://gchq.github.io/CyberChef/