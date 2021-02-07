# FastCook

 Le projet Fast Cook, le fruit de deux projets réunis:
 Anti-waste Food et Foodora, l'un était plutôt orienté utilisateur et l'autre côté commerçant mais il avait un but en commun réduire le gaspillage allimentaire. 

 Notre application sera fait en React Native. Fast Cook vous fera économiser de l'argent et du temps. 
 Plus jamais tu ouvriras ton frigo en te disant "je sais pas quoi me faire à manger, bon bah je vais commander". 
 Pour cela, il suffit d'entrer au plus 5 ingrédients présent dans ton frigo,
 puis grâce à notre base de données elle te ressortira des recettes faciles et simples à faire avec les ingrédients que tu auras choisis.

## Description
 
 Sécurisation pour FastCook :
 Cette partie gère la sécurisation des connexions via Google et Facebook ou Email.

## Generate certificate & key

 openssl genrsa -des3 -out root-ac.key 2048 --seclevel-1 
 openssl req -x509 -new -nodes -key root-ac.key -sha256 -days 1825 -out root-ac.pem
 openssl genrsa -out dev.my-project.com.key 2048
 openssl req -new -key dev.my-project.com.key -out dev.my-project.com.csr
 openssl x509 -req -in dev.my-project.com.csr -CA root-ac.pem -CAkey root-ac.key -CAcreateserial -out dev.my-project.com.crt -days 1825 -sha256

## Installation
 
 Utilisez [Docker](https://www.docker.com/get-started/) pour installer FastCook
 Depuis la racine du projet:
 docker-compose build
 docker-compose up

## Usage
 
 Ajouter le certificat de FastCook aux certificats acceptés par votre naviagateur
 Connexion via [localhost](https://localhost/) 
 
 
 ## Do not work
 
 Lors de la redirection du login le callback ne nous permet pas de se log sur le https après diverses recherches
 nous n'avons pas pu trouver une solution, malgré les chagements de URL du callback.
 
 http://localhost:3000/callback -> celui ci nous sert à faire le lien avec le serveur node 
 

## Authors and acknowledgment

 Tristan Gualini
 Basile Lequeux
 Jennifer Chan
 Benjamin Dembin
