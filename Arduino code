#include<Servo.h>
Servo s1;
int led1=7;
int led2=8;
int pos;
int data;
void setup() {
  // put your setup code here, to run once:
  Serial.begin(9600);
s1.attach(9);
pinMode(7,OUTPUT);
}

void loop() {
  // put your main code here, to run repeatedly:
  while(Serial.available()>0)
{
  data=Serial.read();
  Serial.println(data);
  if(data=='A')
  {
    digitalWrite(7,HIGH);
    for(pos=0;pos<=180;pos+=2)
 {
   s1.write(pos);
 delay(10);
 }
        for(pos=180;pos<=360;pos+=2)
 {
   s1.write(pos);
 delay(10);
      digitalWrite(8,HIGH);
 }

  }
    if(data=='B')
  {
    digitalWrite(7,LOW);
    digitalWrite(8,LOW);

    for(pos=180;pos>=0;pos-=1)
   {
   s1.write(pos);
   delay(5);
   }


  }  
}
}  
