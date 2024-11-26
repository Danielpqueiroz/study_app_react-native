# study_app_react_native

## **COMANDOS IMPORTANTES:**

**Primeiro de tudo, você precisa do NodeJS na versão mais nova instalado na sua máquina. Pesquise no google por "NodeJS download" e instale o programa.**

- **CRIAR UM PROJETO EXPO/REACT NATIVE DO ZERO (substitua "MeuPrimeiroApp" pelo nome do seu projeto):**
````bash
npx create-expo-app@latest MeuPrimeiroApp --template blank
````
- **CASO A CRIAÇÃO DO PROJETO DÊ UM ERRO DEVIDO A AUSÊNCIA DA PASTA ".../npm":**
````bash
mkdir C:\Users\JJQ\AppData\Roaming\npm
````
Substitua "JJQ" pelo seu usuário do windows.
- **ATIVAR O PROJETO PARA FUNCIONAR NO NAVEGADOR WEB:**
**PRMEIRO ENTRAR NA PASTA DO PROJETO NO TERMINAL E DEPOIS:** 
**(Só precisa na primeira vez que vai usar o expo na máquina, pois instala global, nas próximas vezes não precisa: npm install -g expo-cli)**
            
**Dentro da pasta do projeto:**
````bash
npx expo install react-native-web react-dom -- --legacy-peer-deps
npx expo install @expo/metro-runtime -- --legacy-peer-deps
````
- **DEPOIS DO PROJETO CRIADO E A PARTE DAS BIBLIOTECAS PARA ABRIR NA WEB TAMBÉM INSTALADOS, VOCÊ PODE INICIAR O PROJETO (ENTRANDO NA PASTA DELE NO TERMINAL), ATRAVÉS DE:**
````bash
npm start
````
O npm start vai abrir um QR Code e uma lista de opções... Se você for usar em casa vai conseguir escanear o QR no app Expo Go e testar a aplicação no celular, nos computadores da UNIESP você pode apertar a opção "w" que vai abrir o navegador web com a aplicação para testar.

Para criar uma estrutura inicial
````bash
rnfe
````
Extenção necesssaria:
````bash
ES7+
````
Bibliotecas necessarias:

Navigation
````bash
npm install @react-navigation/native
npm install react-native-screens react-native-safe-area-context
npm install @react-navigation/native-stack
````

Date picker e picker
````bash
npm install react-native-picker/picker
npm install react-native-modal-datetime-picker
````

Para gerar o .apk
- Registro no site: expo.dev
````bash
npm install -g expo-cli
npm install -g eas-cli
eas login
eas build:configure
eas build -p android --profile preview
````

## **Arquitetura das Pastas**

### **`/assets`**
Contém os recursos estáticos do aplicativo, como ícones e imagens:
- `adaptive-icon.png`: Ícone adaptativo usado em dispositivos Android/iOS.
- `favicon.png`: Ícone usado em navegadores da web.
- `icon.png`: Ícone principal do aplicativo.
- `logo.png`: Logo do aplicativo.
- `splash-icon.png`: Imagem exibida na tela de carregamento (splash screen).

### **`/src`**
O diretório principal do código-fonte do projeto.

#### **`/config`**
- **`firebaseConfig.js`**: Configuração do Firebase para autenticação e armazenamento de dados.

#### **`/contexts`**
Armazena os contextos do React para gerenciar o estado global:
- **`AuthContext.js`**: Gerencia o estado de autenticação do usuário (login, logout, etc.).
- **`CartoesEstudoContext.js`**: Gerencia o estado relacionado aos cartões de estudo (adição, edição e exclusão).

#### **`/screens`**
Contém as telas do aplicativo:
- **`EdicaoCartaoScreen.js`**: Tela para editar os cartões de estudo.
- **`ListaCartaoScreen.js`**: Tela que exibe a lista de cartões de estudo.
- **`LoginScreen.js`**: Tela de login do aplicativo.
- **`RegistroScreen.js`**: Tela para registro de novos usuários.
- **`TarefasVencimentoProximoScreen.js`**: Tela que exibe tarefas com vencimento próximo.

### Arquivos na Raiz do Projeto
- **`.env`**: Armazena variáveis de ambiente sensíveis, como chaves de API.
- **`.gitignore`**: Define os arquivos que não devem ser incluídos no controle de versão.
- **`App.js`**: Arquivo principal que inicializa o aplicativo e configura a navegação.
- **`app.json`**: Configurações do Expo para o projeto.
- **`babel.config.js`**: Configurações do Babel para transpilar o código JavaScript.
- **`eas.json`**: Configurações do Expo Application Services (EAS).

---

## **Bibliotecas Utilizadas**

### **Bibliotecas Principais**
- **`react-native`**: Framework para desenvolvimento de aplicativos móveis nativos.
- **`expo`**: Framework que simplifica o desenvolvimento de aplicativos React Native.

### **Navegação**
- **`@react-navigation/native`** e **`@react-navigation/stack`**: Gerenciam a navegação entre telas do aplicativo.
- **`@react-navigation/native-stack`**: Navegação otimizada para maior desempenho.

### **Gerenciamento de Estado**
- **`@react-native-async-storage/async-storage`**: Armazena dados localmente no dispositivo.

### **Integrações e Funcionalidades**
- **`firebase`**: Integração com o Firebase para autenticação e banco de dados.
- **`expo-local-authentication`**: Implementa autenticação local (como biometria).
- **`react-native-dotenv`**: Permite o uso de variáveis de ambiente.
- **`react-native-modal-datetime-picker`**: Permite selecionar datas e horários em modais.

### **Interface de Usuário**
- **`react-native-vector-icons`**: Biblioteca de ícones vetoriais.
- **`react-native-safe-area-context`** e **`react-native-screens`**: Gerenciam áreas seguras e transições de tela.
- **`react-native-web`**: Permite rodar aplicativos React Native no navegador.

---
