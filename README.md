# Webpack
Proyecto y notas del [Curso de Webpack en Platzi](https://platzi.com/clases/webpack/)

## Proyecto en vivo
[js-porfolio](https://hectormoreira.github.io/js-portfolio/dist/)

## Conceptos
- **Weback** es un module bundler, es un paquete de módulos estáticos para aplicaciones de JS modernas
- **Webpack** construye un gráfico de dependencias que mapea cada módulo para con verlo en uno o más módulos
- Desde webpack 4 ya no dependemos de tener un archivo de configuración, pero si debemos tener un punto de entrada
- Sirve para empaquetar nuestro código y trabajar en forma modular
- **Loader** (transformador): Los loaders lo que hacen es decirle a webpack como tiene que transformar el código de un módulo en concreto. **Ejemplo** : Los loaders pueden transformar ficheros a JavaScript, o cargar CSS directamente en archivos JS, (si usas reactjs ya sabrás como)
- **Plugins** (complementos): Nos van a ayudar a extender las funcionalidades con los loaders, añadir otras configuraciones. **Ejemplo**: hay un módulo llamado HTMLWebpackPlugin que este se encarga de crear un HTML personalizado que le inyecta todos los bundles finales que compilamos.

## Dependencias
```sh
npm install webpack webpack-cli -D
npm install -D babel-loader @babel/core @babel/preset-env @babel/plugin-transform-runtime -D
npm install html-webpack-plugin -D
npm install mini-css-extract-plugin css-loader -D
npm install stylus stylus-loader -D
npm install copy-webpack-plugin -D
npm install url-loader file-loader -D
```
- `npm install webpack webpack-cli -D` instalar webpack en desarrollo
- `npx webpack` ejecutar paquetes directamente de npm, este viene instalado de npm
- `npx webpack --mode development` activar modo de desarrollo
- `npx webpack --mode production` activar modo de producción
- `npx webpack --mode production --config webpack.config.js` preparar el proyecto con las configuraciones
- `webpack.config.js` contiene las configuraciones de webpack
- `entry` es el punto de entrada
- `output` es el punto de salida de los archivos, por estandar es la carpeta `dist`
- `rules` reglas para trabajar con diferentes archivos
- `test` test declara que extensión de archivos aplicara el loader, usa regex
- **Babel**
    - Es un transcompilador de JavaScript que agarra el código ECMAScript 2015 en adelante y lo transforma en una versión que todos los navegadores anteriores lo puedan usar
    - Babel permite hacer que el código JavaScript sea compatible con todos los navegadores
    - Agregar al proyecto las siguientes dependencias `npm install -D babel-loader @babel/core @babel/preset-env @babel/plugin-transform-runtime`
    - `.babelrc` contiene las configuraciones de **Babel**
    - `presets` para trabajar con js moderno
    - `babel-loader`
- **CSS**
    - `npm install mini-css-extract-plugin css-loader` plugin para reconocer css
    - `npm install stylus stylus-loader` preprocesador stylus
- `npm install copy-webpack-plugin -D` plugin para copiar archivos
- `npm install url-loader file-loader -D` trabajando con fonts


## Recursos
- [Web de Webpack](https://webpack.js.org/)
- [html-loader](https://webpack.js.org/loaders/html-loader/)
- [html-webpack-plugin](https://webpack.js.org/plugins/html-webpack-plugin/)
- [asset-management Webpack](https://webpack.js.org/guides/asset-management/#loading-images)
- [Font Ubuntu](http://google-webfonts-helper.herokuapp.com/fonts/ubuntu?subsets=cyrillic,latin)