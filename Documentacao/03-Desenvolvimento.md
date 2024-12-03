
# Materiais

Os materiais utilizados no projeto foram:
- ESP32
- Módulo Relé 5V
- Jumpers
- Bomba de água submersível (3V a 6V)
- 2 Protoboards de 400 pontos
- Buzzer ativo 3V
- Resistor 330R 1/4W
- LED alto brilho 5mm (branco)
- Sensor de obstáculos reflexivo infravermelho
- Módulo sensor de umidade de solo

# Desenvolvimento

Etepa 1: Definição do Projeto.

Etepa 2: Compra dos materiais.

Etepa 3: Contrução da casa e do circuito.

Etepa 4: Contrução do aplicativo e código do circuito.

Etepa 5: Integração da casa com os circuitos criados.

Etepa 6: Implementação do código para o Esp32.

Etepa 7: Ajustes finais.

Etepa 8: Entrega.

## Desenvolvimento do Aplicativo

### Interface

Foi criado um aplicativo com cinco telas, o visual minimalista ajuda no entendimento das funcionalidades. Todas as telas tem botões pensados para que consiga voltar a página principal.

### Código

O aplicativo contém a conexão bluetooth e depois que conecta uma vez não é necessário mais fazer a reconexão, pois ele armazena os dados do bluetooth em um banco de dados do APP Inventor chamado TinyDB.

Todas as telas estabelecem uma conexão direta via bluetooth com o Esp32, fazendo a comunicação com os sistemas de iluminação e de sensor de presença por exemplo.

## Desenvolvimento do Hardware

### Montagem

A casa foi projetada e desenhada por Pedro Henrique e Luiz Felipe, que também construíram a estrutura de cabos. A parte de software foi planejada em conjunto por todos os integrantes, mas desenvolvida por João Pedro. Além disso, o sistema do ESP32, incluindo toda a lógica de funcionamento, foi projetado exclusivamente por João Pedro.


<li><a href="Documentacao\img-cabos-casa.JPG"> Imagem Estrutura de cabos</a></li>

<li><a href="Documentacao\img-desenvolvimento-casa.JPG"> Imagem Estrutura de cabos 2</a></li>

### Desenvolvimento do Código

Foi estabelecido no projeto que seria mais fácil realizar a lógica no Esp32 e não no App Inventor, então criamos toda a lógica de envio e recebimento de sinal bluetooth. Além disso, criamos uma lógica que recebe bytes de sinal para ligar e deligar os sistemas físicos do Esp32, tudo isso integrado com regras de notificações de usuário no App Inventor.

## Comunicação entre App e Hardware

O aplicativo contém a conexão bluetooth e depois que conecta uma vez não é necessário mais fazer a reconexão, pois ele armazena os dados do bluetooth em um banco de dados do APP Inventor chamado TinyDB.

<img src="Documentacao\fluxograma-conexão.png" width="auto" height="500">