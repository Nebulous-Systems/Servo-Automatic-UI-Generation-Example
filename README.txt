Instructions to run the Servo Motor example for automatic UI building:

1. Download RIP-LabView server from https://github.com/Nebulous-Systems/rip-server_labview

2. Follow the instructions in the RIP-LabView server readme file to run the server and test 
   if it is working.

3. Place the "SimEx DC Motor Position Control with PID.vi" file in 
   C:\Program Files\National Instruments\LabVIEW 2020\examples\Control and Simulation\Simulation\Controllers\ (or
   the equivalent path in Mac OS).

4. Replace the mygadgets_conf.json file you got when downloaded the RIP server by the one in the RIP Server
   folder here. If using Mac OS, replace the path to the VI with the corresponding one.

5. If you placed the .vi file in a different folder, you would need to modify the mygadgets_conf.json file
   to update the path to the .vi file.

6. In order to check out whether everything is set up correctly, you can open a web browser and type one of this,
   depending on which port you are running your LabView services:
   http://localhost:8001/RIP?expId=Motor
   http://localhost:8080/RIP?expId=Motor
   http://localhost:8081/RIP?expId=Motor
   If you get a json text response, then everything is fine. If you get any type of HTTP error, then something 
   is wrong.

7. Stop the RIP server and open Servo_Automatic_UI.xhtml with a browser. Only an image of a motor disc will be
   displayed. 

8. Close the web browser.

9. Run the RIP server once again and open the .xhtml file. The app UI will now show all the controls and indicators
   required to monitor and operate the .vi model.

10. You can try hiding, deleting or adding new controls and indicators in the .vi file and refreshing the webpage
   (no need to close the browser and open it again) to see how the UI is updated automatically.


Requirements:

1. LabVIEW 2020 or above.

2. Port 8001, 8080 or 8081 must be free to run the service.
