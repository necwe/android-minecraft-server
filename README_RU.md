# **[English](./README.md)** | **[Deutsch](./README_DE.md)** | **[Українська](./README_UA.md)** | **Русский**

Эта инструкция позволит вам запустить сервер Minecraft с телефона.

> [!CAUTION]
> Возможны сбои и перегрев устройства, используйте на свой страх и риск.

## Установка

1. Установка обновлений и Java. При выборе (Y/N) введите "Y".

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

3. Установка сервера Minecraft в папку "MinecraftServer" в Termux.
<details>
<summary>Чистый сервер Vanilla Minecraft 1.21.5</summary>
<pre><code>mkdir ~/MinecraftServer && wget -P ~/MinecraftServer  https://piston-data.mojang.com/v1/objects/e6ec2f64e6080b9b5d9b471b291c33cc7f509733/server.jar &&
cd MinecraftServer && java -Xmx1024M -Xms1024M -jar server.jar nogui</code></pre>
<p>
  <img src="https://media1.giphy.com/media/v1.Y2lkPTc5MGI3NjExcXZpdzRoYjl0dmkwZjQ5cDgxMHBqaWZpbXd3NHViM2c2OGk5cGQ4ciZlcD12MV9pbnRlcm5hbF9naWZfYnlfaWQmY3Q9Zw/bDqpjNmqdwLlzDlMeA/giphy.gif" alt="hippo" />
</p>
</details>

<details>
<summary>Загрузка собственного сервера (даже с модами/плагинами).</summary>
Переименуйте файл запуска в "server.jar" и импортируйте папку с сервером в загрузки телефона.<br>
⚠ Обратите внимание на копируемую команду!

 <pre><code>mkdir ~/MinecraftServer && cd ~/storage/downloads/Ваша папка сервера && cp -r * ~/MinecraftServer && cd ~/</code></pre>
 <p>
  <img src="https://media1.giphy.com/media/v1.Y2lkPTc5MGI3NjExNjNpcHVtMjM5b2FrdHFsdmh2c2pjZDJhNWF4czIyM3Q1N3hoaTQ4eiZlcD12MV9pbnRlcm5hbF9naWZfYnlfaWQmY3Q9Zw/lq7CavFOQJH0zSgCJz/giphy.gif" alt="hippo" />
</p>
</details>

4. Согласитесь с лицензией eula.
Стрелками перейдите на строку с "eula=false", измените "false" на "true".
Для сохранения нажмите:<br>
Ctrl+X<br>
Y<br>
Enter

![hippo](https://media1.giphy.com/media/v1.Y2lkPTc5MGI3NjExeDhoODdvN2hjcnF6ODRrcnYzM2UwdWxzaGMyMWV1OWdkc2Q3YXM2cSZlcD12MV9pbnRlcm5hbF9naWZfYnlfaWQmY3Q9Zw/GsSgLaOAFo6RL1n41h/giphy.gif)

5. Установка параметров запуска сервера.
 - Настоятельно рекомендую перейти на сайт [flags.sh](https://flags.sh/), установив подходящее количество оперативной памяти с вашего телефона, оставив под систему хотя бы 0.5 GB ОЗУ.

 После скачивания добавьте в файл:
  ```
 cd MinecraftServer
 ```

 После вышеуказанного импортируйте файл в Termux следующей командой:
  ```
 cp ~/storage/downloads/start.sh ~/ && chmod +x start.sh
 ```

<p>
  <img src="https://media0.giphy.com/media/v1.Y2lkPTc5MGI3NjExeTI5anZsbzZnb24xdTI1dGt0aDZ6ajVheDQ5M2wza2x6dDVqeGFjeiZlcD12MV9pbnRlcm5hbF9naWZfYnlfaWQmY3Q9Zw/8HpNYcY48ag9tUwZID/giphy.gif" alt="hippo" />
</p>

## Сервер успешно установлен и запускается командой:
  ```
 ./start.sh
 ```
