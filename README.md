# Semana 5 - API + POSTGRES DATABASE


## Dependencias

### JEST
    
    npm i -D jest

### LINTER
    
    npm i -D eslint
   
#### Agregar en package.json
    "scripts": {
        "test": "jest --verbose"
    }

    npm test
    npm test filename.test.js

#### Crear archivo de configuración de linter (.eslintrc.js)
    npm init @eslint/config

    module.exports = {
        "env": {
            "browser": true,
            "commonjs": true,
            "es2021": true,
            "jest": true
        },
        "extends": "eslint:recommended",
        "parserOptions": {
            "ecmaVersion": "latest"
        },
        "rules": {
            indent: ["error", 4],
            "linebreak-style": ["error", "unix"],
            quotes: ["error", "double"],
            semi: ["error", "always"]
        }
    };

#### Agregar en package.json
    "scripts": {
        "test": "jest --verbose",
        "linter": "node ./node_modules/eslint/bin/eslint.js .",
        "linter-fix": "node ./node_modules/eslint/bin/eslint.js . --fix"
    }

#### Correr linter y corregir errores
    npm run linter
    npm run linter-fix
    
### EXPRESS

    npm install express --save-dev

### PRISMADB

    npm install prisma --save-dev

#### Inicializar prisma
    npx prisma init


#### Creación de base de datos

    create database explorers_api;
