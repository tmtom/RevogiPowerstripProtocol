# Commands

Using bogus data:

- SN `SWW0123456789012`
- MAC `00:11:22:33:44:55`
- sak `333444555666`
- regid `rvg012345678`

## HTTP commands

### Command 1 - configure wifi client connection

Configure wifi client connection - SSID, password, mode

### Command 2 - wifi scan

Scan wifi and get list of "visible" AP SSIDs together with signal strength and mode.

### Command 5 - register to cloud server

Configure Server URL, registration ID

## Websocket commands

### Command 2 - cloud server regitrsation/redirect??

### Command 3 - check fw version/fw upgrade??

Socket to cloud report FW version and SAK??


`V3{"sn":"SWW0123456789012","cmd":3,"sak":"333444555666","ver":"3.49","ip":"192.168.2.200","mac":"00:11:22:33:44:55"}`

`V3{"code":200,"newver":"3.49","url":"","checksum":0,"time":1729363966,"response":3,"cmd":3,"sn":"SWW0123456789012"}`


### Command 4 - ??


`V3{"sn":"SWW0123456789012","cmd":4,"mac":"00:11:22:33:44:55","sak":"333444555666"}`

### Command 5 - rules??

Socket to cloud report rules???

`V3{"sn":"SWW0123456789012","cmd":5,"page":0,"rule":[]}`

`V3{"code":200,"response":5,"page":0,"cmd":5,"sn":"SWW0123456789012"}`


### Command 7 - switch port??

`V3{"sn":"SWW0123456789012","cmd":7,"en":1,"port":[0,0,1,0,0,0]}`

`V3{"code":200,"port":[0,0,1,0,0,0],"response":7,"en":1,"sn":"SWW0123456789012","cmd":7}`

### Command 10 - report status (switch, watt, amp)??

Socket reports every minute its state to the cloud?

`V3{"sn":"SWW0123456789012","cmd":10,"ip":"192.168.2.125","isTime":1,"time":1729285153,"zone":8,"switch":[1,0,0,0,0,0],"watt":[0,0,0,0,0,0],"amp":[0,0,0,0,0,0]}`

`V3{"code":200,"response":10,"cmd":10,"sn":"SWW0123456789012"}`

### Command 20 - switch socket/port on/off

Cloud requests socket port switch

`V3{"protocol":3,"sn":"SWW0123456789012","port":0,"state":0,"cmd":20}`

`V3{"response":20,"code":200,"sn":"SWW0123456789012","sak":"333444555666"}`

### Command 26 - ???

`V3{"en":1,"port":[0,0,1,0,0,0],"cmd":26,"sn":"SWW0123456789012"}`

`V3{"response":26,"code":200,"sn":"SWW0123456789012","sak":"333444555666"}`

### Command 30

`V3{"protocol":3,"sn":"SWW0123456789012","op":2,"cmd":30}`

### Command 50 - sync???

Cloud to socket

`V3{"sn":"SWW0123456789012","cmd":50,"sync":10}`

`V3{"response":50,"code":200,"sn":"SWW0123456789012","sak":"333444555666"}`


## From doc only

### Command 90 - query status
