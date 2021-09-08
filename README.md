# Compile on Android using Termux

1. First Download  <a href="https://f-droid.org/en/packages/com.termux/">Termux from F-Droid</a> as the Playstore version is no longer maintained and install on your android device.

2. Either type the commands below directly into the Termux terminal on the device or SSH into it. 

3. Download the config file into the same directory rename it and modify your algo and pool details

4. Be careful you may damage your device or overheat. USE AT YOUR OWN RISK! 

***
PASTE THE FOLLOWING INTO THE TERMINAL:

1. Install all the everything required
`apt update && apt upgrade &&
apt install -y git wget proot build-essential cmake libmicrohttpd &&
git clone https://github.com/RabbitGray/Custom-xmrig --depth 1 &&
mkdir xmrig/build &&
cd xmrig/build &&
cmake -DWITH_HWLOC=OFF .. &&
make -j10`

2. Download example config file 
`wget https://github.com/RabbitGray/Custom-xmrig/blob/master/example_android_config.conf`

3. Rename config file
`mv example_android_config.conf config.json`

4. Edit the config file 
`nano config.json` 
<img src="https://github.com/RabbitGray/Custom-xmrig/blob/e50bd264d969a88ce550dc1be4b531339d9544a8/doc/Screenshot_modify_settings.jpg" width="400" height="900">

***

5. Now let's start mining! 
`./xmrig --config config.json`
<img src="https://github.com/RabbitGray/Custom-xmrig/blob/e50bd264d969a88ce550dc1be4b531339d9544a8/doc/Screenshot_android_mining.jpg" width="400" height="900">



## Working Devices Tested
Oppo F9
Firestick 4k





## Forked from Original Developers
* **[xmrig](https://github.com/xmrig)**
* **[sech1](https://github.com/SChernykh)**

