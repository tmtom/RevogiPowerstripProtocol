# Device config files

Accessible via `telnet`.

## /home/switch/config

```bash
DEV_NAME=MyPowerStrip
PORT1_NAME=Port 1
PORT2_NAME=PORT 2
PORT3_NAME=PORT 3
PORT4_NAME=PORT 4
PORT5_NAME=PORT 5
PORT6_NAME=PORT 6
ZONE=1
RECORD_DATE=2013-12-26,09:10:55
REG_ID=rvg012345678
BIND=1
SLAVE_SERVER=lon.revogi.net
SLAVE_PORT=5000
ANTI=
```

## /etc/dev

```bash
DEV_SN=SWW0123456789012
DEV_SAK=333444555666
DEV_MAC=001122334455
```

## /etc/wlan

```bash
[default]
WLAN_MODE=2
WLAN_SECURITY=5
```

## /etc/wlan0_cfg_file.conf

```bash
[default]
### Operating mode configurable ###
#AP:0 CLIENT:1 REPEATER:2
BASE_MODE=1

#11B:1 11G:2 11BG:3 11N:8 11GN:10
#eg:11BGN=11GN+11B
BASE_BAND=11

#Operation frequency used.
#0 for auto channel.
#1-14 for 11b/11g.
#36-165 for 11a.
BASE_CHANNEL=0

#INFRASTRUCTURE:0 ADHOC:1
BASE_NETWORK_TYPE=0

#AP:Access point essid name.
#CLIENT:Connect essid name.
#ANY or any mean scan ap node, Max 32 bytes.
BASE_SSID=ssid_02

#Adhoc default ssid,Max 32 bytes.
#If don't give SSID in Ad -hoc client mode and no IBSS available, it will start an IBSS with SSID given here.
BASE_DEFAULT_SSID=

#Hidden AP.
#DISABLE:0 ENABLE:1
BASE_HIDDEN_SSID=0

#Guest access privilege.
#DISABLE:0 ENABLE:1
BASE_ACCESS=0

### Encryption and auth configurable ###
#Encryption mode.
#DISABLE:0 WEP:1 WPA:2 WPA2:4 WPA/WPA2:6
BASE_ENCRYPT=4

#802.11 Authentication type.
#OPEN SYSTEM:0 SHARED KEY:1 AUTO:2
BASE_AUTH_TYPE=2

### WEP key configurable ###
#DISABLE:0 WEP64:1 WEP128:2
WEP=0

#10 hex digits,Type of byte array.
WEP64_KEY1=0000000000
WEP64_KEY2=0000000000
WEP64_KEY3=0000000000
WEP64_KEY4=0000000000

#26 hex digits,Type of byte array.
WEP128_KEY1=00000000000000000000000000
WEP128_KEY2=00000000000000000000000000
WEP128_KEY3=00000000000000000000000000
WEP128_KEY4=00000000000000000000000000

#WEP default Tx key.
#array[0~3]
WEP_DEFAULT_KEY=0

### WPA key configurable ###
#RADIUS:1 PSK:2
WPA_AUTH=2

#WPA PSK cipher suite
#TKIP:1 AES:2 MIXED:3
WPA_CIPHER_SUITE=2

#WPA2 PSK cipher suite
#TKIP:1 AES:2 MIXED:3
WPA2_CIPHER_SUITE=2

#PSK key.
#Max 32 characters.
WPA_PSK=secret_wifi_password

#Group key update time.
#Time unit is second.
WPA_GROUP_REKEY_TIME=86400
```

