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

![]()



