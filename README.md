# FishFeeding-starter-Project
Motivation: Want to know if the fish has been fed in the last X - Hours. 
Approach:
Node-Red-Flow involving mqtt and node-red context variables. 
ESP32 that listens to its own topic and blinks an LED thats strapped to the fish tank

Two groups. Group one: 
A button that you press after you fed the fish (later the button will actually feed the fish)
it sets the context variable of the flow (lastFed) to NOW

Group two: 
Checking the variable "lastFed", display it in our Node-red UI, beautifying it so its not just a boring number being displayed instead, also checking if its time to feed already. put the payload for the mqtt and the appropriate message in the message container. (blink once or blink twice, for the LED thats strapped to the fish tank making a visual indicator for kids to understand wether fishy needs to be fed or not)

Sceenshots
![image](https://github.com/user-attachments/assets/1c6ad450-3d9f-4504-b775-674834ea0680)
Image: The flow. note that now after setting when the fish last has been fed, updating the display comes immediately which makes it very satisfying to play with

![image](https://github.com/user-attachments/assets/8ad89da5-19bc-4479-8beb-b4063210f648)
Image: what you can have as a dashboard. Strap it to the fish tank aswell and you already have your button

![image](https://github.com/user-attachments/assets/7ad39835-cd82-4eb4-afea-18d1a46fb848)
Image: note to myself on how to get the current date in milliseconds, saving a node-red context variable

![image](https://github.com/user-attachments/assets/53560adf-ef7a-4528-99b6-efb3f0adbcf0)
Image: checking the value, returning it in a more human readable manner (hours in decimal instead of milliseconds...)
