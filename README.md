# Cours de Rust   
Ceci n'est qu'une fiche patique où est annoté l'essentiel. Pour tous les détails merci de vous reporter au [BOOK](https://doc.rust-lang.org/book/) ou a sa version non officielle française: [LE LIVRE](https://jimskapt.github.io/rust-book-fr/title-page.html).   
   
# SOMMAIRE:   
[Installation](#installation-linux)   
[Initiation](#initiation)   
[Concepts de bases](#concepts-courants-de-programmation)   
   
   

# Installation (linux)   
   
```$ curl --proto '=https' --tlsv1.2 https://sh.rustup.rs -sSf | sh```
   
Mettre à jour:
```rustup update```   
   
Désinstaller:   
```rustup self uninstall```   
   
Accéder à la *Documentation* en local:
```rustup doc```   
## Cargo le paquet manager   
   
Créer un projet:
```cargo new projet_rust```  
Compiler du code:
```cargo build```   
et ainsi verifier les erreurs.   
   
Compiler et lancer:   
```cargo run```   
   
Compiler sans produire de binaire juste pour la verif:   
```cargo check```   
   

# Initiation   
Merci de vous referer au projet plus_moins dans ce même dépot.   
   
# Concepts courants de programmation   
   

### Variable rust   
let x = 5;   
   
Immuable par défaut, on peut les rendre mutable:   

let mut x = 5;   
Ansi x peut être réaffecté:   

x = 7;   
   
Les variables peuvent être masquées:   

let x =5;   
Application du masque:   
let x= x+2; => valable dans un bloc, apres reprend la valeur initiale et permet le changement de type:   

let espaces = "   ";   

let espaces = espaces.len();   
   
   
### Constante   

const TROIS_HEURES_EN_SECONDES: u32 = 60 * 60 * 3;   
Nommage: snake case majuscule + type.   
   
### Types de données   
   
On verra deux catégories de type de données: **scalaire** et **composés** .   
   
#### Type scalaire   
Quatre types de scalaire: - nombre entier   
- à virgule flottante   
- chaine de caractère   
- booléens   
   
##### Entier   
Noté u (unsign) ou i (integer) de 8 à 128 bits, ex: u32.   





