# README: Funcionamiento de la aplicación Svelte

## Descripción
Este proyecto Svelte es una aplicación para gestionar gastos compartidos entre varios usuarios. Permite ingresar el gasto total, así como las aportaciones individuales de cada usuario y calcula automáticamente los saldos pendientes.

## Componentes Principales
### 1. `Aportacion.svelte`
Este componente se encarga de recibir la entrada del usuario para el gasto total y las aportaciones individuales de cada participante. También, realiza cálculos y actualiza el estado de la aplicación en consecuencia.

### 2. `Saldo.svelte`
Es un componente que muestra el saldo pendiente para cada usuario después de realizar las aportaciones. Este saldo se calcula automáticamente.

## Funcionamiento
1. **Ingreso de Datos:** Se ingresa el gasto total y las aportaciones de cada usuario en los campos correspondientes.
2. **Cálculo de Saldos:** El sistema calcula automáticamente el saldo pendiente para cada usuario.
3. **Visualización de Resultados:** Los resultados se muestran en una tabla donde se listan los nombres de los usuarios, sus aportaciones y sus saldos pendientes.
4. **Estilos Interactivos:** Los estilos CSS utilizados proporcionan una experiencia visual atractiva, incluyendo animaciones en el título y estilos de tabla alternativos para mejorar la legibilidad.

## Variables Principales
- `totalGasto`: Almacena el gasto total ingresado por el usuario.
- `cadaUsuario`: Representa la cantidad que cada usuario debería aportar para equilibrar los gastos.
- `aportadoPorPersona`: Lista las aportaciones individuales de cada usuario.
- `recorrerArray`: Array que almacena los objetos de cada usuario con su nombre, aporte y saldo pendiente.
- `pasta`: Calcula el saldo pendiente de cada usuario.

## Funciones Utilizadas
- `reduce(n)`: Redondea un número `n` a dos decimales.
- `valor`: Variable calculada que representa el valor redondeado de `cadaUsuario`.

## Estilos CSS
- Se han definido estilos para mejorar la presentación de la aplicación, incluyendo colores alternativos para las filas de la tabla y efectos visuales para el título.
- Los estilos aseguran una visualización clara y atractiva de los datos.

## Uso
1. Clona este repositorio.
2. Instala las dependencias utilizando npm o yarn.
3. Ejecuta la aplicación utilizando el comando adecuado para el entorno de desarrollo.
4. Ingresa el gasto total y las aportaciones de cada usuario.
5. Observa los resultados en la tabla generada.

¡Disfruta gestionando tus gastos compartidos con esta aplicación Svelte!









# Svelte + Vite

This template should help get you started developing with Svelte in Vite.

## Recommended IDE Setup

[VS Code](https://code.visualstudio.com/) + [Svelte](https://marketplace.visualstudio.com/items?itemName=svelte.svelte-vscode).

## Need an official Svelte framework?

Check out [SvelteKit](https://github.com/sveltejs/kit#readme), which is also powered by Vite. Deploy anywhere with its serverless-first approach and adapt to various platforms, with out of the box support for TypeScript, SCSS, and Less, and easily-added support for mdsvex, GraphQL, PostCSS, Tailwind CSS, and more.


```js
// store.js
// An extremely simple external store
import { writable } from 'svelte/store'
export default writable(0)
```
