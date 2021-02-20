# Tiendafrontend (con Svelte)



## ¿Qué es **svelte**?



Existen muchas bibliotecas y frameworks para desarrollo en Javascript, tanto para su uso en el **backend** con node.js, como en el **frontend**.

En cuanto al **frontend**, tenemos a **Angular**, **React** y **Vue** como las bibliotecas/frameworks más usadas/os.

El desarrollo de frontend está muy publicitado y la necesidad de dicho tipo de desarrolladores es manifiesta. Independientemente de framework usado, parece haber una convergencia y acuerdo entre ellos: **todos realizadan desarrollo por componentes web**.

Un **componente web** es una **parte de una aplicación web que encapsula código HTML, CSS y JavaScript**, de forma que no puede ser afectado por el código de la página que lo incluye, salvo que usemos los mecanismos establecidos a tal efecto. Por tanto permiten la reutilización y encapsulación de código cliente.

Svelte es un **compilador** (también puede calificarse como framework), que toma muchas ideas prestadas de los frameworks anteriores, sobre todo de React. Sin embargo hay una característica que lo diferencia de los anteriores:

- Svelte **realiza una compilación** de nuestro código, convirtiendo sus componentes en código imperativo altamente eficiente.

Proporcionando las siguientes ventajas:

- Tenemos que escribir mucho menos código frente a otros frameworks.
- El código final se ejecuta de forma muy eficiente y rápida.
- El peso (cantidad de KB) de la aplicación final es muy pequeño.
- Facilita la programación reactiva.

Un ventaja añadida es que su sintaxis es más simple, lo cual hace que su curva de aprendizaje sea menos pronunciada que la de otros frameworks. Por este motivo es un buen candidato para su uso con fines didácticos.

## Inicio de un proyecto de svelte



```
npx  degit  sveltejs/template   nombre-proyecto
```



**Estructura de un proyecto Svelte**

````
├── package.json
├── public
│   ├── favicon.png
│   ├── global.css
│   └── index.html
├── README.md
├── rollup.config.js
└── src
    ├── App.svelte
    └── main.js
````



**Para ejecutar la aplicación deberemos ejecutar:**

```
npm  run  dev
```

**Para instalar las dependencias del package.json, ejecutamos:**

````npm  install````



