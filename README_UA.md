# **[English](./README.md)** | **[Deutsch](./README_DE.md)** | **Українська** | **[Русский](./README_RU.md)**

Ця інструкція дасть вам змогу запустити сервер Minecraft із телефона.

> [!CAUTION]
> Можливі збої і перегрів пристрою, використовуйте на свій страх і ризик.

## Встановлення

1. Встановлення оновлень і Java. При виборі (Y/N) введіть «Y».

Якщо збираєтеся грати на версії 1.20.5 і вище.
 ```
 pkg upgrade -y && pkg install openjdk-21 -y && pkg install wget -y
 ```
Якщо збираєтеся грати на версії 1.20.4 і нижче.
  ```
 pkg upgrade -y && pkg install openjdk-17 -y && pkg install wget -y
 ```
 ![hippo](https://media2.giphy.com/media/v1.Y2lkPTc5MGI3NjExamNiMnl3MW9yZm5wcnh3dmFlZjJsODF2aW43OXl3Zmpyb2IzMzh5MCZlcD12MV9pbnRlcm5hbF9naWZfYnlfaWQmY3Q9Zw/JDvvVvvuYn4RvqT4bM/giphy.gif)

2. Дайте дозвіл Termux до сховища Android.
  ```
 termux-setup-storage
 ```
 ![hippo](https://media2.giphy.com/media/v1.Y2lkPTc5MGI3NjExanVuMmpvc205ZjA5MnNweHBiN2IydGJ1bXZsMzd6Y2Vocm0zMzllZSZlcD12MV9pbnRlcm5hbF9naWZfYnlfaWQmY3Q9Zw/lTddG6F2dAVHilKPDd/giphy.gif)

3. Встановлення сервера Minecraft у папку «MinecraftServer» у Termux.
<details>
<summary>Чистий сервер Vanilla Minecraft 1.21.5</summary>
<pre><code>mkdir ~/MinecraftServer && wget -P ~/MinecraftServer  https://piston-data.mojang.com/v1/objects/e6ec2f64e6080b9b5d9b471b291c33cc7f509733/server.jar &&
cd MinecraftServer && java -Xmx1024M -Xms1024M -jar server.jar nogui</code></pre>
<p>
  <img src="https://media1.giphy.com/media/v1.Y2lkPTc5MGI3NjExcXZpdzRoYjl0dmkwZjQ5cDgxMHBqaWZpbXd3NHViM2c2OGk5cGQ4ciZlcD12MV9pbnRlcm5hbF9naWZfYnlfaWQmY3Q9Zw/bDqpjNmqdwLlzDlMeA/giphy.gif" alt="hippo" />
</p>
</details>

<details>
<summary>Завантаження власного сервера (навіть із модами/плагінами).</summary>
Перейменуйте файл запуску на «server.jar» та імпортуйте папку із сервером у завантаження телефона.<br>
⚠ Зверніть увагу на копійовану команду!

 <pre><code>mkdir ~/MinecraftServer && cd ~/storage/downloads/Ваша папка сервера && cp -r * ~/MinecraftServer && cd ~/</code></pre>
 <p>
  <img src="https://media1.giphy.com/media/v1.Y2lkPTc5MGI3NjExNjNpcHVtMjM5b2FrdHFsdmh2c2pjZDJhNWF4czIyM3Q1N3hoaTQ4eiZlcD12MV9pbnRlcm5hbF9naWZfYnlfaWQmY3Q9Zw/lq7CavFOQJH0zSgCJz/giphy.gif" alt="hippo" />
</p>
</details>

4. Погодьтеся з ліцензією eula.
Стрілками перейдіть на рядок з «eula=false», змініть “false” на «true».
Для збереження натисніть:<br>
Ctrl+X<br>
Y<br>
Enter

![hippo](https://media1.giphy.com/media/v1.Y2lkPTc5MGI3NjExeDhoODdvN2hjcnF6ODRrcnYzM2UwdWxzaGMyMWV1OWdkc2Q3YXM2cSZlcD12MV9pbnRlcm5hbF9naWZfYnlfaWQmY3Q9Zw/GsSgLaOAFo6RL1n41h/giphy.gif)

5. Встановлення параметрів запуску сервера.
 - Наполегливо рекомендую перейти на сайт [flags.sh](https://flags.sh/), встановивши відповідну кількість оперативної пам'яті з вашого телефону, залишивши під систему хоча б 0.5 GB ОЗП.

 Після скачування додайте у файл:
  ```
 cd MinecraftServer
 ```

 Після вищевказаного імпортуйте файл у Termux такою командою:
  ```
 cp ~/storage/downloads/start.sh ~/ && chmod +x start.sh
 ```

<p>
  <img src="https://media0.giphy.com/media/v1.Y2lkPTc5MGI3NjExeTI5anZsbzZnb24xdTI1dGt0aDZ6ajVheDQ5M2wza2x6dDVqeGFjeiZlcD12MV9pbnRlcm5hbF9naWZfYnlfaWQmY3Q9Zw/8HpNYcY48ag9tUwZID/giphy.gif" alt="hippo" />
</p>

## Сервер успішно встановлений і запускається командою:
  ```
 ./start.sh
 ```