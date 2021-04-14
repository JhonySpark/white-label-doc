### Celer Bank - White-label

Neste documento vamos listar e documentar os paramentros necessários 
para gerar um white-label do app Celer Bank.

O processo de criação e geração do white-label começa a partir da criação de um arquivo JSON contendo os paramentros do app, cores, url de arquivos e imagens, etc. 

Este arquivo JSON é importado para o firebase que mantem os cadastros dos clientes white-label, onde podemos acessa-lo no script de geração do white-label.

#### Script NODE 
----
Criamos um script NODE.JS que faz a leitura dos parametros no firebase e os grava em 
um arquvo de configuração dentro do diretório "src/config". 

Depois de criar o aquivo de configuração, o script faz o download dos arquivos,  imagens e ícones listados dentro no JSON e os insere no diretório do objeto.

Após rodar o script o projeto é modificado, os itens são sobrescritos e o app está pronto para fazer a build do novo white-label. 


`$ npm run create-label` ou `$ yarn create-label`

#### JSON 
----
***Estrutura para arquivos, icones e imagens do JSON***
- [x] **"arquivo**
  - [x] format: png - `( formato do arquivo exp: js, json, jpg, img. )`
  - [x] name: logo - `( nome do arquivo )`
  - [x] path: "./src/assets/img/",  - `( diretório do arquivo )`
  - [x] url: "https://firebases..." - `( url do arquivo no storage )`

***Estrutura completa do JSON***

- [x] **clients**
  - [x] **Celer**
  	- [x] contractingID
    - [x] **files**
        - [x] **"Android Strings"**
          - [x] format
          - [x] name
          - [x] path
          - [x] url
        - [x] **gradle-properties**
          - [x] format
          - [x] name
          - [x] path
          - [x] url
    - [x] **icons** - `(Colocar todos os tamanhos)`
        - [x] **hdpi-round**
          - [x] format
          - [x] name
          - [x] path
          - [x] url
        - [x] **hdpi-square**
          - [x] format
          - [x] name
          - [x] path
          - [x] url
    - [x] **imagens** `(Todas estão na seção de cores)`
        - [x] **backgroundChat** 
          - [x] format
          - [x] name
          - [x] path
          - [x] url
        - [x] **...**
    - [x] **stylesConfig**
        - [x] ***AppData***
        	- [x] AppName
        	- [x] BankName
        	- [x] appId
        	- [x] contractingID
        	- [x] editFintechCode
        	- [x] fintechCode
        - [x] ***Colors*** 
        	- [x] ColorName: ... `(listadas na seção de cores)`
        - [x] ***fonts***
        	- [x] ***Family***
              - [x] Bold
              - [x] Regular
              - [x] Semibold
        	- [x] ***Size***
              - [x] Details
              - [x] HeaderBar
              - [x] Min
              - [x] Priority
              - [x] Subtitle
              - [x] TabBar
              - [x] Title
              - [x] Value
              - [x] ValuePrefix
        	- [x] ***Texts***
              - [x] featuredOne
              - [x] featuredThree
              - [x] featuredTwo
              - [x] phraseOne
			  - [x] phraseTwo
              - [x] phraseThree

#### CORES
> Client => stylesConfig => Colors 

