Variable rust
https://jimskapt.github.io/rust-book-fr/ch03-01-variables-and-mutability.html


let x = 5;

mutable:
let mut x = 5;

constante:
const TROIS_HEURES_EN_SECONDES: u32 = 60 * 60 * 3;

masqué:
let x =5;
let x= x+2; => valable dans un bloc, apres reprend la valeur initiale et permet le changement de type:
let espaces = "   ";
let espaces = espaces.len();



