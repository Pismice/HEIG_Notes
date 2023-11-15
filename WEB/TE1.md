# 1. Introduction
## Layers (Internet Protocol Suite)
- Application Layer (HTTP, FTP, SSH, SMTP, IMAP, Telnet, ...)
- Transport Layer (TCP, UDP, ...)
- Internet Layer (IP, ICMP, ...)
- Link Layer (ARP, MAC, Ethernet, Wifi, DSL, Fibre, ...)
## DNS
Utilise TCP
La résolution de domaine se fait de manière *recursive*, on commence par le TLD (ex: .com) qui va lui aller faire "example", puis "www", ...
Chaque zone NDS contient la liste des adresses IP associé au nom de domaine (Ressource Records)
**Differentes commandes:**
- nslookup heigé-vd.ch
- host 91.198.174.192
- whois heig-vd.ch
## WWW
HTTP: Transfert de données entre client-serveur
HTML: Format de publication de documents WEB
## URL
![](images/Pasted%20image%2020231026001013.png)
Les query sont séparés par des "&"
## HTTP
- GET: Returns the resource
- POST: Create resource
- HEAD: Returns the headers of resource
- PUT: Create/update resource
- DELETE: Deletes resource
![](images/Pasted%20image%2020231026001239.png)
# 2. HTML & CSS
## HTML
- DOCTYPE: version HTML
- html: root element
- head: metadata (titre, utf8, ...)
	- meta: infos pour les search engines et browsers
- body: tout le corps du site web
## SEO
Utiliser pour classer les différents sites WEB dans les recherches
Pour un bon SEO:
- Utiliser les bons tags
- Metadata relevant
- Bonne structuration du site (tags)
## HTML elements
**Différents attributs:**
- id
- class
- style

**Faire une liste:**
ol/ul -> li

**Faire une table:**
table -> tr -> th/td

**Faire une form**
form action="/articles" method="POST"
## HTML Entities
Permet d'afficher des *char* spéciaux (commence par & et fini par ;)
## CSS
**Différentes manières d'ajouter du CSS:**
1. Embedded avec \<style>
2. External stylesheets (link rel="stylesheet" type="text/css" href="style.css")
3. Inlined directories (\<h1 style="...">)

**Différents Selectors**
- *type* (p {})
- *id* \#myid {}
- *class* .myclass {}
- *universal* * {}
- *attribute* [attr=value] {}
- *grouped* h1, h2, h3, p {}

**Selectors ++**
![](images/Pasted%20image%2020231026005136.png)

**Combinators**
![](images/Pasted%20image%2020231026005312.png)

**Pseudo-class**
![](images/Pasted%20image%2020231026005347.png)

