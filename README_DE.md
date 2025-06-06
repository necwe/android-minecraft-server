# **[English](./README.md)** | **Deutsch** | **[Українська](./README_UA.md)** | **[Русский](./README_RU.md)**

Mit dieser Anleitung kannst du einen Minecraft-Server von deinem Handy aus starten.

> [!CAUTION]
> Es kann zu Fehlfunktionen und Überhitzung des Geräts kommen, die Benutzung erfolgt auf eigene Gefahr.

## Einrichtung

1. Updates und Java installieren. Wenn (Y/N) ausgewählt ist, geben Sie „Y“ ein.

Wenn Sie mit der Version 1.20.5 und höher spielen wollen.
 ```
 pkg upgrade -y && pkg install openjdk-21 -y && pkg install wget -y
 ```
Wenn Sie mit der Version 1.20.4 und darunter spielen wollen.
  ```
 pkg upgrade -y && pkg install openjdk-17 -y && pkg install wget -y
 ```
 ![hippo](https://media2.giphy.com/media/v1.Y2lkPTc5MGI3NjExamNiMnl3MW9yZm5wcnh3dmFlZjJsODF2aW43OXl3Zmpyb2IzMzh5MCZlcD12MV9pbnRlcm5hbF9naWZfYnlfaWQmY3Q9Zw/JDvvVvvuYn4RvqT4bM/giphy.gif)

2. Geben Sie Termux die Berechtigung für den Android-Speicher.
  ```
 termux-setup-storage
 ```
 ![hippo](https://media2.giphy.com/media/v1.Y2lkPTc5MGI3NjExanVuMmpvc205ZjA5MnNweHBiN2IydGJ1bXZsMzd6Y2Vocm0zMzllZSZlcD12MV9pbnRlcm5hbF9naWZfYnlfaWQmY3Q9Zw/lTddG6F2dAVHilKPDd/giphy.gif)

3. Installieren Sie den Minecraft-Server in den Ordner „MinecraftServer“ in Termux.
<details>
<summary>Sauberer Server Vanilla Minecraft 1.21.5</summary>
<pre><code>mkdir ~/MinecraftServer && wget -P ~/MinecraftServer  https://piston-data.mojang.com/v1/objects/e6ec2f64e6080b9b5d9b471b291c33cc7f509733/server.jar &&
cd MinecraftServer && java -Xmx1024M -Xms1024M -jar server.jar nogui</code></pre>
<p>
  <img src="https://media1.giphy.com/media/v1.Y2lkPTc5MGI3NjExcXZpdzRoYjl0dmkwZjQ5cDgxMHBqaWZpbXd3NHViM2c2OGk5cGQ4ciZlcD12MV9pbnRlcm5hbF9naWZfYnlfaWQmY3Q9Zw/bDqpjNmqdwLlzDlMeA/giphy.gif" alt="hippo" />
</p>
</details>

<details>
<summary>Laden Sie Ihren eigenen Server (auch mit Mods/Plugins).</summary>
Benennen Sie die Startdatei in „server.jar“ um und importieren Sie den Server-Ordner in die Downloads Ihres Telefons.<br>
⚠ Achten Sie auf den Befehl, der kopiert wird!

 <pre><code>mkdir ~/MinecraftServer && cd ~/storage/downloads/Ihr Server-Ordner && cp -r * ~/MinecraftServer && cd ~/</code></pre>
 <p>
  <img src="https://media1.giphy.com/media/v1.Y2lkPTc5MGI3NjExNjNpcHVtMjM5b2FrdHFsdmh2c2pjZDJhNWF4czIyM3Q1N3hoaTQ4eiZlcD12MV9pbnRlcm5hbF9naWZfYnlfaWQmY3Q9Zw/lq7CavFOQJH0zSgCJz/giphy.gif" alt="hippo" />
</p>
</details>

4. Ich stimme mit der Eula-Lizenz überein.
Navigieren Sie mit den Pfeilen zu der Zeile mit „eula=false“ und ändern Sie ‚false‘ in „true“.
Klicken Sie zum Speichern:<br>
Ctrl+X<br>
Y<br>
Enter

![hippo](https://media1.giphy.com/media/v1.Y2lkPTc5MGI3NjExeDhoODdvN2hjcnF6ODRrcnYzM2UwdWxzaGMyMWV1OWdkc2Q3YXM2cSZlcD12MV9pbnRlcm5hbF9naWZfYnlfaWQmY3Q9Zw/GsSgLaOAFo6RL1n41h/giphy.gif)

5. Legen Sie die Startparameter für den Server fest.
 - Ich empfehle dringend, [flags.sh](https://flags.sh/) aufzurufen und die entsprechende Menge an RAM von Ihrem Telefon zu installieren, so dass mindestens 0,5 GB RAM für das System übrig bleiben.

 Nach dem Download fügen Sie die Datei hinzu:
  ```
 cd MinecraftServer
 ```

 Danach importieren Sie die Datei in Termux mit folgendem Befehl:
  ```
 cp ~/storage/downloads/start.sh ~/ && chmod +x start.sh
 ```

<p>
  <img src="https://media0.giphy.com/media/v1.Y2lkPTc5MGI3NjExeTI5anZsbzZnb24xdTI1dGt0aDZ6ajVheDQ5M2wza2x6dDVqeGFjeiZlcD12MV9pbnRlcm5hbF9naWZfYnlfaWQmY3Q9Zw/8HpNYcY48ag9tUwZID/giphy.gif" alt="hippo" />
</p>

## Der Server wurde erfolgreich installiert und mit dem Befehl gestartet:
  ```
 ./start.sh
 ```
