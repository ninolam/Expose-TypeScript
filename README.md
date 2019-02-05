# Expose-TypeScript

## Sources

https://blog.cellenza.com/developpement-specifique/web-developpement-specifique/introduction-a-typescript/
https://www.grafikart.fr/tutoriels/typescript-781

https://blog.logrocket.com/7-bad-excuses-for-not-using-typescript-dbf5e603a9a8

## Sommaire :

1. Qu'est-ce que TypeScript ?
2. Installation et configuration 
3. Syntaxe du typage en TypeScript
5. Quelques type en TypeScript: String, number, array, functions
6. Les modules et les classes
7. Avantages et inconvénients
8. Conclusion


### 1. Qu'est-ce que TypeScript ?

TypeScript est un langage de programmation open-source développé par Microsoft en 2012.

Il reprend le langage JavaScript en ajoutant un typage strict. Si vous vous y connaissez déjà en JS, il sera facile de migrer vers TypeScript, ce n'est pas comme si vous passez d'un langage à un autre. Il faut savoir que tout code valide en Javascript l’est également en TypeScript.
TypeScript, c'est un peu comme du JavaScript moderne et conforme aux normes.

Il a été conçu pour le développement d'applications volumineuses et la transcompilation (prend en entrée le code source d'un langage de programmation et produit le code source équivalent dans un autre langage de programmation) en JavaScript.

Il permet de développer des applications JavaScript pour les deux côté client et côté serveur

#### Pourquoi a t-il été conçu ?

TypeScript est né des faiblesses de JavaScript pour le développement d'applications à grande échelle, chez microsoft et leur clients externes.

Les développeurs de TypeScript recherchaient une solution qui ne romprait pas la compatibilité avec la norme et son support multi plate-forme

---

# 2.Installation et configuration

TypeScript est un langage open source, compatible avec n'importe quel navigateur, n'importe quel hôte et tout OS.

Via le gestionnaire de paquets Node.js vous pouvez obtenir la dernière version stable de TypeScript :

* Installer

```
npm install -g typescript
```

Si vous avez Visual Studio 2015 Update 3, Visual Studio 2017 ou encore Visual Studio code, TypeScript est installé par défaut.

Il faut savoir que JavaScript est valide dans un fichier TypeScript. Afin de pouvoir exécuter ce programme, il faut d’abord le compiler grâce à la commande suivante :

* Compiler

```
tsc helloworld.ts
```
À partir de là, il vous suffit de référencer le fichier Javascript dans la page html pour exécuter le programme.


----


### 3. Syntaxe du typage en TypeScript

TypeScript introduit la notion d’un typage un peu plus fort que pour le langage Javascript. Ce typage se manifeste par l’ajout de plusieurs types de bases ainsi qu’un typage statique.

Rappelons qu’un langage est dit de typage statique quand celui-ci vérifie les types des variables à la compilation, alors qu’un langage dit de typage dynamique,effectue cette vérification à l’exécution.

```TypeScript

let myVar: boolean;

let myVarinitialize: number = 2;

let bar = "hello world";
```
Dans l’exemple ci-dessous, les 2 premières déclarations de variables sont typées explicitement et la dernière l’est implicitement. 

----

### 5. Les modules et les classes 

#### Les classes
La classe est la notion qui définit un objet, elle est l’un des concepts clés de la programmation orientée objet avec l’interface. Ces dernières sont utilisées en tandem au travers de structures appelées “design pattern” dont l’objectif est de résoudre des problèmes spécifiques. Le TypeScript pousse les choses plus loin en permettant de gérer la visibilité des propriétés et la gestion des méthodes statiques.

 Ci-dessous un exemple de classe.

 ```TypeScript
class Personnage {
   public fullname: string;
 
   constructor(firstname: string, lastname: string) {
       this.fullname = `${firstname} ${lastname}`;
   }
 
   public greet(name?: string): string {
       if(name)
           return "Bonjour " + name + "! Je m'appelle " + this.fullname;
 
       return "Bonjour! Je m'appelle " + this.fullname;
    }
}
 
let vendeur = new Personnage("Pierre","Paul");
let msg = vendeur.greet("");
 
alert(msg);

 ```
 Dans cet exemple nous avons défini une classe “Personnage”. Pour accéder aux variables de classe, on utilise le mot-clé “this”.


#### Les modules

Un module est un regroupement logique de classes et d’interfaces qui permet de structurer un projet et de le rendre plus propice aux changements.

Le module se déclare à l’aide du mot-clé “module”. Ci-dessous un exemple de déclaration et d’utilisation d’un module simple.

```TypeScript
export module Module1{
   export class Person{
       constructor(){
       }
 
       greeting(): void{
           greeting("Module1.print()");
       }
   } 
   export const pi: number = 3.14;
 
   export interface IGreeter{
       greeting():void;
   }
 
   export function farwell(){
       alert("Bye!! You're just called the method: farwell of the module: Module1");
   }
}
 
function greeting(methodName: string): void{
   alert("Greeting !! You called the method: " + methodName);
}
```