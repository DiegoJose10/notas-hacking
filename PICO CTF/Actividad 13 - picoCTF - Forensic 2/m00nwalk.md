Decode this [message](https://jupiter.challenges.picoctf.org/static/d6fcea5e3c6433680ea4f914e24fab61/message.wav) from the moon.
Hints:
- How did pictures from the moon landing get sent back to Earth?
- What is the CMU mascot?, that might help select a RX option
# Solucion
Al hacer clic en el enlace de mensaje nos proporciona un archivo de audio **_.wav_**, El reto hace referencia a como el Apolo 11 utilizó la televisión de escaneo lento (TV) incompatible con la televisión. 
Instalando y usando QSSTV, una herramienta para decodificar transmisiones y **pavucontrol** (para gestionar la conexión de audio virtual): $ sudo apt install qsstv & & sudo apt install pavucontrol -y 
$ qsstv $ pavucontrol y uniendolos en una conexion virtual $ pactl load-module module-null-sink sink_name=virtual-cable
se puede transmitir el archivo. wav usando $ paplay -d virtual-cable message.wav y viendo QSSTV la imagen empieza a  renderizarse y nos proporciona la bandera
picoCTF{beep_boop_im_in_space}
