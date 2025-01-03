# Milepael 2
Midjo Grand Prix 1970 is a fast-paced racing game developed for the Raspberry Pi SenseHat. Play as Arne Midjo and race in the speedy car "Hype One", navigating through gates while managing your fuel levels. The challenge is to keep your fuel up by collecting fuel cans scattered on the track.

The game features simple gyro-based controls: tilt the Raspberry Pi to steer the car. With multiplayer support, you can use a phone, tablet, or PC as a controller and compete for high scores.

Points are earned by passing gates, and fuel is consumed as you race. Collect fuel cans to stay in the game, and advance through levels with increasing difficulty. Running out of fuel means "Game Over," but you can restart by pressing the joystick. Win the game by reaching 32 points on level 3!


## Starting the game
### Without multiplayer
```console
python3 Milepael_2.py
```
### With multiplayer
```console
sudo python3 Milepael_2.py host
```
### Multiplayer interface endpont
https://pearpie.is-very-sweet.org/site/index.html


## Generating SSL certificates
### With Open SSL (slow)
[Stack Overflow Post](https://stackoverflow.com/questions/29458548/can-you-add-https-functionality-to-a-python-flask-web-server)
```console
openssl req -x509 -newkey rsa:4096 -nodes -out cert.pem -keyout key.pem -days 365
```
### With certbot (fast)
[Tutorial](https://pimylifeup.com/raspberry-pi-ssl-lets-encrypt/)
```console
sudo apt-get update
sudo apt-get upgrade
sudo apt-get install certbot
certbot certonly --standalone -d example.com -d www.subdomain.example.com
sudo ls /etc/letsencrypt/live/example.com/
```
