
# dogemap-api-code (documentation)

This is the dogemap API no api keys needed but abuse and we can remove.

# The api parameters

## function

example: **https://dogemap.cf/api/?function=ping**

output:

    {"ping":"pong"}

Other parameters will be listed on there respected function.

# The functions of dogemap
the core of it all.


### ping

Ping is used to check if you can connect to the server.

example: **https://dogemap.cf/api/?function=ping**

output:

    {"ping":"pong"}
### listalllocations
This function lists all the locations of dogemap with there respected json, IDS, etc.
example: **https://dogemap.cf/api/?function=listalllocations**

output: `[{"0":"48","ID":"48","1":"SCAN Computers","name":"SCAN Computers","2":"Store stocking PCs, hardware and components, plus software, gaming consoles and audio equipment.","description":"Store stocking PCs, hardware and components, plus software, gaming consoles and audio equipment.","3":"25-28 Enterprise Park, Middlebrook, Horwich, Bolton BL6 6PE","address":"25-28 Enterprise Park, Middlebrook, Horwich, Bolton BL6 6PE","4":"Shop","category":"Shop","5":"-2.5409226417541504","long":"-2.5409226417541504","6":"53.58420181274414","lat":"53.58420181274414","7":"scan.co.uk","website":"scan.co.uk"},{"0":"49","ID":"49","1":"Csoftware","name":"Csoftware","2":"Software company that develops software like dogemap.","description":"Software company that develops software like dogemap.","3":"waltham chase","address":"waltham chase","4":"other","category":"other","5":"-1.2005596160888672","long":"-1.2005596160888672","6":"50.93511199951172","lat":"50.93511199951172","7":"csoftware.cf","website":"csoftware.cf"}]` (shortened to save space)

output parms:
ID
name
address
long
lat
category

### addtomap
add to map is to add a new location to the dogemap system.

example: **https://dogemap.cf/api/?function=addtomap&company=(name)&description=(description)&address=(address in a URL format)&website=(website without http:// or https://)&category=(category)**


# Issues and how to resolve them.


i get this error `This location dosent exist according to OSM check the address and try again try removing the house number or unit number and place the full address in the description the address box is for the address but also the lat and lon.` How do i fix this?

This is due to OSM(Open street maps) not regonizing the address in question try removing the house number or unit number and see if it works with that exclusively if not try filtering it more by keeping the street and the city.

I get errors relating to a parameter being missing (`You are missing a required parameter.`) how do i fix this?

Check if you have all the parameters that are required in your code if one is missing it will not function and will output a error saying that its missing check the documentation and check your code and see if you are missing something if not check the request method it could be because its either a POST request or a GET request when it needs to be the other way round.

## If your error or issue isnt here you can submit using the issue reporter.
