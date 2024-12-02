# Arduino-Unity communication example

This is a simple Unity project that communicates to an Arduino card. The card controls the state of a river blocking the way
and the speed of pressure plate timers, allowing to turn on an LED when both timers are active at the same time.  
It uses the `System.IO.Ports` serial objects provided by the .NET framework. Check that the project is using .NET 4 in the player settings in Unity !

The Arduino script is contained in the [Arduino_Controller](Arduino_Controller) folder. It cannot be moved out, otherwise the Arduino IDE will complain and force you to create the folder.

It also features an example communication via TCP/IP between a WiFi enabled ESP8266 board and a Unity script. The Arduino file is in [Arduino_Wifi](Arduino_Wifi) and the Unity side is handled by `TCPHandler.cs`.  
The Arduino echoes back what it receives on the serial port while the Unity script uses `Debug.Log`.

This was tested using the ***2022.3.9f1*** version of Unity.
