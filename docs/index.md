[Roblox]: https://www.roblox.com
# Introduction #
Welcome to the **The Roblox CAuth Project**!
### About
CAuth is a Roblox Module that enables Debug features and gives you an out-of-the-box experience. These Debug features are used by the developers of Roblox Games to track and provide details of Guis, Players and more.

CAuth is exclusive only to the Roblox Default Developer Console. CAuth can also be customized to the Developer's Choice. CAuth checks for ``Enabled`` Property in Guis.

### Construction

Creating a new setting(s) and linking is as simple as:
``` lua
local VarName = Value

-- And in the return part
return Var1, Var2, YourVar
-- make sure to put it in the correct order
```
And Defining in In the Client Script.

``` lua
local Var1, Var2, YourVar = GetStatusRF:InvokeServer() -- make sure that you do NOT change The Value of the line.
```
And Coding the function of the Setting(s).
``` lua
if YourVar == true then
  -- put your desired code here
end
```
!!! info
  Remember to put the If Statement inside of the CAuth Function then in the ``mastere`` `if` statement.
