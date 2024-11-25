# d3ll rakbot
## Installation
To start working with it, download the latest version of Node.JS and the following packages in the project folder.
```
npm i cluster 
npm i fs 
npm i readline
npm i mineflayer
npm i path
```
**For the rakbot to work with DexLand, MasedWorld, CheatMine, etc., you need to patch the mineflayer's skin module.**
After installing all the packages, go to `node_modules/mineflayer/lib/plugins/entities.js`.
Scroll to the bottom and add these lines of code:
```js
function extractSkinInformation (properties) {
  return undefined
}
```
This fixes the problem of CM based servers crashing the mineflayer clients by sending malformed skin data.
To launch the rakbot, make a bat file with the following code:
```bat
@echo off
:loop
node rakbot.js
pause
goto loop
```
Launch it.

## Working with it
There are 5 commands to manage the rakbot. These are for setting the server, username, start, stop and info.
Type the command inside the console to use it.

`@start` - Starts the rakbot and automatically connects to the server with specified username.

`@quit` - Stops the rakbot.

`@sethost <ip>` - Sets the server to the specified server IP.

`@setuser <name>` - Sets the player to be targeted.

`@info` - Outputs all the information (server and user).

-------------------------------
# d3ll ракбот
## Установка
Чтобы начать работать с ним, установите последнюю версию Node.JS и эти библиотеки в папке проекта.
```
npm i cluster 
npm i fs 
npm i readline
npm i mineflayer
npm i path
```
**Чтобы ракбот работал с DexLand, MasedWorld, CheatMine, и т.д., вам надо пропатчить модуль mineflayer скинов.**
После установки библиотек, заходите в `node_modules/mineflayer/lib/plugins/entities.js`.
В конец файла добавьте эти строчки кода:
```js
function extractSkinInformation (properties) {
  return undefined
}
```
Это исправляет ошибку mineflayer на серверах CM который отправляет неправильные данные о скина, краша клиент.
Чтобы запустить ракбот, сделайте бат файл со следующим кодом:
```bat
@echo off
:loop
node rakbot.js
pause
goto loop
```
Запустите его.

## Инструкции
В ракботе есть 5 команд для его работы. Это установка сервера, игрока, старт, остановка и информация.
Напишите команду в консоль чтобы ее выполнить.

`@start` - Начинает работу ракбота, автоматически подключается к серверу с ником игрока.

`@quit` - Останавливает ракбота.

`@sethost <ip>` - Устанавливает сервер.

`@setuser <name>` - Устанавливает игрока, который будет заракбочен.

`@info` - Выводит информацию настроек ракбота (сервер и игрок).
