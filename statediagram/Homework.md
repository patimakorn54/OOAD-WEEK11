#นายปฏิมากร บุญเปลี่ยน  57030190

##State Diagram

รูปที่ 1 ตู้ ถอนเงิน ATM
```
Code
```
```
@startuml
state "Insert ATMCard" as incard
state "Insert Password" as inpass
state "Select Draw MOney" as select
state "Insert amount" as inamount
state "wait for money" as wait
state "receive money" as receive
state "receive ATMCard" as receiveatm
[*] --> incard
incard --> inpass
inpass --> select
select -Right-> inamount
inamount -Right-> wait
wait -up-> receive
receive -up-> receiveatm
receiveatm -up-> Finish
@enduml
```

![](https://github.com/patimakorn54/OOAD-WEEK11/blob/master/statediagram/1.png?raw=true)


รูปที่ 2 ตู้หยอดน้ำดื่ม
```
Code
```
```
@startuml
state "Drink water machine" as drink
state "Place a bottle" as place
[*] --> drink

state drink{
  [*] -> SelectVolumeWater
 SelectVolumeWater --> InsertCoin
 InsertCoin --> place
 place --> Recivewater 
@enduml
```

![](https://github.com/patimakorn54/OOAD-WEEK11/blob/master/statediagram/2.png?raw=true)


รูปที่ 3 ร้านกาแฟ
```
Code
```
```
@startuml

[*] --> Cafe
state Cafe{
state "Order Coffee" as order
state "wait a  Coffee" as wait
state "recive a  Coffee" as recive
  [*] -> order
 order -r-> cashmoney
 cashmoney -r-> wait
 wait  -r-> recive 
 }
@enduml
```

![](https://github.com/patimakorn54/OOAD-WEEK11/blob/master/statediagram/3.png?raw=true)


รูปที่ 4 ลงชื่อเข้าใช้ Internet
```
Code
```
```
@startuml 
state "Login to Internet" as login
[*] --> login
state login{
state "Connect to internet" as connect
state "Open Web Browser" as open
state "Insert Username and Password" as insert
state "Click 'Login'" as click
  [*] -> connect
 connect -u-> open
 open -r-> insert
 insert  -r-> click 
 }
@enduml
```

![](https://github.com/patimakorn54/OOAD-WEEK11/blob/master/statediagram/4.png?raw=true)


รูปที่ 5 พิมพ์เอกสาร
```
Code
```
```
@startuml 
state "Print Document" as Document
[*] --> Document
state Document{
state "Open Office word" as open
state "Key Data to Document" as key
state "Save Data File" as save
state "Select size paper" as select
state "Print to paper" as print
  [*] -> open : Open Program
 open -u-> key :
 key -r-> save
 save  -r-> select 
 select  -r-> print
 }
@enduml
```

![](https://github.com/patimakorn54/OOAD-WEEK11/blob/master/statediagram/5.png?raw=true)


##Activity Diagram



รูปที่ 6 พิมพ์เอกสาร
```
Code
```
```
@startuml
(*) --> "Insert Password"

if "Key Password" then
  -->[true] "Open Windows"
  --> (*)
else
  ->[false] "Insert Again"
  -->(*)
Endif
@enduml
```

![](https://github.com/patimakorn54/OOAD-WEEK11/blob/master/statediagram/6.png?raw=true)


รูปที่ 7 พิมพ์เอกสาร
```
Code
```
```
@startuml
(*) --> "Calender"

if "24 Hr." then
  -->[true] "Change Date"
  --> (*)
else
  ->[false] "Stay Date"
  -->(*)
Endif
@enduml
```

![](https://github.com/patimakorn54/OOAD-WEEK11/blob/master/statediagram/7.png?raw=true)



รูปที่ 8 พิมพ์เอกสาร
```
Code
```
```
@startuml
(*) --> "Sell Ticket"

if "Have Money" then
  -->[true] "Buy Ticket"
  --> (*)
else
  ->[false] "Not Sell Ticket"
  -->(*)
Endif
@enduml
```

![](https://github.com/patimakorn54/OOAD-WEEK11/blob/master/statediagram/8.png?raw=true)



รูปที่ 9 พิมพ์เอกสาร
```
Code
```
```
@startuml
(*) --> "Drive Car"

if "Fuel Full" then
  -->[true] "Drive"
  --> (*)
else
  ->[false] "Fuel Fill"
  -->(*)
Endif
@enduml
```

![](https://github.com/patimakorn54/OOAD-WEEK11/blob/master/statediagram/9.png?raw=true)




รูปที่ 10 พิมพ์เอกสาร
```
Code
```
```
@startuml
(*) --> "Room Computer"

if "Have Member card" then
  -->[true] "Use Rooom Computer๊"
  --> (*)
else
  ->[false] "Register Member Card"
  -->(*)
Endif
@enduml
```

![](https://github.com/patimakorn54/OOAD-WEEK11/blob/master/statediagram/10.png?raw=true)

