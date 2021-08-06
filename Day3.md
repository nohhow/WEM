# 3일

## Tab Bar
## Import Export
## Fragment
## User Enrollment

Tab Bar로 넘겼을 때, Alert(경고) 무시후 Save 진행 가능 Issue

0ad9fd058f1bf54328f9543c85144b2ae9ae25a6


c87e3764904a7b863aecc03051b3e32b9a35ec8a

DB 5f41e1795a44f3f7869cd89b0a1f478df27698a7


test1 salt : 27&a6TApgENof:AK33j.?5uny5&n9AoB
test1 hash : 5f41e1795a44f3f7869cd89b0a1f478df27698a7

login test1 hash : b6acf0127d0bc8bb8099a3ffc5caf4388afd60a2


[Temp.TempId] in ([Users.UserId] of [Users] where [4854983: ID] < 2000000000) 
and
(PBKDF2([Temp.TempPass], (([Users.Salt] of [Users] where [4854983: ID] < 2000000000 and [Users.UserId] = [Temp.TempId])+[Settings.Pepper])) in ([Users.PasswordHash] of [Users] where [4854983: ID] < 2000000000 and [Users.UserId] = [Temp.TempId]))

#현장실습