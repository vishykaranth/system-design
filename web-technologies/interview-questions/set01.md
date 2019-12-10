## What happens when you type in a URL (google.com)
- Is a deceptive question commonly asked in tech interviews. 
- If you look online, there are many very detailed resources but few concise explanations of how a web browser, a server, 
- and the general internet work together.

### How it works 
- You enter a URL into a web browser
- The browser looks up the IP address for the domain name via DNS
    - The browser sends a HTTP request to the server
    - The server sends back a HTTP response
    - The browser begins rendering the HTML
- The browser sends requests for additional objects embedded in HTML (images, css, JavaScript) and repeats steps 3-5.
- Once the page is loaded, the browser sends further async requests as needed.

### Examples 
- When you type “google.com” into your browser the first thing that happens is a Domain Name Server (DNS) matches “google.com” to an IP address. 
    - Then the browser sends an HTTP request to the server and the server sends back an HTTP response. 
    - The browser begins rendering the HTML on the page while also requesting any additional resources such as CSS, JavaScript, images, etc. 
    - Each subsequent request completes a request/response cycle and is rendered in turn by the browser. 
    - Then once the page is loaded some sites will make further asynchronous requests.
- If I were asked to explain further I might start talking about how the server and browser connect via TCP. 
    - And we could discuss encryption via https, too.

## TCP v/s UDP 

- TCP (Transmission Control Protocol) is the most commonly used protocol on the internet. 
    - It is a connection-oriented stream over an IP network that guarantees all sent packets reach the destination in the correct order.
- A TCP handshake or 3 way handshake occurs between the client and server where the client sends a SYNC (synchronize) request, 
    - the server sends back and an ACK (acknowledgment) and sync, 
    - and then finally the client sends an ACK back.
- Once the TCP Handshake is complete, 
    - the client and server exchange data 
        - (with an ACK after every packet sent, to confirm that the packet safely reached it’s destination with the correct checksum). 
    - Once the client and server are done, the handshake is finished and is closed.
- TCP must receive acknowledgment packets from the sender and automatically re-sends any transmissions loss. 
    - This causes delays and makes it slow.
- UDP (User Datagram Protocol) is a connection-less protocol that is datagram oriented. 
    - The only guarantee is the single datagram, which can arrive out of order or not at all. 
    - UDP is more efficient than TCP 
    - and used for real-time communication (audio, video) where a little percentage of packet loss rate is preferable to the overhead of a TCP connection.

### Quick Takeaways
- TCP is reliable, UDP is unreliable
- TCP is stream oriented, UDP is message oriented
- TCP is slower than UDP, but UDP has some signal loss