# Async communication Example with Reference Workshop Net

## Description

Este repositorio contem um modelo, constituido por redes Reference Workshop, que foi apresentaado no papaer cientifico  intitulado *Leveraging High-Level Petri Nets for Cyber-Physical Systems Development* proposto para PNSE'24 - International Workshop on Petri Nets and Software Engineering, Geneva, Switzerland, June 24-25, 2024.

Este modelo demonstra como implementar comunicação biderecional assincrona recorrendo ao protocolo MQTT.

## Descrição do caso a modelar

Idializou-se um cenario composto por comportas e um botão de panico. 
As comportas estão inicialmente abertas e passam ao estado fechado e permanecem nesse ciclo até que o botõ de panico seja presionado e então as portas param o seu movimento e permanecem imoveis até que seja resposto o seu movimento no sentido anterior ou oposto.

## Descrição do modelo
O modelo é composto pelas seguintes redes:

* **Controller -** Rede que que apresenta o estado dos *Cyber Physical Systems* (CPS)
* **Gate -** Rede que representa a contraparte digital de uma CPS. Esta CPS representa uma contraporta.
* **Button -** Rede que reporesenta a contraparte digital de uma CPS que haje como botão de panico.
* **Communiator -** Rede que instancia as classe MQTT client e possibilita a comunicação entre as Redes da parte logica do CPS e a su contraparte.
* **mqtt_message_receiver -** Rede utilizada como observer na classe Java para *receber* as mensagens e por sincronia entre transições passa-la para as outras redes.


