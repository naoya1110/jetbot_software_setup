# JetBot Software Setup

This is the instruction for setting up JetBot software in NCKU-NITKC AI Robotics Lab.

YouTube: https://youtu.be/qC0zNpWyClw


## Get balenaEtcher
1. visit https://www.balena.io/etcher/
1. download and install balenaEtcher application to your PC.

## Get JetBot SD Card Image
1. visit https://jetbot.org/master/software_setup/sd_card.html
1. download [SD card image for Jetson Nano 4GB](https://drive.google.com/file/d/1o08RPDRZuDloP_o76tCoSngvq1CVuCDh/view?usp=sharing) to your PC

## Write JetBot Image on MicroSD Card
1. Insert a microSD card into your PC.
1. Launch balenaEtcher application.
1. Select the JetBot image and the target SD card on the app.
1. Flash!

## Boot JetBot
1. Insert the microSD card into the Jetson Nano on the JetBot.
1. Connect a monitor and a keyboard to the Jetson Nano.
1. Turn on the JetBot.
1. Log in using the user `jetbot` and the password `jetbot`

## Connect JetBot to WiFi
1. Check available WiFi using the following command with the password `jetbot`
    ```
    $ sudo nmcli device wifi list
    ```
1. Connect to a WiFi using the following command. The IP address of the JetBot appears on the OLED display when the WiFi connection is established.
    ```
    $ sudo nmcli device wifi connect <SSID> password <PASSWORD>
    ```

## Reboot JetBot without Monitor and Keyboard
1. Shutdown the JetBot.
    ```
    $ sudo shutdown now
    ```
1. Turn off the JetBot
1. Remove the monitor and the keyboard from the JetBot
1. Turn on the JetBot. Now the JetBot will be connected to the WiFi automatically.

## Remote Access to JetBot with Web Browser
1. Check the IP address shown on the OLED display.
1. Open a web browser and navigate to `http://<jetbot_ip_address>:8888`
1. Log in to the jupyter lab with the password `jetbot`

## Additional Setups
1. Open a terminal from Launcher.
1. Update apt package list.
    ```
    $ apt update
    ```
1. Install SSH.
    ```
    $ apt install ssh
    ```

## Shutdown JetBot from Web Browser
1. Open a terminal
1. Log in to the JetBot with SSH.
    ```
    $ ssh jetbot@0.0.0.0
    ```
1. Shutdown the JetBot.
    ```
    $ sudo shutdown now
    ```