**Specificity (ordre du choix des règles CSS)**
1. Si inlined
2. Nb d'id
3. Nb de class, attribute, pseudo-class
4. Nb d'element et pseudo-element
### Propreties
![](images/Pasted%20image%2020231026010423.png)
### Positionning
#### Box model
utiliser calc() pour faire des calculs
![](images/Pasted%20image%2020231026010532.png)
#### Flexbox
display: flex;
flex-direction: row/column
justify-content
align-items
align-content
### Media queries
C'est comme des if en gros
![](images/Pasted%20image%2020231026011026.png)
### CSS Variables
![](images/Pasted%20image%2020231026011525.png)
![](images/Pasted%20image%2020231026011545.png)
### DOM
![](images/Pasted%20image%2020231026011642.png)
![](images/Pasted%20image%2020231026011651.png)
# 3. Foundations of Javascript
## JS Versioning
ECMAScript 6 (ES6) = ECMAScript 2015 (ES2015)
...
ECMAScript 2019 (ES2019)
...
ECMAScript 2021 (ES2021)
...
## AJAX
AJAX (Asynchronous Javascript and XML) -> permet les pages dynamiques
## Server-Side JS vs Client-Side JS
### Client-side
![](images/Pasted%20image%2020231026132555.png)
### Server-Side
NodeJS
## Types
- **Undefined**: ne peut être que *undefined*
- **Number**: Réels ou entiers (*3.14*,*42*,...)
- **Boolean**: *true* ou *false*
- **String**: Chaine de chars (*"Hello"*, *'Hello'*)
- **BigInt**: Entiers à precision arbitraire qui FINIT par *n* (*84390480934083n*)
- **Symbol**: Valeurs uniques globales (*Symbol("description)"*)
- **Null**: ne peut être que *null*
- **Object**: peut être un *object*, un *array* ou une *date* (8ème et dernier type)
typeof permet de trouver le type de l'objet à la compilation

### Symbol
Object proprety key
![](images/Pasted%20image%2020231030215843.png)
### Objects
![](images/Pasted%20image%2020231026133256.png)
### Arrays
![](images/Pasted%20image%2020231026133322.png)
![](images/Pasted%20image%2020231026134727.png)
### String
String concatenation can be done 2 ways:
1. "con" + "cat"
2. 'PI = ${Math.PI}' (AVEC ´´ obligatoires ! pas de " ")
### Generator
```
function* numberGenerator() {
  yield 1;
  yield 2;
  yield 3;
}

const generator = numberGenerator();

console.log(generator.next()); // Output: { value: 1, done: false }
console.log(generator.next()); // Output: { value: 2, done: false }
console.log(generator.next()); // Output: { value: 3, done: false }
console.log(generator.next()); // Output: { value: undefined, done: true }
```
## Optional chaining (?.)
![](images/Pasted%20image%2020231026134832.png)
## Variable declaration
var: scope = current execution context (enclosing function ou global)
let: scope = block scoped
const: scope = block scoped (immutable)
## For loops
for ... in boucle sur les PROPRIETES et non les valeurs
for ... of boucle sur les valeurs
## Functions
first-class citizens
### Declaration
![](images/Pasted%20image%2020231026135357.png)
### Higher-order functions
![](images/Pasted%20image%2020231026135510.png)
![](images/Pasted%20image%2020231026135607.png)
### Regex
2 manières d'en créer:
> const re = /ab+c/;
> const re = new RegExp("ab+c"); 

Quelques règles:
1. Literal string: /hello/ (hello mister)
2. Any char: /.oo/ (foo)
3. Char range: /[a-z]/
4. Specifi number of char: /l{2}o/ (hello)
5. Any digits: /\d/ (42)
6. Whitespace: /\s/
7. Word: /\w/
8. Alternatives: /cat|dog/
Exemple du cours:
![](images/Pasted%20image%2020231026135803.png)
# 4. Object-Oriented JavaScript
## Objects methods
![](images/Pasted%20image%2020231026144527.png)
![](images/Pasted%20image%2020231026162812.png)
## Prototypes
Les prototypes sont également des objets !!!
Si on crée un object sans class il pointera directement sur "proto de Object"
![](images/Pasted%20image%2020231026144902.png)
![[Pasted image 20231010145521.png]]
### Constructeur
![](images/Pasted%20image%2020231026145651.png)
![](images/Pasted%20image%2020231026145733.png)
### Heritage
![](images/Pasted%20image%2020231026145931.png)
### Override prototype
Ici on va override le proto de Array
![](images/Pasted%20image%2020231026150222.png)
## Object-oriented JS
Introduit avec ECMAScript2015
Il ne s'agit que d'un sucre syntaxique les prototypes
Basic exemple:
![](images/Pasted%20image%2020231026151012.png)
### static
![](images/Pasted%20image%2020231026151106.png)
### private
![](images/Pasted%20image%2020231026151120.png)
### getters and setters
![](images/Pasted%20image%2020231026151150.png)
### species
Permet de créer un nouvel objet du même qu'un objet existant
![](images/Pasted%20image%2020231026151725.png)
### mix-ins
Permet de simuler l'héritange multiple
![](images/Pasted%20image%2020231026151837.png)
## Modules
Marche uniquement sur NodeJS (server-code)
![](images/Pasted%20image%2020231026152107.png)
![](images/Pasted%20image%2020231026152132.png)
![](images/Pasted%20image%2020231026152221.png)
## Manipulating DOM Objects
![](images/Pasted%20image%2020231026154926.png)
### Listening to DOM events
```
document.onkeydown = function(event) {console.log(event);}
OR
document.addEventListener('keydown', event => console.log(event))
OR
<button onclick="handleButtonClick()"> Click Me </button>
function handleButtonClick() {
	alert('button clicked')
}
OR
<button onclick="alert('Button clicked!')">Click Me</button>
```
### DOM Manipulation Libraries
*Libraires:* jQuery and Zepto (imperative)
*Modern frameworks:* React, Angular, Vue (declarative)
## Drawing in a canvas
save() pour push
restore() pour pop
![](images/Pasted%20image%2020231026155751.png)
![](images/Pasted%20image%2020231026160520.png)
## Game Loop
Remarque: setTimeout ne s'execute que 1 seule fois
```
setInterval(() => {
	game.step();
}, stepIntervalMs);
```
## Quizz
### JS du changement de couleurs (manip DOM)
![](images/Pasted%20image%2020231026163352.png)
### class -> prototype
#### class
![](images/Pasted%20image%2020231026163739.png)
#### prototype
![](images/Pasted%20image%2020231026163749.png)
# 5. Testing
Unit tests: smallest pieces
Integration tests: test unitaires mis ensembles (sans les utiliser directement)(ex: composants)
System tests: End2End (hard to automate and exepensive to execute)
![](images/Pasted%20image%2020231026163850.png)
# 6. Iterators & Client-Server Applications
## Array methods
![](images/Pasted%20image%2020231026164856.png)
![](images/Pasted%20image%2020231026164925.png)
![](images/Pasted%20image%2020231026165100.png)
## Iterators(generator)
![](images/Pasted%20image%2020231026181345.png)
![](images/Pasted%20image%2020231026222031.png)
## Flattening generator
![](images/Pasted%20image%2020231026222246.png)
## Exercice: sum of squares
![](images/Pasted%20image%2020231026222749.png)
## Exercice: count words
![](images/Pasted%20image%2020231026222824.png)
![](images/Pasted%20image%2020231026222832.png)
## Client-Server Applications
![](images/Pasted%20image%2020231026222935.png)
### Express
- Middleware
- Router
- Template engine
# 0. Autres
## Creer un projet NodeJS
>npm init
>npm install eslint --save-dev
>npx eslint --init
## Rendering patterns
### Static
HTML basique sans dynamisme
### MPA (Multi Page Application)
Render 100% sur le serveur dynamiquement -> lent pour l'utilisateur
Facile à deployer, maintenir, scale, test, secure, debug
Souvent utilisé avec MVC pattern
- Django
- Ruby on Rails
- Wordpress
- Souvent PHP, Python, Java, ...
### SPA
Shell sur le browser et JS pour fetch depuis le serveur (donne l'impression d'etre plus fluide pour l'user)
Mauvais pour SEO car les navigateurs ne savent pas à l'avance ce qu'il y a
- AngularJS
- React
### SSR
1ère requête sur le browser puis le reste sur le serveur (meta frameworks)
- NextJS
- Nuxt
- SvelteKit