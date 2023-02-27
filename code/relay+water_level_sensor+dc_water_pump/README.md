this code is for automatic water pumping into water tank. 


if(digitalRead(FLOAT_SENSOR) == LOW) //water levels low -> turns on dc pump
  {
    // turn LED on:
    digitalWrite(LED, HIGH); //led indicator for low water levels
    digitalWrite(RELAY_PIN, HIGH); //switch relay on till water level rises
    delay(5000); //after raising and sensor sending signal to switch relay off, pump will continue pumping water for additional 5 seconds 
    }  
     else 
  {
    digitalWrite(LED, LOW); //turns off low water level indicator (our led)
    digitalWrite(RELAY_PIN, LOW); //turns off relay
  
  } 
  
} 


this code is no way near good, i will update it 
if u want this code to work while performing multiple tasks u will have to use millis() function in order not to fuck up other delay() functions
