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
 ![hippo](https://media2.giphy.com/media/v1.Y2lkPTc5MGI3NjExamNiMnl3MW9yZm5wcnh3dmFlZjJsODF2aW43OXl3Zmpyb2IzMzh5MCZlcD12MV9pbnRlcm5hbF9naWZfYnlfaWQmY3Q9Zw/JDvvVvvuYn4RvqT4bM/giphy.gif)

2. Дайте разрешение Termux к хранилищу Android.
  ```
 termux-setup-storage
 ```
 ![hippo](https://media2.giphy.com/media/v1.Y2lkPTc5MGI3NjExanVuMmpvc205ZjA5MnNweHBiN2IydGJ1bXZsMzd6Y2Vocm0zMzllZSZlcD12MV9pbnRlcm5hbF9naWZfYnlfaWQmY3Q9Zw/lTddG6F2dAVHilKPDd/giphy.gif)

3. Установка Minecraft сервера в папку "MinecraftServer" в Termux.
<details>
<summary>Чистый Vanilla Minecraft server 1.21.5</summary>
<pre><code>mkdir ~/MinecraftServer && wget -P ~/MinecraftServer  https://piston-data.mojang.com/v1/objects/e6ec2f64e6080b9b5d9b471b291c33cc7f509733/server.jar &&
cd MinecraftServer && java -Xmx1024M -Xms1024M -jar server.jar nogui</code></pre>
<p>
  <img src="https://media1.giphy.com/media/v1.Y2lkPTc5MGI3NjExcXZpdzRoYjl0dmkwZjQ5cDgxMHBqaWZpbXd3NHViM2c2OGk5cGQ4ciZlcD12MV9pbnRlcm5hbF9naWZfYnlfaWQmY3Q9Zw/bDqpjNmqdwLlzDlMeA/giphy.gif" alt="hippo" />
</p>

</details>

<details>
<summary>Загрузка своего сервера(даже с модами/плагинами).</summary>
Переменуюте файл запуска в "server.jar", и импортируйте на ваш телефон.<br>
⚠ Обратите внимание на копируемую команду!

 <pre><code>mkdir ~/MinecraftServer && cp ~/Ваш путь в папку с файлами сервера/. ~/MinecraftServer/</code></pre>
</details>

4. Согласитесь с лицензией eula.
Стрелочками перейдите на строчку с "eula=false", измените "false" на "true".
Для сохранения, прожмите:<br>
Ctrl+X<br>
Y<br>
Enter

![hippo](https://media1.giphy.com/media/v1.Y2lkPTc5MGI3NjExeDhoODdvN2hjcnF6ODRrcnYzM2UwdWxzaGMyMWV1OWdkc2Q3YXM2cSZlcD12MV9pbnRlcm5hbF9naWZfYnlfaWQmY3Q9Zw/GsSgLaOAFo6RL1n41h/giphy.gif)

5. Установка параметров запуска сервера.
 - Настойчиво рекомендую перейти на сайт [flags.sh](https://flags.sh/), установив подходящее количество оперативной памяти с вашего телефона, оставив под систему хотябы 0.5 GB ОЗУ.

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
