
## Instruções de utilização

##Configuração de conexão no Esp32:

#Portas arduino:

- LEDS
15 - led 1
02 - led 2
04 - led 3

- Bomba de água
17 - bomba
34 - sensorUmidade

- Sensor de Presença
16 - sensorMovimento

- Som de bipe   
5 - Buzzer


#Comunicação Entre ESP32 e App inventor:

Foi definodo para que o App Inventor enviasse 1 byte de sinal bluetooth em decimal para o arduino receber,
então no script (../src/src-C++/main.c++) vai receber números inteiros apartir da condição SerialBT.read().

- LED1 (pino 15):
Ligar: 1
Desligar: 0

- LED2 (pino 2):
Ligar: 2
Desligar: 3

- LED3 (pino 4):
Ligar: 4
Desligar: 5

- Bomba Hidráulica (pino 17):
Ligar: 6
Desligar: 7

- Buzzer (pino 5):
Ligar: 8
Desligar: 9

- Sensor alarme (pino 16):
Ligar: 10
Deligar:11


---

##Importação de código App Inventor:

Baixe o arquivo .aia e importe para o APP Inventor.

<li><a href="App\Casa_Inteligente.aia"> Arquivo .aia</a></li>

Depois conecte com o celular ao aplicativo no via QRcode.

---

##Configuração de Esp32 e compilação

Para usar e programar ESP32 na IDE do Arduino, precisamos primeiro que ele reconheça os
modelos da placa. Para isso, primeiramente devemos ir até as Preferências (Arquivo/Preferências) e
colar a URL abaixo no campo de URLs adicionais:

https://dl.espressif.com/dl/package_esp32_index.json

Com isso, permitimos que a IDE acesse uma pequena “base de dados” no formato .json que contém
a configuração de inúmeras placas. Após isso, devemos acessar o menu Ferramentas -> Placa ->
Gerenciador de Placas.

Nele, pesquise por ‘esp32′ na caixa de pesquisa. Em seguida, instale a versão mais recente do
driver que irá aparecer: “esp32 by Espressif Systems’.

Feito isso, você deve selecionar a placa “ESP32 Dev Module”, no menu de placas, para programar
na ESP.

Por fim, basta você selecionar a porta a qual a ESP está conectada (vá em Ferramentas/Porta/”porta
que Esp32 está conectado”)

#Compilação

- Baixe o arquivo .ino

<li><a href="Codigo\Casa_Inteligente.ino"> Arquivo .ino</a></li>

- Abra o aplicativo Arduino IDE e clique em "arquivo" na parte superior esquerda, depois abrir. Selecione o arquivo baixado e clique na seta para esquerda para compilar o código. Assim, você estará passando o código para o Esp32.

