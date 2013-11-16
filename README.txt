SE 3314B - Assignment 1 - Chris Wyant -250517111
-----------------------------------------------------
Note: This assignment does not use any external modules to the standard node libraray, therefore a package.json file is not required to run the application.

To Run:
To run the server application navigate to the  assignment1_cwyant folder in the terminal and run node server.js

Server Components:
server.js - the root application file. This file is run using the node server.js command and is responsible for loading the RTSP module and setting up the TCP 
			server that the client connects with to send RTSP commands.
			
RTSP.js - called in the server.js file, the RTSP module is responsible for parsing client requests and responding accordingly. RTSP also makes use of the RTP.js module.

RTP.js - The RTP module implements the actual streaming. For example, pressing the play button will parse the video file and send it over UDP to the client at a 100ms interval
		 The RTP module also contains support to handle multiple clients through the clientList array.
		 
RTPpacket.js - This module is responsible for wraping the payload with a 12-byte header.