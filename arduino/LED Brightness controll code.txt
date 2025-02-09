// C++ code
//
int potpin=A0;
int potvalue;
int led=5;
int ledv;
void setup()
{
Serial.begin(9600);
pinMode(potpin,INPUT);
  pinMode(led,OUTPUT);
}

void loop()
{
  potvalue=analogRead(potpin);
  ledv=map(potvalue,0,1023,0,255);
  analogWrite(led,ledv);
  Serial.print("Led Brightness:    ");
  Serial.println(ledv);
}