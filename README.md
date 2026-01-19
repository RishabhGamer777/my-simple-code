# my-simple-code
nothing
int ldrPin = A0;  
int ldrValue = 0;

int ledPin1 = 8;
int ledPin2 = 9;

void setup() {

    Serial.begin(9600);

    pinMode(ledPin1, OUTPUT);

    pinMode(ledPin2, OUTPUT);

}

void loop() {
 


  ldrValue = analogRead(ldrPin);  

  Serial.print("LDR Value: ");

  Serial.println(ldrValue);

  delay(100);   

  if (ldrValue <= 500) {

    analogWrite(ledPin1, 150); 

    analogWrite(ledPin2, 150);

    delay(100);

    analogWrite(ledPin1, 0); 

    analogWrite(ledPin2, 0);

    delay(100);
  }

  else {

    analogWrite(ledPin1, 0); 

    analogWrite(ledPin2, 0);

  }

}


