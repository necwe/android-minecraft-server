# **Русский | [English](./README.md) | [Deutsch](./README_DE.md) **

Эта инструкция позволит вам открыть сервер Minecraft с вашего телефона.

> [!ОСТОРОЖНО]
> Возможны сбои и перегрев устройства, используйте на свой страх и риск.

## Установка

1. Установка обновлений, и Java. При выборе (Y/N) пропишите "Y"
Если собираитесь играть на версии 1.20 и выше.
 ```
 pkg upgrade -y && pkg install openjdk-21 -y && pkg install wget -y
 ```
 Если собираитесь играть на версии 1.19 и ниже.
  ```
 pkg upgrade -y && pkg install openjdk-17 -y && pkg install wget -y
 ```

2. Дайте разрешение Termux к хранилищу Android.
  ```
 termux-setup-storage
 ```

3. Установка Minecraft 1.21.5 сервера в созданную папку "MinecraftServer" в Termux.
 ```
 mkdir ~/MinecraftServer &&
wget -P ~/MinecraftServer  https://piston-data.mojang.com/v1/objects/e6ec2f64e6080b9b5d9b471b291c33cc7f509733/server.jar &&
cd MinecraftServer && java -Xmx1024M -Xms1024M -jar server.jar nogui
 ```
Или можно загрузить свой прогрузивщийся сервер(даже с модами/плагинами).
Заранее изменив файл запуска на "server.jar".
  ```
 mkdir ~/MinecraftServer && cp ~/Ваш путь в папку с файлами/. ~/MinecraftServer/
 ```

4. 
