# gogaudrian-powershell
$onoff = read-host -prompt "Gogaurdian On or Off"

$onoffoptions = @(

"on"

"off"

)

If ($onoff -eq "on") {

move-item -path "C:\Users\\:):)\AppData\Local\Microsoft\Edge\User Data\Default\Extensions\haldlgldplgnggkjaafhelgiaglafanh" -destination "C:\Users\\:):)\AppData\Local\Microsoft\Edge\User Data\Default"; rename-item "C:\Users\\:):)\AppData\Local\Microsoft\Edge\User Data\Default\Extensions\haldlgldplgnggkjaafhelgiaglafanhE" -newname "haldlgldplgnggkjaafhelgiaglafanh"; get-process -name msedege | stop-process

}

if ($onoff -eq "off") {

rename-item -path "C:\Users\\:):)\AppData\Local\Microsoft\Edge\User Data\Default\Extensions\haldlgldplgnggkjaafhelgiaglafanh" -newname "haldlgldplgnggkjaafhelgiaglafanhE"; move-item -path "C:\Users\\:):)\AppData\Local\Microsoft\Edge\User Data\Default\haldlgldplgnggkjaafhelgiaglafanh" -destination "C:\Users\\:):)\AppData\Local\Microsoft\Edge\User Data\Default\Extensions"; get-process -name msedge | Stop-Process

}

if ($onoff -notin $onoffoptions) {

Write-Host "ERROR: You must pick exactly on or off, if you put anything else it will be ignored and nothing will happen..."
Write-Host " "

}

$clearhostoptions = @(

"y"

"n"

)

$clearhost = read-host -prompt "clear terminal (enter y or n)"

if ($clearhost -eq "y") {
clear-host

}

if ($clearhost -notin $clearhostoptions) {
Write-Host "ERROR: You must put exactly y or n, if you put anything else it will be ignored and nothing will happen"

}
