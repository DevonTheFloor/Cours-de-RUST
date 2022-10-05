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
Chaque variante signée peut stocker des nombres allant de −(2n − 1) à 2n − 1 − 1 inclus (cf tableau dans la doc: [tableau](https://jimskapt.github.io/rust-book-fr/ch03-02-data-types.html#types-de-nombres-entiers)   
Voir aussi les littéraux d'entier dans la doc.   
   
Pour eviter le "rebouchage" du dépassement d'entier à la compilation de publication ( drapeau: ```--release``` ):   

    - Enveloppez les opérations avec les méthodes ```wrapping_*```, comme par exemple wrapping_add   
- Retourner la valeur None s'il y a un dépassement avec des méthodes ```checked_*```   
- Retourner la valeur et un booléen qui indique s'il y a eu un dépassement avec des méthodes ```overflowing_*```   
- Saturer à la valeur minimale ou maximale avec des méthodes ```saturating_*```   
   
##### Types de nombre à vigule flottante   
[voir dans la doc](https://jimskapt.github.io/rust-book-fr/ch03-02-data-types.html#types-de-nombres-%C3%A0-virgule-flottante)   
   

Les types de flottants en Rust sont les ```f32``` et les ```f64``` qui est le type par défaut, ex:   
```rust
fn main() {
    let x = 2.0; // f64

    let y: f32 = 3.0; // f32
}
```   





