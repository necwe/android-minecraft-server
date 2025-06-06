# **[English](./README.md)** | **[Deutsch](./README_DE.md)** | **[Українська](./README_UA.md)** | **Русский**

Эта инструкция позволит вам открыть сервер Minecraft с вашего телефона.

> [!CAUTION]
> Возможны сбои и перегрев устройства, используйте на свой страх и риск.

## Установка

1. Установка обновлений, и Java. При выборе (Y/N) пропишите "Y"

Если собираитесь играть на версии 1.20.5 и выше.
 ```
 pkg upgrade -y && pkg install openjdk-21 -y && pkg install wget -y
 ```
Если собираитесь играть на версии 1.20.4 и ниже.
  ```
 pkg upgrade -y && pkg install openjdk-17 -y && pkg install wget -y
 ```
 ![hippo](https://media3.giphy.com/media/v1.Y2lkPTc5MGI3NjExZXQ3cW5hemozZHY0eWl0OXNhZGJzZ3QwdmZxNWV2ejVxZDQweTA0MiZlcD12MV9pbnRlcm5hbF9naWZfYnlfaWQmY3Q9Zw/zfTypSIDGNaUH3IZF4/giphy.gif)

2. Дайте разрешение Termux к хранилищу Android.
  ```
 termux-setup-storage
 ```

3. Установка Minecraft 1.21.5 сервера в созданную папку "MinecraftServer" в Termux.
 ```
 mkdir ~/MinecraftServer && wget -P ~/MinecraftServer  https://piston-data.mojang.com/v1/objects/e6ec2f64e6080b9b5d9b471b291c33cc7f509733/server.jar &&
cd MinecraftServer && java -Xmx1024M -Xms1024M -jar server.jar nogui
 ```
Или можно загрузить свой прогрузивщийся сервер(даже с модами/плагинами).
Заранее изменив файл запуска на "server.jar".
  ```
 mkdir ~/MinecraftServer && cp ~/Ваш путь в папку с файлами/. ~/MinecraftServer/
 ```

4. Согласитесь с лицензией eula.
  ```
 termux-setup-storage
 ```
Стрелочками перейдите на строчку с "eula=false", измените "false" на "true".
Для сохранен7ия, прожмите:
Ctrl+X
Y
Enter

5. Установка параметров запуска сервера.
 - Настойчиво рекомендую перейти на сайт [flags.sh](https://flags.sh/), установив подходящее количество оперативной памяти с вашего телефона, оставив под андроид хотябы 0.5 GB ОЗУ.

 После скачивания, добавте в файл:
  ```
 cd MinecraftServer
 ```

 После выше перечисленного, импортируйте файл в Termux следуйщей командой:
  ```
 cp ~/storage/downloads/start.sh ~/ && chmod +x start.sh
 ```

Сервер успешно установлен, и запускаеться командой:
  ```
 ./start.sh
 ```
