# Fask-Cook_PF
Le projet Fast Cook, le fruit de deux projets réunis:  Anti-waste Food et Foodora, l'un était plutôt orienté utilisateur et l'autre côté commerçant mais il avait un but en commun réduire le gaspillage allimentaire. 

Notre application sera fait en React Native. Fast Cook vous fera économiser de l'argent et du temps. Plus jamais tu ouvriras ton frigo en te disant "jsais pas quoi me faire à manger bon bah je vais commander", il suffit d'entrer au plus 5 ingrédients présent dans ton frigo puis grâce à notre base de données elle te ressortira des recettes faciles et simples à faire avec les ingrédients que tu auras choisis.


Base de donnée : NoSQL


## Génération des certificats
openssl genrsa -des3 -out root-ac.key 2048
openssl req -x509 -new -nodes -key root-ac.key -sha256 -days 1825 -out root-ac.pem

openssl genrsa -des3 -out dev.my-project.com.key 2048
openssl req -new -key dev.my-project.com.key -out dev.my-project.com.csr

openssl x509 -req -in dev.my-project.com.csr -CA root-ac.pem -CAkey root-ac.key -CAcreateserial -out dev.my-project.com.crt -days 1825