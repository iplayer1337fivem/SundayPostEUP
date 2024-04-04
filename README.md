# SundayPostEUP
Some working clothes in thew style of Sheep map, and suitable for the job of Lamark

![Sunday Post Logo](https://users-cdn.versescripts.net/99f8073f5323184bed29a1c6de00ff12.png)

![FEMALE CLOTHES SNEAKPEAK](https://i.postimg.cc/QVFnDG4g/Rottenberger-sheep-eup-icecream-Female.gif)

![MALE CLOTHES SNEAKPEAK](https://i.postimg.cc/sMrn5BVK/Rottenberger-sheep-eup-icecream-Male.gif)


[MLO made of Sheep -](https://github.com/cmgjones1231/Sheep-FreeReleases)
Vehicle made of Sheep^^^^^^^

![SHEEP MAPPING](https://users-cdn.versescripts.net/0c6acfaf9892140d82e556380b0de4b0.gif)
**SHEEP DISCORD - PLEASE GO SUPPORT [SHEEP DISCORD](https://discord.gg/EbRHb2sy)

You will just need to change some coordinates. I will put in the files ASAP.
[Job script for QB/OX made of Lusty94 -](https://github.com/Lusty94/lusty94_icecream)


[EUP made of Rottenberger - you are here currently - but for future reference : ](https://github.com/iplayer1337fivem/SundayPostEUP/)



**Tribute to the Creators and Contributors**

In the vibrant world of the FiveM community, where creativity knows no bounds and innovation thrives, there's a special place reserved for those who envision, build, and nurture. Today, we pay homage to the creators who laid the foundation and the contributors who breathe life into our shared virtual spaces.

To the creators, whose visionary spirit sparked the inception of this community, we owe a debt of gratitude. Your tireless efforts, unwavering dedication, and boundless imagination have paved the way for countless adventures, friendships, and memories. From the first lines of code to the intricate designs, your passion resonates in every corner of our digital realm.

And to those who contribute, like myself, our journey is one of shared passion and collective growth. Each line of code, every suggestion, and the smallest of tweaks is a testament to our commitment to making this community thrive. It's not just about the contributions themselves, but the camaraderie, the shared laughs, and the joy of collaborating with like-minded individuals.

As I reflect on my own role in this community, I can't help but feel grateful for the opportunity to be part of something bigger than myself. My contribution may be just a partition in the grand symphony of creativity, but it's a partition made with love, enthusiasm, and a deep appreciation for the vibrant spirit of collaboration that defines the FiveM community.

To the creators and contributors alike, I extend my heartfelt thanks. Your passion, dedication, and creativity inspire us all to reach greater heights and forge stronger bonds within our beloved community.

Here's to the creators, the contributors, and the spirit of collaboration that makes the FiveM community truly special.

With sincere appreciation,

**Rottenberger**

 [FiveM Social](https://fivem.social/@advancedroleplay)  
 - start your server profile or character profile today, its free forever. Free img hosting and changelog in serverlist features <3
 
 [My Roleplay discord](https://discord.com/invite/advancedroleplay) - Upcomming server 03/04-2024

 [My GraphicStore](https://discord.gg/6W4jGY8B) - Feel free to join - I specialize into customizing GIFs <3


 04.04.24 - update since I got told the other script was a ripoff, then we might aswell send you to a script made of the original creator. I will provide coordinates in files asap.
 Until then, here is the coordinates. you can c/p If you do it before me.

--
		       label = "Sunday Post", -- Set this to the required job
        zones = {
          vector2(-1197.3486328125, -1538.5164794922),
          vector2(-1191.2731933594, -1534.2912597656),
          vector2(-1188.7746582031, -1537.8775634766),
          vector2(-1185.3186035156, -1543.2625732422),
          vector2(-1183.9841308594, -1545.1079101562),
          vector2(-1189.3872070312, -1549.2679443359)
        },
		blip = vector3(-1190.44, -1542.65, 4.39),
		blipcolor = 48,
--

job info
icecream = {
	label = 'Sunday Post',
	type = 'icecream',
	defaultDuty = true,
	offDutyPay = false,
	grades = {
		['0'] = { name = 'Recruit', payment = 150 },
		['1'] = { name = 'Novice', payment = 200 },
		['2'] = { name = 'Experienced', payment =225 },
		['3'] = { name = 'Advanced', payment = 250 },
		['4'] = { name = 'Manager', isboss = true, payment = 250 },
	},
},

--
--STASHES
	exports['qb-target']:AddBoxZone("CreamPrepared", vector3(-1192.04, -1541.45, 5.36), 2.0, 2.5, { name="CreamPrepared", heading = 32.22, debugPoly=Config.Debug, minZ=4.36, maxZ=6.36 },
		{ options = { {  event = "amari-icecreamshop:Stash", icon = "fas fa-box-open", label = "Storage", stash = "Shelf" }, },  distance = 2.0 })
    --CLOCKIN
	exports['qb-target']:AddBoxZone("CreamClockin", vector3(-1190.28, -1546.52, 4.39), 3.5, 0.5, { name="CreamClockin", heading = 217.86, debugPoly=Config.Debug, minZ=3.6, maxZ=6.6 },
    	{ options = { { type = "server", event = "QBCore:ToggleDuty", icon = "fas fa-user-check", label = "Toggle Duty", job = "icecream" }, }, distance = 2.0 })
	--PAYMENTS
    exports['qb-target']:AddBoxZone("CreamReceipt", vector3(-1188.03, -1542.1, 5.86), 0.5, 0.5, { name="CreamReceipt", heading = 217.86, debugPoly=Config.Debug, minZ = 3.86, maxZ = 7.86, },
		{ options = { { event = "jim-payments:client:Charge", icon = "fas fa-credit-card", label = "Charge Customer", job = "icecream" }, }, distance = 2.0 })
    --TRAYS
	exports['qb-target']:AddBoxZone("CreamCounter", vector3(-1192.99, -1543.2, 5.6), 0.6, 0.6, { name="CreamCounter", heading = 122.89, debugPoly=Config.Debug, minZ=3.6, maxZ=6.6 },
    	{ options = { { event = "amari-icecreamshop:Stash", icon = "fas fa-hamburger", label = "Open Counter", stash = "Counter" }, }, distance = 2.0	})
	--FRIDGE
	exports['qb-target']:AddBoxZone("CreamFridge", vector3(-1189.7, -1543.21, 5.8), 3.5, 0.5, { name="CreamFridge", heading = 213.73, debugPoly=Config.Debug, minZ = 3.8, maxZ = 7.8, },
		{ options = { {  event = "amari-icecreamshop:Stash", icon = "fas fa-temperature-low", label = "Open Fridge", stash = "Fridge", job = "icecream" }, }, distance = 2.0 })
    --WARESTORAGE
	exports['qb-target']:AddBoxZone("CreamStorage", vector3(-1191.17, -1543.78, 4.39), 4.0, 1.5, { name="CreamStorage", heading = 217.86, debugPoly=Config.Debug, minZ=3.6, maxZ=6.6 },
		{ options = { {  event = "amari-icecreamshop:Shop", icon = "fas fa-box-open", label = "Open Store", job = "icecream" }, }, distance = 2.0 })
	--ICECREAM MAKER
	exports['qb-target']:AddBoxZone("CreamHob", vector3(-1189.1, -1538.98, 4.39), 1.5, 0.6, { name="CreamHob", heading = 43.05, debugPoly=Config.Debug, minZ=2.39, maxZ=6.39 },
		{ options = { { event = "amari-icecreamshop:Menu:Hob", icon = "fas fa-temperature-high", label = "Use Ice Cream Churner", job = "icecream" }, }, distance = 2.5 })	
end)
--








 
 




