---
layout: default
title:  "Getting Started"
nav_order: 1
parent: General
grand_parent: Minecraft
permalink: /minecraft/general/getting-started/
tags: minecraft message motd color create creating configure configuring ip address connecting server icon installing eula
---
# Creating a Server
To create a Minecraft Java server, go to your Client Panel. On the left sidebar, choose Create Server. Type in all required information like server name, memory amount, and server location. Once done, click the Create button and wait at least a minute in the Client Panel for the new server to be created for your account. Now, in the [Game Panel](https://panel.falix.gg/) you should see the new server on your server list. If the server list indicates that it is still installing, wait at least 2 to 5 minutes for the installation to be complete. If the installation is taking longer than usual (over 5 to 10 minutes or more), head back to your [Client Panel](https://client.falix.gg/) and delete, then re-create the server. Select your new server and go to the Console tab, usually already selected by default. Click the Start button, located in the upper left corner of the Console tab. You're going to be selecting which type of server you want during the first startup of your new server. In this case, we're creating a Minecraft Java server, to select Minecraft Java, then the type of Minecraft Java server that you want like Vanilla or PaperMC, and select the version of Minecraft Java you want to play on. Your server should've crashed with the exit code "0" and with an error message that says "`You need to agree to the EULA in order to run the server. Go to eula.txt for more info.`". You will have to accept to [Mojang's EULA](https://account.mojang.com/documents/minecraft_eula) in order to start your server.

# Choosing Your Server Java Version
<!-- # What is Java? (An explantion for noobs will be added later on) -->
## Minecraft Versions
Use **Java 8** for Minecraft 1.12.2 or older

Use **Java 11** for Minecraft 1.13 or newer

Use **Java 16** for Minecraft 1.17 or newer

## Set a Default Version
> Make sure your server is turned off before doing the next steps.

To make a Java version the default one, so that you don't need to select it every time you start your server, visit the [game panel](https://panel.falixnodes.net/), find and click on your server, find the "Startup" page on the top bar, scroll down to "Variables", then find "JAVA VERSION" and type the following for:

## Java8
`adopt@1.8.0-275`

## Java11
`adopt@1.11.0-9`

## Java 16
`adopt@1.16.0-1`

Now, go back to your console, start your server and you'll see it using the Java version you set.

> If the above does not work, manually delete the `.jabba` folder and restart your server.

# Accepting Mojang's EULA
<!-- Who is Mojang? (An explantion for noobs will be added later on) -->
In order to start your server, you must accept [Mojang's EULA](https://account.mojang.com/documents/minecraft_eula). If you agree to it, go to your server's file manager, find and open the file "`eula.txt`", find the "`eula`" string and set it to `true`.

# Configuring
## Message of the Day
Also known as MOTD, is the message that shows up below the server name on a multiplayer server list. Usually used to say what's new about the server and/or also displaying what version it supports. Sometimes also used to indicate what games it has to offer or just a short description of the server.

To configure MOTD(Message of the Day), the setting for this is usually found in the server.properties file. Simply just change it to what you want for your Minecraft Java Server.

If you're interested in changing text colors, use these color codes:

<div id="color_table_mc" class="collapsable">
    <button onclick="openMenu_ColorMC();" id="open_ColorMC">View Colors <i class="fas fa-angle-up"></i></button>
    <button onclick="closeMenu_ColorMC();" id="close_ColorMC">Colors <i class="fas fa-angle-down"></i></button>
    <div id="cc_ColorMC" class="collapsable_content">
        <table>
        <tbody>
        <tr>
        <th id="black_color">COLOR_BLOCK</th>
        <th>Black</th>
        <th>\u00A70</th>
        </tr>
        <tr>
        <th id="dark_blue_color">COLOR_BLOCK</th>
        <th>Dark Blue</th>
        <th>\u00A71</th>
        </tr>
        <tr>
        <th id="blue_color">COLOR_BLOCK</th>
        <th>Blue</th>
        <th>\u00A79</th>
        </tr>
        <tr>
        <th id="dark_green_color">COLOR_BLOCK</th>
        <th>Dark Green</th>
        <th>\u00A72</th>
        </tr>
        <tr>
        <th id="green_color">COLOR_BLOCK</th>
        <th>Green</th>
        <th>\u00A7a</th>
        </tr>
        <tr>
        <th id="dark_aqua_color">COLOR_BLOCK</th>
        <th>Dark Aqua</th>
        <th>\u00A73</th>
        </tr>
        <tr>
        <th id="aqua_color">COLOR_BLOCK</th>
        <th>Aqua</th>
        <th>\u00A7b</th>
        </tr>
        <tr>
        <th id="dark_red_color">COLOR_BLOCK</th>
        <th>Dark Red</th>
        <th>\u00A70</th>
        </tr>
        <tr>
        <th id="red_color">COLOR_BLOCK</th>
        <th>Red</th>
        <th>\u00A7c</th>
        </tr>
        <tr>
        <th id="dark_purple_color">COLOR_BLOCK</th>
        <th>Dark Purple</th>
        <th>\u00A75</th>
        </tr>
        <tr>
        <th id="gold_color">COLOR_BLOCK</th>
        <th>Gold</th>
        <th>\u00A76</th>
        </tr>
        <tr>
        <th id="yellow_color">COLOR_BLOCK</th>
        <th>Yellow</th>
        <th>\u00A7e</th>
        </tr>
        <tr>
        <th id="light_purple_color">COLOR_BLOCK</th>
        <th>Light Purple</th>
        <th>\u00A7d</th>
        </tr>
        <tr>
        <th id="gray_color">COLOR_BLOCK</th>
        <th>Gray</th>
        <th>\u00A77</th>
        </tr>
        <tr>
        <th id="dark_gray_color">COLOR_BLOCK</th>
        <th>Dark Gray</th>
        <th>\u00A78</th>
        </tr>
        <tr>
        <th id="white_color">COLOR_BLOCK</th>
        <th>White</th>
        <th>\u00A7f</th>
        </tr>
        </tbody>
        </table>
    </div>
</div>

## Server Icon
The server icon helps indicate the branding of your Minecraft Java server, it's easy to set one. Simply create an icon that is 64x64 in resolution. Name the server icon as <u>server-icon.png</u> and add it to the root of your Minecraft Java server files.

## Player Limit

By default, Minecraft sets 20 as the max player limit for Minecraft Java servers. You can increase this, or decrease, to any number you want. To configure the player limit, the setting for this is usually found in the server.properties file. Simply, just change the number 20 to something else, you could also set -1 for unlimited.

# Setting Operators
An operator is a player with administrative access to your server, giving them full access to all commands. Even commands like /stop or /restart.
To set an operator, use:

```
/op Username
```

As an example, if you wanted to op Notch, you would use:

```
/op Notch
```

Please don't use `/` in the Console tab.

If you want to give some players access to specific admin commands, but not everything, you can use [LuckPerms](https://luckperms.net/) for this, which we recommend.

# Connecting
## Find your Server IP Address
In your [Game Panel](https://panel.falix.gg/) the IP is shown in the upper left on the Console tab. Use this to connect to your server.
If you're looking for the numeric IP, this usually shows up when booting the server.

## Play In-Game
On your Multiplayer server list, click Add Server, then put the IP for your server into the IP Address box. As for the Server Name, this can be set as whatever. Click Add and the server should appear on your list.