Abaixo estão listadas todas as cores utilizadas por padrõa no app Celer Bank
Caso algum parametro de cor não seja alterado, o white-label vai manter a cor padrão ou a utilizada no white-label anterior.

      "AcquaGreen" : "#00D68E",
      "AddCredit" : "#06afef",
      "AlmostLight" : "#fbfbfb",
      "Black" : "#000000",
      "Credit" : "#86db61",
      "CyanGreen" : "#32bcad",
      "Dark" : "#1e1e1e",
      "DarkBlue" : "#0041a0",
      "DarkGrey" : "#5a5a5a",
      "Debit" : "#e80000",
      "Error" : "#e80000",
      "ErrorBorder" : "#FF8A8A",
      "Extract" : "#86db61",
      "Gradient" : [ "#06afef", "#6dd5ed" ],
      "GradientError" : [ "#BCE0FD", "#EAF8FF" ],
      "Green" : "#86db61",
      "GreenPantone" : "#3cae3c",
      "Grey" : "#a7a7a7",
      "IndigoDye" : "#083c50",
      "Light" : "#fff",
      "LightDarkGrey" : "#969696",
      "LightGreen" : "#b2f251",
      "LightGrey" : "#d2d2d2",
      "LightSecundaryBlue" : "#BCE0FD",
      "LilyWhite" : "#E9FBFF",
      "LittleGrey" : "#e5e5e5",
      "MineShaft" : "#232323",
      "Orange" : "#f6811d",
      "PayBillet" : "#780fbe",
      "Pix" : "#32bcad",
      "Primary" : "#06afef",
      "Purple" : "#780fbe",
      "Recharge" : "#ffb400",
      "Red" : "#e80000",
      "Rose" : "#FF8A8A",
      "Secundary" : "#6dd5ed",
      "Tertiary" : "#BCE0FD",
      "Transaction" : "#f6811d",
      "WildSand" : "#F6F6F6",
      "Yellow" : "#ffb400"
      
#### Imagens
> Client => imagens 

Abaixo estão listadas todas as imagens utilizadas por padrõa no app Celer Bank
Caso alguma não seja alterada, o white-label vai manter a cor padrão ou a utilizada no white-label anterior..

    "backgroundChat - 359x607" : {
      "format" : "png",
      "name" : "bg-chat",
      "path" : "./src/assets/img/",
      "url" : ""
    },
    
    "businessCard - 1277x794" : {
      "format" : "png",
      "name" : "app-business-card",
      "path" : "./src/assets/img/",
      "url" : ""
    },
    "cardSuccessUnblock - 1206x819" : {
      "format" : "png",
      "name" : "card-success-unblock",
      "path" : "./src/assets/img/",
      "url" : ""
    },
    "changeDevice - 651x483" : {
      "format" : "png",
      "name" : "change-device",
      "path" : "./src/assets/img/",
      "url" : ""
    },
    "elementLogin - 1080x938" : {
      "format" : "png",
      "name" : "element-login",
      "path" : "./src/assets/img/",
      "url" : ""
    },
    "enableBiometric - 2084x1416" : {
      "format" : "png",
      "name" : "enable-biometrics",
      "path" : "./src/assets/img/",
      "url" : ""
    },
    "failOnboard - 1206x819" : {
      "format" : "png",
      "name" : "fail-onboard",
      "path" : "./src/assets/img/",
      "url" : ""
    },
    "internalCard - 1277x795" : {
      "format" : "png",
      "name" : "app-internal-card",
      "path" : "./src/assets/img/",
      "url" : ""
    },
    "loginFirst - 1080x1920" : {
      "format" : "png",
      "name" : "login-first",
      "path" : "./src/assets/img/",
      "url" : ""
    },
    "loginSecond - 1080x1920" : {
      "format" : "png",
      "name" : "login-second",
      "path" : "./src/assets/img/",
      "url" : ""
    },
    "loginThird - 1080x1920" : {
      "format" : "png",
      "name" : "login-third",
      "path" : "./src/assets/img/",
      "url" : ""
    },
    "logoApp155x51 - 155x51" : {
      "format" : "png",
      "name" : "logo-app-155x51",
      "path" : "./src/assets/img/",
      "url" : ""
    },
    "logoApp788x1202 - 788x1202" : {
      "format" : "png",
      "name" : "logo-app-788x1202",
      "path" : "./src/assets/img/",
      "url" : ""
    },
    "logoAppSplash - 207x298" : {
      "format" : "png",
      "name" : "logo-app-splash-207x298",
      "path" : "./src/assets/img/",
      "url" : ""
    },
    "logoAppWhite - 434x138" : {
      "format" : "png",
      "name" : "logo-app-white-434x138",
      "path" : "./src/assets/img/",
      "url" : ""
    },
    "logoHeader - 154x50" : {
      "format" : "png",
      "name" : "logo-header-154x50",
      "path" : "./src/assets/img/",
      "url" : ""
    },
    "logoMain - 83x110" : {
      "format" : "png",
      "name" : "logo-main",
      "path" : "./src/assets/img/",
      "url" : ""
    },
    "logoPixFull - 80x28" : {
      "format" : "png",
      "name" : "logo-pix-full",
      "path" : "./src/assets/img/",
      "url" : ""
    },
    "logoSystemMessageAvatar - 176x210" : {
      "format" : "png",
      "name" : "logo-system-messager-avatar-176x210",
      "path" : "./src/assets/img/",
      "url" : ""
    },
    "onboardingConcluded - 1206x819" : {
      "format" : "png",
      "name" : "onboarding-concluded",
      "path" : "./src/assets/img/",
      "url" : ""
    },
    "passwordSuccess - 1206x819" : {
      "format" : "png",
      "name" : "password-success",
      "path" : "./src/assets/img/",
      "url" : ""
    },
    "personalCard - 1277x795" : {
      "format" : "png",
      "name" : "app-personal-card",
      "path" : "./src/assets/img/",
      "url" : ""
    },
    "pixIconAtive - 31x31" : {
      "format" : "png",
      "name" : "pix-icon-ative",
      "path" : "./src/assets/img/",
      "url" : ""
    },
    "pixIconInative - 22x22" : {
      "format" : "png",
      "name" : "pix-icon-inative",
      "path" : "./src/assets/img/",
      "url" : ""
    },
    "pixIconWhite - 1361x1365" : {
      "format" : "png",
      "name" : "pix-icon-white",
      "path" : "./src/assets/img/",
      "url" : ""
    },
    "pixPrimary - 805x667" : {
      "format" : "png",
      "name" : "pix-primary",
      "path" : "./src/assets/img/",
      "url" : ""
    },
    "pixSecondary - 1009x668" : {
      "format" : "png",
      "name" : "pix-secundary",
      "path" : "./src/assets/img/",
      "url" : ""
    },
    "tokenChange - 2085x1379 " : {
      "format" : "png",
      "name" : "token-change",
      "path" : "./src/assets/img/",
      "url" : ""
    },
    "transactionPassword - 1040x713" : {
      "format" : "png",
      "name" : "transaction-password",
      "path" : "./src/assets/img/",
      "url" : ""
    },
    "virtualCard - 1277x794" : {
      "format" : "png",
      "name" : "app-virtual-card",
      "path" : "./src/assets/img/",
      "url" : ""
    },
    "virtualGeneratedCard - 1277x794" : {
      "format" : "png",
      "name" : "app-virtual-generate-card",
      "path" : "./src/assets/img/",
      "url" : ""
    }
    
    
   
   
