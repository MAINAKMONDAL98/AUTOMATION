# AUTOMATION
HOW TO MAKE AUTOMATIC ELECTRIC CONTROLLER BY USING PIR SENSOR AND RELAY IN ARDUINO PLATFORM
CODE:
#define  PIR_OUTPUT 10
byte relay_pin = 8 ;
byte  PIR_outputVal ;

void setup(){
  pinMode(relay_pin,OUTPUT);
pinMode(PIR_OUTPUT, INPUT);
  Serial.begin(9600);
}
void loop(){
   PIR_outputVal = digitalRead( PIR_OUTPUT);
   //Serial.println( PIR_outputVal);
//delay(100);
if( PIR_outputVal ==  HIGH) 

// reading the data from the pir sensor
{
 digitalWrite(8,  LOW);
 Serial.println("motion detected");
 delay(10000);
}
else {
 digitalWrite(8, HIGH);
 //
  Serial.println("scanning");
  
}//delay(10000);
}
