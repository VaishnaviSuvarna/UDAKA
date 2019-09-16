//include the library code:
#include<LiquidCrystal.h> 
#include<dht.h> 
  dhtDHT; 
 #define DHT11_PIN8 
//initialize the library with the numbers of the interface pins 
LiquidCrystal lcd(12,11,5,4,3,2); 
Void setup() 
{
// set up the LCD's number of columns and rows: 
lcd.begin(16,2); 
//PrintamessagetotheLCD.
lcd.print("COLDWATER"); 
}
Void loop(){ 
{
//set the cursor to column0, line1 
//(note:line1isthesecondrow,sincecountingbeginswith0):
lcd.setCursor(0,1);
 int chk=DHT.read11(DHT11_PIN);
 lcd.print("Tempin`c="); 
 lcd.print(DHT.temperature,1); 
delay(2000); 
//print the number of seconds since reset:
lcd.print(millis()/1000);
 }
} 
