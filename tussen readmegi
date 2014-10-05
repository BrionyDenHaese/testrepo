#Cheat-sheets Briony Den Haese

##1) Initiele setup voor bestanden via terminal up te loaden op bitbucket
```
mkdir /path/to/your/project 
```
*Hier kan je gewoon een map aanmaken om vanuit deze map te werken*
```
cd /path/to/your/project
git init
git remote add origin --link naar bitbucket die hier nodig is, bij mij was dit https://BrionyDH@bitbucket.org/sebastienpattyn/labo-taken.git--
```


Het volgende is om een klein bestand te maken en dit up te loaden:
```
echo "Briony Den Haese" >> contributors.txt
git add contributors.txt
git commit -m 'Initial commit with contributors'
git push -u origin master
```
##2) Een bestand aanpassen in bitbucket
```
echo "Sebastien Pattyn" >> contributors.txt 
```
*Dit is gewoon een voorbeeld van een aanpassing van een bestand, je kan ook gewoon in de folder een bestand zetten en dit uploaden*
```
git add contributors.txt
git commit -m '*Gekozen tekst bij commit*'
git push -u origin master
```
##3) SSH pubic en private key genereren

```
ssh-keygen -t rsa -C "comment"
```
* Als je in de standaard repository deze key wil opslaan, 'enter' nogmaals, zoniet geef zelf een repository in. Geef daarna ook een passphrase op.
```
cat /root/.ssh/id_rsa.pub
```
* Dit is de repository waar de key bij is gestored, dit kan mogelijks op een andere plaats zijn.
* Kopieer deze key naar GitHub en BitBucket bij de SSH-keys
* Vervolgens testen we de verbinding
```
ssh -T git@github.com
ssh -T git@bitbucket.org
```

Als dit een foutmelding geeft bij een van de 2 moet er eerst iets anders gebeuren:
```
ssh-add /home/briony/.ssh/id_rsa
```
* Dit is terug de repository waar de keys zich bevinden, en hierbij zal er opnieuw naar de passphrase gevraagd worden, wanneer deze juist is ingegeven zou de bovenstaande test van de verbinding wel moeten lukken, en zou de SSH keypair juist tot stand moeten gebracht zijn

##4) Verbinding met github maken via terminal

* Om te starten moet je op je eigen pc een directory aanmaken, waarin je de bestanden van github zult plaatsen en synchroniseren. Maak daarna een klein tekstbestand aan, om op te volgen of het communiceren met github lukt.
```
mkdir ~/MyGithubProject
cd ~/MyGithubProject
touch test.txt
```
* Van hieruit start een opeenvolging van enkele commando's:
```
git status
git add test.txt
git commit -m "Add test.txt"
git remote add origin https://github.com/username/mygithubproject.git
git remote -v
git push -u origin master
```
* als er een foutmelding wordt gegeven na de *git push*, typ dan *git remote rm origin*, en start opnieuw met de commando's vanaf *git remote add origin*

##5) Bestanden binnenhalen van github:

```
git pull remote master
```