#### Lista de imagens necessárias
| Imagem  								   |  Tamanho  |
| ---------------------------------------- | --------- |
| app-business-card.png 				   | 1277x794  |
| app-internal-card.png 				   | 1277x795  |
| app-personal-card.png 				   | 1277x795  |
| app-virtual-card.png   	               | 1277x794  |
| app-virtual-generate-card.png 		   | 1277x794  |
| card-success-unblock.png 				   | 1206x819  |
| change-device.png 					   | 651x483   |
| element-login.png 					   | 1080x938  |
| enable-biometrics.png 				   | 2084x1416 |
| fail-onboard.png 						   | 1206x819  |
| login-first.png 						   | 1080x1920 |
| login-second.png 						   | 1080x1920 |
| login-third.png 						   | 1080x1920 |
| logo-app-155x51.png  					   |  155x51   | 
| logo-app-788x1202.png 				   | 788x1202  |
| logo-app-splash-207x298.png 			   | 207x298   |
| logo-app-white-434x138.png 			   | 434x138   |
| logo-header-154x50.png 				   | 154x50    |
| logo-main.png 						   | 83x110    |
| logo-system-messager-avatar-176x210.png  | 176x210   |
| onboarding-concluded.png 				   | 1206x819  |
| password-success.png 					   | 1206x819  |
| pix-primary.png 						   | 805x667   |
| pix-secundary.png 					   | 1009x668  |
| token-change.png 						   | 2085x1379 |
| transaction-password.png 			       | 1040x713  |
| logo.png ( Para gerar icones)			   |  512x512  |













 

