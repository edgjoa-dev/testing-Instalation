
# Instalación y configuracion de Jest + React Testing Library

### 1.- instalacion
```bash
  yarn add --dev jest babel-jest @babel/preset-env @babel/preset-react 
  yarn add --dev @testing-library/react @types/jest jest-environment-jsdom
```
### 2.- instalacion si usas fetchAPI
```bash
  yarn add --dev whatwg-fetch
```
### 3.- Actualizar testing live - add to package.json
```bash
  "scripts: {
  ...
  "test": "jest --watchAll"
```
### 4.- Crear la configuración de babel babel.config.js
```bash
 module.exports = {
    presets: [
        [ '@babel/preset-env', { targets: { esmodules: true } } ],
        [ '@babel/preset-react', { runtime: 'automatic' } ],
    ],
};
```
### 5.- Opcional, pero eventualmente necesario, crear Jest config y setup: jest.config.js
```bash
module.exports = {
    testEnvironment: 'jest-environment-jsdom',
    setupFiles: ['./jest.setup.js']
}
```
### 5.- jest.setup.js
```bash
// En caso de necesitar la implementación del FetchAPI
import 'whatwg-fetch'; // <-- yarn add whatwg-fetch
```
    
## Authors

- [@edgjoa-dev](https://github.com/edgjoa-dev?tab=repositories)

