# Docker
Info generali su Docker: dalla creazione di un'immagine da Dockerfile al push su DockerHub

1) Creo una cartella di Docker files

$**mkdir DockerFiles**

2) Creo ed edito un file Dockerfile (senza estensione)

$**touch Dockerfile**

$**nano Dockerfile**

**FROM** ubuntu

**RUN** apt-get update

**CMD** ["echo", "Hello World..!"]

3) Buildo l'immagine dal Dockerfile (in questo caso il nome dell'immagine sarà "prova")

$**docker build -t prova:latest .** (devi stare all'interno della cartella dove è presente il Dockerfile)

4) Controllo che l'immagine sia stata buildata

$**docker images**

5) Effettuo il login su DockerHub

$**docker login**

6) Taggo un'immagine in modo da poterla pushare in una repo di DockerHub

$**docker tag <nome_immagine> <nome_utente>/<nome_repository>**

7) Push di un'immagine su DockerHub

$**docker push <nome_utente>/<nome_repository>**
