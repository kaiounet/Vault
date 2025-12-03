# Le modele de reference OSI 

![OSI-Model](/home/yunus/Documents/OSI-Model.gif)

Gif link if not locally not available <a href ="https://media.geeksforgeeks.org/wp-content/uploads/20241111182857579134/OSI-Model.gif">OsiModel</a>

grab it locally 

Note:

NetworkLayer --> Router

DataLinkLayer --> Switch

PhysicalLayer --> Cable + Wi-fi



## Couche physique

Specification mecanique et electrique des interfaces

- Voltages pour representer 0 et 1
- Duree d'un bit

## Couche Liason

- Decouper les sequences de bits en paquets (appeles trames) (avec le code CRC)
  - Reconneaitre les frontieres entre les trames
- Detecter et corriger des erreurs de transmission
- Regulation de flux
- Si la liaison physique est tres fiable, la couche liaison n'  pas besoin d'utiliser des mecanismes supplementaires pour corriger les erreurs.

## Couche Reseau

- Acheminement de paquets entre la source et le destinaire
  - Service soit oriente connexion soit sans connexion
- Adressage des noeuds du reseaux
- Interconnexion de reseaux heterogenes
  - Fragmentation de paquets
  - Conversion d'adresses

## Couche Transport

#### Transmission de bout en bout, entre les terminaux (sender + receiver) 

- Optimiser le transport des donnees
  - Ne pas surcharger le recepteur ou le reseau
  - Decouper les donnees de la couche superieure en unites plus petites (Segments)
- Service fiable (TCP)
  - Avec etablissement d'une connexion
  - S'assurer que tous les paquets arrivent correctement au destinataire
- Service non fiable (UDP)
  - Sans connexion, plus simple
  - Ne retransmet pas les paquets perdus

## Couche Session

Elle etablit la session, faire la gestion de la session et fermer la session

Si la connexion de la couche transfert est interrompue, la session la retablit et reprend le transfert

## Couche Presentation ( ! Importante )

#### S'occupe de la syntaxe des donnees transmises

- Negociatiion de la syntaxe de transfert
  - ASCII, Unicode, ...
  - Entieres sur 16 ou 32 bit
- Conversion entre la representation utilisee par les terminaux et la syntaxe de transfert
  - Assure que des systemes terminaux utilisant des representations differentes se comprennent

## Couche Application

#### Protocoles des applications

- De nombreaux protocoles qui realisent des services a travers le reseau
  - Exemples :
    - WWW -> protocole HTTP
    - E-MAIL -> protocole SMTP
    - Telephonie sur Internet -> protocole SIP
