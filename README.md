# **English** | **[Deutsch](./README_DE.md)** | **[Українська](./README_UA.md)** | **[Русский](./README_RU.md)**

These instructions will allow you to start a Minecraft server from your phone.

> [!CAUTION]
> Malfunctions and overheating of the device may occur, use at your own risk.

## Installation

1. Install updates and Java. When selecting (Y/N), enter ‘Y’.

If you are going to play on version 1.20.5 and above.
 ```
 pkg upgrade -y && pkg install openjdk-21 -y && pkg install wget -y
 ```
If you are going to play on version 1.20.4 and below.
  ```
 pkg upgrade -y && pkg install openjdk-17 -y && pkg install wget -y
 ```
 ![hippo](https://media2.giphy.com/media/v1.Y2lkPTc5MGI3NjExamNiMnl3MW9yZm5wcnh3dmFlZjJsODF2aW43OXl3Zmpyb2IzMzh5MCZlcD12MV9pbnRlcm5hbF9naWZfYnlfaWQmY3Q9Zw/JDvvVvvuYn4RvqT4bM/giphy.gif)

2. Give Termux permission to the Android storage.
  ```
 termux-setup-storage
 ```
 ![hippo](https://media2.giphy.com/media/v1.Y2lkPTc5MGI3NjExanVuMmpvc205ZjA5MnNweHBiN2IydGJ1bXZsMzd6Y2Vocm0zMzllZSZlcD12MV9pbnRlcm5hbF9naWZfYnlfaWQmY3Q9Zw/lTddG6F2dAVHilKPDd/giphy.gif)

3. Install the Minecraft server in the ‘MinecraftServer’ folder in Termux.
<details>
<summary>Clean server Vanilla Minecraft 1.21.5</summary>
<pre><code>mkdir ~/MinecraftServer && wget -P ~/MinecraftServer  https://piston-data.mojang.com/v1/objects/e6ec2f64e6080b9b5d9b471b291c33cc7f509733/server.jar &&
cd MinecraftServer && java -Xmx1024M -Xms1024M -jar server.jar nogui</code></pre>
<p>
  <img src="https://media1.giphy.com/media/v1.Y2lkPTc5MGI3NjExcXZpdzRoYjl0dmkwZjQ5cDgxMHBqaWZpbXd3NHViM2c2OGk5cGQ4ciZlcD12MV9pbnRlcm5hbF9naWZfYnlfaWQmY3Q9Zw/bDqpjNmqdwLlzDlMeA/giphy.gif" alt="hippo" />
</p>
</details>

<details>
<summary>Loading your own server (even with mods/plugins).</summary>
Rename the startup file to ‘server.jar’ and import the server folder into your phone's downloads.<br>
⚠ Pay attention to the command being copied!

 <pre><code>mkdir ~/MinecraftServer && cd ~/storage/downloads/Your server folder && cp -r * ~/MinecraftServer && cd ~/</code></pre>
 <p>
  <img src="https://media1.giphy.com/media/v1.Y2lkPTc5MGI3NjExNjNpcHVtMjM5b2FrdHFsdmh2c2pjZDJhNWF4czIyM3Q1N3hoaTQ4eiZlcD12MV9pbnRlcm5hbF9naWZfYnlfaWQmY3Q9Zw/lq7CavFOQJH0zSgCJz/giphy.gif" alt="hippo" />
</p>
</details>

4. Agree with the eula licence.
Use the arrows to navigate to the line with ‘eula=false’, change “false” to ‘true’.
Click to save:<br>
Ctrl+X<br>
Y<br>
Enter

![hippo](https://media1.giphy.com/media/v1.Y2lkPTc5MGI3NjExeDhoODdvN2hjcnF6ODRrcnYzM2UwdWxzaGMyMWV1OWdkc2Q3YXM2cSZlcD12MV9pbnRlcm5hbF9naWZfYnlfaWQmY3Q9Zw/GsSgLaOAFo6RL1n41h/giphy.gif)

5. Set the server startup parameters.
 - I highly recommend going to [flags.sh](https://flags.sh/), installing the appropriate amount of RAM from your phone, leaving at least 0.5 GB of RAM for the system.

 Once downloaded, add to the file:
  ```
 cd MinecraftServer
 ```

 After the above, import the file into Termux with the following command:
  ```
 cp ~/storage/downloads/start.sh ~/ && chmod +x start.sh
 ```

<p>
  <img src="https://media0.giphy.com/media/v1.Y2lkPTc5MGI3NjExeTI5anZsbzZnb24xdTI1dGt0aDZ6ajVheDQ5M2wza2x6dDVqeGFjeiZlcD12MV9pbnRlcm5hbF9naWZfYnlfaWQmY3Q9Zw/8HpNYcY48ag9tUwZID/giphy.gif" alt="hippo" />
</p>

## The server is successfully installed and started with the command:
  ```
 ./start.sh
 ```
