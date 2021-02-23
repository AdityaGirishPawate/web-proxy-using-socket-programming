# web-proxy-using-socket-programming
This repo tells contains the code to run the proxy server for your web browser using python. Just run the run.py on the terminal with appripriate IP address and the proxy server will get activated. Then go to your browser and set up manual proxy with the localhost and port number 8888. Then you will connected to the internet through the proxy server.<br>
When the browser client is going to make a request for the first time. The program tries to open
a cache file named with url (filename to be “www.google.com” for google site), and raises an IO
Exception because it does not exist. Then, the proxy needs to forward requests to the remote
server and retrieve the webpage. The proxy will then receive a file from the server, cache it to
tmpFile, and forward it to the client.<br>
The next time the client requests the same file, instead of having to query to remote
server, your proxy will simply read the appropriate webpage from its cache file in the local
directory and send it directly back to the client.<br>
Note that the proxy server keeps a server socket the whole time to receive connection from
browser client and send response to it. But if there is no cache, it needs to create a new client
socket to connect to the remote server and retrieve the webpage.
<br>

