# projekt-led
Reprezentacja dźwięku na linii diod LED
Projekt wykonany będzie na płytce arduino.
Dzięki podłączeniu do układu modułu mikrofonu, 8 diod LED świeci w rytm muzyki
# Wykorzystane elementy:
* 8 diod LED, po 2 czerwone, żółte, zielone i białe
* 8 rezystorów 220ohm
* płytka arduino
* moduł mikrofonu (można zrobić samemu, ale popsuł się wzmacniacz)
* sporo przewodów
* płytka prototypowa

# KOD
> int lPin1= 13; //dioda 1. na porcie 13 płytki
> int lPin2= 12; //dioda 2. na porcie 12 płytki
> int lPin3= 11; //dioda 3. na porcie 11 płytki
> int lPin4= 10; //dioda 4. na porcie 10 płytki
> int lPin5= 9; //dioda 5. na porcie 9 płytki
> int lPin6= 8; //dioda 6. na porcie 8 płytki
> int lPin7= 7; //dioda 7. na porcie 7 płytki
> int lPin8= 6; // dioda 8 na porcie 6 płytki
> int sensorPin= A0; //port analogowy, na który podajemu muzykę z mikrofonu
> int val = 0;

> void setup(){
  > pinMode(lPin1, OUTPUT); //ustawiamy piny jako wyjście
  > pinMode(lPin2, OUTPUT);
  > pinMode(lPin3, OUTPUT);
  > pinMode(lPin4, OUTPUT);
  > pinMode(lPin5, OUTPUT);
  > pinMode(lPin6, OUTPUT);
  > pinMode(lPin7, OUTPUT);
  > pinMode(lPin8, OUTPUT);
  > pinMode(sensorPin, INPUT); 
  > Serial.begin (9600);
> }
  
> void loop (){
  > val =analogRead(sensorPin);
  > Serial.println (val);
  
  
  > //dioda  1
  > if (val >= 125) {
    > digitalWrite(lPin1, HIGH); 
  > }
  > else {
    > digitalWrite(lPin1, LOW);
  > }

  > //dioda 2
   > if (val >= 375) {
    > digitalWrite(lPin2, HIGH);
  > }
  > else {
    > digitalWrite(lPin2, LOW);
  > }

   > //dioda 3
   > if (val >= 505) {
    > digitalWrite(lPin3, HIGH);
  > }
  > else {
    > digitalWrite(lPin3, LOW);
  > }

  > //dioda 4
  > if (val >= 635) {
    > digitalWrite(lPin4, HIGH);
  > }
  > else {
    > digitalWrite(lPin4, LOW);
  > }

  > //dioda 5
  > if (val >= 760) {
    > digitalWrite(lPin5, HIGH);
  > }
  >  else {
    > digitalWrite(lPin5, LOW);
  > }

  > //dioda 6
  > if (val >= 885) {
    > digitalWrite(lPin6, HIGH);
  > }
  > else {
    > digitalWrite(lPin6, LOW);
  > }

  > //dioda 7
  > if (val >= 980) {
    > digitalWrite(lPin7, HIGH);
  > }
  > else {
    > digitalWrite(lPin7, LOW);
  > }

  > //dioda 8
  > if (val >= 1000) {
    > digitalWrite(lPin8, HIGH);
  > }
  > else {
    > digitalWrite(lPin8, LOW);
  > }
> }
