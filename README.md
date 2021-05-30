# Reconocimiento Automatizado
Reconocimiento automatizado mediante monkey-cypress and RIPuppet

Previo a la ejecución de los scripts de reconocimiento, se debe ejecutar la aplicación ghost v3.42.5 localmente. Por default, los archivos están configurados para asumir que la aplicación ghost esta corriendo bajo la siguiente url: http://localhost:2368

## Requerimientos

Los scripts presentes en este repositorio se ejecutaron usando los siguiente programas:

- node v12.17.0
- npm v6.14.4

## Ejecucion de monkey-cypress:
La carpeta raiz del script a ejecutar es "/monkey-cypress". Ingrese a esta carpeta y ejecute el comando:
```
npm install
```
Para ejecutar el script de prueba de reconocimiento con monkeys, sobre la carpera  "/monkey-cypress" ejecute el siguiente comando:
```
./node_modules/.bin/cypress run -C monkey-config.json
```
El comando anterior ejecuta el script "monkey.js" ubicado en la carpeta direccion "cypress/integration/monkey".<br>
Se cuenta con el script "smart-monkey.js" el cual se encuentra en la misma carpeta. Para ejecutarlo, asumiendo que la raiz del script de ejecucion es la carpeta "/monkey-cypress":
```
./node_modules/.bin/cypress run -C smart-monkey-config.json
```
Los resultados para ambos scripts se almacenan en la ruta "/monkey-cypress/results".<br>
Para configurar los parametros de ejecucion de los scripts, modifique los archivos "monkey-cypress/monkey-config.json" y "monkey-cypress/smart-monkey-config.json", o puede modificar directamente los scripts "monkey-cypress/cypress/integration/monkey/monkey.js" y "monkey-cypress/cypress/integration/monkey/smart-monkey.js". Para mayor informacion, pude recurrir a la fuente original de estos scripts: https://github.com/TheSoftwareDesignLab/monkey-cypress

## Ejecucion de RIPuppet: 

La carpeta raiz del script a ejecutar es "/RIPuppetCoursera". Ingrese a esta carpeta y ejecute el comando:
```
npm install
```
Para ejecutar el ripper programado sobre la carpeta "/RIPuppetCoursera", ejecute el comando:
```
node index.js
```
Los resultados de la prueba se almacenan en la carpeta "/RIPuppetCoursera/results". Se genera una carpeta cuyo nombre es la estampa de tiempo del momento en el que se ejecuto, por cada ejecucion. Puede modificar los parámetros de la prueba en el archivo "/RIPuppetCoursera/config.json". Para mayor informacion sobr el funcionamiento de este script, consulte la fuente original: https://github.com/TheSoftwareDesignLab/RIPuppetCoursera
