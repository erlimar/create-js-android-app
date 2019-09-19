Como criar um App JavaScript para Android
=========================================

Veja também: https://github.com/erlimar/create-ionic-android-app

1) Instale os pré-requisitos
- NodeJS - https://nodejs.org
- Java JDK - https://www.oracle.com/technetwork/java/javase/downloads/jdk8-downloads-2133151.html
- Android Studio - https://developer.android.com/studio/

2) Crie sua aplicação de exemplo
```sh
$ mkdir my-app
$ mkdir my-app/www
```

```html
<!-- www/index.html -->
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta http-equiv="X-UA-Compatible" content="ie=edge">
    <title>My App 2</title>
</head>
<body>
    <h1 id="message"></h1>
    <script src="app.js"></script>
</body>
</html>
```

```js
// www/app.js
function main(){
    let h1 = document.querySelector("#message")

    h1.innerHTML = "Welcome to my App2!"
}

main()
```

3) Instale o Capacitor
> https://capacitor.ionicframework.com/docs/getting-started/

```sh
$ npm i --save @capacitor/core @capacitor/cli
```

4) Inicialize as informações de sua aplicação
```sh
$ npx cap init
```

5) Adicione o suporte a Android
```sh
 $ npx cap add android
 ```
 
6) Abra a IDE para buildar sua aplicação
```sh
$ npx cap open android
```

Isso irá abrir o Android Studio, carregar os plugins necessários e construir sua aplicação
para uso.

Na primeira vez alguns plugins podem não ser instalados porque exigem você aceitar os
termos de licença, mas um alerta será apresentado e você só precisará clicar em instalar,
aceitar os termo e aguardar a instalação.

8) Rode sua aplicaçao

Só clicar o Play

> Aqui você está no Android Studio normal. Ou seja, você pode rodar direto em seu dispositivo
  ou em um emulador. Fica a seu critério
  
Caso deseje rodar a aplicaão direto no seu dispositivo (recomedo), você precisará conectá-lo
ia USB, e ativar a depuração por USB no dispositivo.
