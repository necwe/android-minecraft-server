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
 ![hippo](https://media3.giphy.com/media/v1.Y2lkPTc5MGI3NjExazVrNmZwbzVvcWM1Z29ua3pzaWptYzFxbGdoNG1xeW1sa2ZsOHJweiZlcD12MV9pbnRlcm5hbF9naWZfYnlfaWQmY3Q9Zw/Tlp3ycP9x8p6ocy4sE/giphy.gif)

3. Установка Minecraft сервера в папку "MinecraftServer" в Termux.
<details>
<summary>Чистый Vanilla Minecraft server 1.21.5</summary>
<pre><code>mkdir ~/MinecraftServer && wget -P ~/MinecraftServer  https://piston-data.mojang.com/v1/objects/e6ec2f64e6080b9b5d9b471b291c33cc7f509733/server.jar &&
cd MinecraftServer && java -Xmx1024M -Xms1024M -jar server.jar nogui</code></pre>

</details>

<details>
<summary>Загрузка своего сервера(даже с модами/плагинами).</summary>
Переменуюте файл запуска в "server.jar", и импортируйте на ваш телефон.
> [!CAUTION]
>Обратите внимание на коприуемую команду!
 <pre><code>mkdir ~/MinecraftServer && cp ~/Ваш путь в папку с файлами сервера/. ~/MinecraftServer/</code></pre>
</details>

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
