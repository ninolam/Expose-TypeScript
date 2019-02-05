# Expose-TypeScript

## Présentation

TypeScript est un langage de programmation open-source développé par Microsoft.

Il reprend le langage JavaScript en ajoutant un typage strict. Si vous vous y connaissez déjà en JS, il sera facile de migrer vers TypeScript, ce n'est pas comme si vous passez d'un langage à un autre.
TypeScript, c'est un peu comme du JavaScript moderne et conforme aux normes.

Il a été conçu pour le développement d'applications volumineuses et la transcompilation (prend en entrée le code source d'un langage de programmation et produit le code source équivalent dans un autre langage de programmation) en JavaScript.

## Sources

https://blog.cellenza.com/developpement-specifique/web-developpement-specifique/introduction-a-typescript/
https://www.grafikart.fr/tutoriels/typescript-781

https://blog.logrocket.com/7-bad-excuses-for-not-using-typescript-dbf5e603a9a8

## Sommaire

1. Qu'est que TypeScript ?
2. Installation et configuration 
3. Quelques types de bases en TypeScript
4. Syntaxe du typage
5. Les modules et les classes
6. String, number, array, functions
7. Avantages et inconvénients
8. Conclusion

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

# 6.String, number, array, functions