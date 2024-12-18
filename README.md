# OpenVPN-DCompose
Docker Compose release of Open VPN Access Server <BR>
Very simple Docker compose file to ensure you can just pull this and get up and running with minimum effort.<BR>
Ensure you've set your network appropriatly re firewall ports.<BR>
Grab the docker-compose.yml <BR>
 git clone https://github.com/ramraider2k6/OpenVPN-DCompose.git<BR>
 cd OpenVPN-DCompose <BR>
Then start it depending on what release of docker compose you have<BR>
 docker compose up -d <BR>
Un-comment line 3 and docker-compose up -d<BR>
Have fun using TLS 1.3<BR>
Once the container has started you'll need to find the auto-generated password to login.<br>
 docker ps|grep openvpn-as<br>
 docker logs -f XX |grep pass <br>
Where XX is the container ID<br>
The Username=openvpn<br>
