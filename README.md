# Trabajo Práctico N° 6 VUE.JS

## Desarrollo

### Crear un proyecto Vue.js con vite

Abrir la terminal de VSCode y escribir el siguiente comando

```cmd
npm init vite
```

Seguir los pasos para la instalacion como lo trabajamos en clase:

- Nombre del proyecto : **tp6-vuejs**
- Framework: **Vue**
- lenguaje: **typescript**

Una vez que se inicia entrar en la carpeta creada

``` cmd
cd tp6-vuejs
```

Ejecutar el comando: ```code .``` esto nos abrirá VSCode en la carpeta donde estemos parados, seguimos en la consola/terminal y corremos el comando:

```cmd
npm install
```

y luego para levantar la aplicación:

``` cmd
npm run dev
```

### Limpiar el archivo App.vue

Veremos que se nos han creados archivos y carpetas, por ahora la que vamos a manejar es la carpeta: ```src/```
buscar el archivo ```App.vue``` y borramos su contenido dejando solo las etiquetas:

```js
<template></template>
<script setup lang='ts'></script>
<style scoped></style>
```

### Crear nuestro primer componente

En la carpeta ```components/``` vamos a crear nuestro primer componente: un **Formulario** (```FormComponent.vue```)
en el ```<template>``` vamos a crear un ```<form>``` que debe tener:

- dos campos input de tipo texto y password respectivamente: **username**, **password**
- un campo input tipo email: **email**  
- un input tipo submit **enviar**

Estos input deben estar bindeados con ```v-model``` a las constantes ```username```, ```password```, ```email```, ```enviar```
que son de tipo:```string```, recuerden que vamos a trabajar con ```typescritp``` asi que tiparemos todo.
ejemplo:

```js
<script setup lang='ts'>
import {ref, Ref} from 'vue'

const username:Ref<string> = ref('')
</script>
```

Lo que acabamos de haces es crear una constante ```username``` de tipo:```string``` con el valor de cadena de texto vacio.

- Crear una función que tome los datos de los campos mencionados y los imprima por consola, recuerden que para tomar los datos del DOM con variables bindeadas tenemos que acceder a su valor ```username.value```.

### Importamos nuestro Componente

- Importar y mostrar el componente ```FormComponent``` en el componente principal ```App```
