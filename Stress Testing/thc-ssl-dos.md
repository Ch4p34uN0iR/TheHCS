# THC-SSL-DOS
## TheHCS / @NitescuLucian / https://www.thc.org/

Establishing a secure SSL connection requires 15x more processing
power on the server than on the client.

THC-SSL-DOS exploits this asymmetric property by overloading the
server and knocking it off the Internet.

This problem affects all SSL implementations today. The vendors are aware
of this problem since 2003 and the topic has been widely discussed.

This attack further exploits the SSL secure Renegotiation feature
to trigger thousands of renegotiations via single TCP connection.

Comparing flood DDoS vs. SSL-Exhaustion attack:

A traditional flood DDoS attack cannot be mounted from a single DSL connection.
This is because the bandwidth of a server is far superior to the
bandwidth of a DSL connection: A DSL connection is not an equal opponent to
challenge the bandwidth of a server.

This is turned upside down for THC-SSL-DOS: The processing capacity for
SSL handshakes is far superior at the client side: A laptop on a DSL
connection can challenge a server on a 30Gbit link.

Traditional DDoS attacks based on flooding are sub optimal: Servers are
prepared to handle large amount of traffic and clients are constantly
sending requests to the server even when not under attack.

The SSL-handshake is only done at the beginning of a secure session and
only if security is required. Servers are _not_ prepared to handle
large amount of SSL Handshakes.

The worst attack scenario is an SSL-Exhaustion attack mounted from
thousands of clients (SSL-DDoS).


Tips & Tricks for whitehats

1. The average server can do 300 handshakes per second. This would require
   10-25% of your laptops CPU.
2. Use multiple hosts (SSL-DOS) if an SSL Accelerator is used.
3. Be smart in target acquisition: The HTTPS Port (443) is not always the
   best choice. Other SSL enabled ports are less likely to use an SSL
   Accelerator (like the POP3S, SMTPS, ...  or the secure database port).

Usage:
./thc-ssl-dos 127.3.133.7 443
Handshakes 0 [0.00 h/s], 0 Conn, 0 Err
Secure Renegotiation support: yes
Handshakes 0 [0.00 h/s], 97 Conn, 0 Err
Handshakes 68 [67.39 h/s], 97 Conn, 0 Err
Handshakes 148 [79.91 h/s], 97 Conn, 0 Err
Handshakes 228 [80.32 h/s], 100 Conn, 0 Err
Handshakes 308 [80.62 h/s], 100 Conn, 0 Err
Handshakes 390 [81.10 h/s], 100 Conn, 0 Err
Handshakes 470 [80.24 h/s], 100 Conn, 0 Err


### Source:
* https://www.thc.org/
* https://thehackerschoice.wordpress.com/2011/10/24/thc-ssl-dos/
