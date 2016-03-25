# Semaforo-Cruzamento
Arduino UNO


//PROJETO SEMAFORO CRUZAMENTO


//SEMAFORO 1
#define LED_VERMELHO 12
#define LED_AMARELO 7
#define LED_VERDE 2


//SEMAFORO 2
#define LED_VERMELHO_2 11
#define LED_AMARELO_2 8
#define LED_VERDE_2 3

void setup() {

 //DEFININDO PINOS SEMAFORO 1
 pinMode(LED_VERMELHO,OUTPUT);
 pinMode(LED_AMARELO,OUTPUT);
 pinMode(LED_VERDE,OUTPUT);

 //DEFININDO PINOS SEMAFORO 2
 pinMode(LED_VERMELHO_2,OUTPUT);
 pinMode(LED_AMARELO_2,OUTPUT);
 pinMode(LED_VERDE_2,OUTPUT);
 
 //DEFININDO ESTADO INICIAL SEMAFORO 1
 digitalWrite(LED_VERMELHO,LOW);
 digitalWrite(LED_AMARELO,LOW);
 digitalWrite(LED_VERDE,LOW);

 //DEFININDO ESTADO INICIAL SEMAFORO 2
 digitalWrite(LED_VERMELHO_2,HIGH);
 digitalWrite(LED_AMARELO_2,LOW);
 digitalWrite(LED_VERDE_2,LOW);

}

void loop() {
  digitalWrite(LED_VERMELHO,HIGH);

  delay(5000);

  digitalWrite(LED_VERMELHO,LOW);
  digitalWrite(LED_VERDE,HIGH);
  digitalWrite(LED_VERMELHO_2,HIGH);

  delay(6000);

  digitalWrite(LED_VERDE,LOW);
  digitalWrite(LED_AMARELO,HIGH);

  delay(4000);

  digitalWrite(LED_AMARELO,LOW);
  digitalWrite(LED_VERMELHO,HIGH);
  digitalWrite(LED_VERMELHO_2,LOW);
  digitalWrite(LED_VERDE_2,HIGH);

  delay(6000);
  digitalWrite(LED_VERDE_2,LOW);
  digitalWrite(LED_VERMELHO,HIGH);
  digitalWrite(LED_AMARELO_2,HIGH);

  delay(4000);
  digitalWrite(LED_AMARELO_2,LOW);
  digitalWrite(LED_VERMELHO_2,HIGH);
  
  

}
