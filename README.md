# CF-lean


Requirements:
QB-Target

If you are using the locations I made, use the MLOs I sent


Drug Script 
['lean'] 		 		 = {['name'] = 'lean', 			 			['label'] = 'Lean', 				['weight'] = 200, 		['type'] = 'item', 		['image'] = 'images/lean.png', 			['unique'] = false, 	['useable'] = true, 	['shouldClose'] = true,	   ['combinable'] = nil,   ['description'] = 'Time to get fucked up'},

['styrofoamcups'] 		 = {['name'] = 'styrofoamcups', 			['label'] = 'Styrofoam Cups', 		['weight'] = 200, 		['type'] = 'item', 		['image'] = 'images/styrofoamcups.png', ['unique'] = false, 	['useable'] = false, 	['shouldClose'] = true,	   ['combinable'] = nil,   ['description'] = 'Used for drinks'},

['promethazine'] 		 = {['name'] = 'promethazine', 			    ['label'] = 'Promethazine', 		['weight'] = 800, 		['type'] = 'item', 		['image'] = 'images/promethazine.png', 	['unique'] = false, 	['useable'] = false, 	['shouldClose'] = true,	   ['combinable'] = nil,   ['description'] = 'Suppose to be used when people are sick'},

['codeine'] 		 	 = {['name'] = 'codeine', 			  		['label'] = 'Codeine', 				['weight'] = 800, 		['type'] = 'item', 		['image'] = 'images/codeine.png', 		['unique'] = false, 	['useable'] = false, 	['shouldClose'] = true,	   ['combinable'] = nil,   ['description'] = 'Relieve some pain'},

['coughsyrup'] 			 = {['name'] = 'coughsyrup', 			    ['label'] = 'Cough Syrup', 			['weight'] = 400, 		['type'] = 'item', 		['image'] = 'images/coughsyrup.png', 	['unique'] = false, 	['useable'] = false, 	['shouldClose'] = true,	   ['combinable'] = nil,   ['description'] = 'Main Ingredient'},

['sprite'] 				 = {['name'] = 'sprite', 			    	['label'] = 'Sprite', 				['weight'] = 300, 		['type'] = 'item', 		['image'] = 'images/sprite.png', 		['unique'] = false, 	['useable'] = true, 	['shouldClose'] = true,	   ['combinable'] = nil,   ['description'] = 'Tasty Drink'},


Add this into your qb-shops
1. Go to Config.lua
2. Config.Products
3. Copy this code


 [13] = {
            name = "styrofoamcups",
            price = 2,
            amount = 50,
            info = {},
            type = "item",
            slot = 13,
        },
4. Place it into Config.Products = {
["normal"] = {
    
}
}


Add this in qbcore/server/player.lua
around line 80
PlayerData.metadata['drugxp'] = PlayerData.metadata['drugxp'] or 0 -- Added for lean or drug you wish to make.

Go to qb-drugs/config.lua

and go to Config.CornerSellingDrugsList{
    "lean"
}
 then go to 
 Config.DrugsPrice{

     ["lean"] = {
        min = 400,
        max = 500,
    },
 }

 Go to Dpemotes/client/animationlist.lua
 then to DP.Emotes{

 }
 and this inside DP.Emotes
    ["drinklean"] = {"mp_player_intdrink", "loop_bottle", "Drink", AnimationOptions =
   {
        Prop = "v_ret_gc_cup",
        PropBone = 18905,
        PropPlacement = {0.12, 0.008, 0.03, 240.0, -60.0},
        EmoteMoving = true,
        EmoteLoop = true,
   }},

**About Our Server**

Welcome to our server! We proudly operate on our dedicated servers, catering to a community of over 200+ players. Our unique scripts set us apart, offering an exclusive experience unavailable elsewhere.

Key Features:

Custom Scripts: Uniquely crafted scripts tailored to enhance gameplay.
Established Services: Our server boasts a well-established Police Enforcement, EMS Staff, and ongoing development of our Fire Department.
Player-Driven Development: We prioritize player feedback to create innovative scripts, some of which set new standards in the gaming community.
Innovative Gameplay: Experience our homeless script, enabling players to engage in activities like begging for money, playing music with boxes, and embodying the role of a homeless character. Additionally, you can run your own business or engage in window wiping activities.
At our server, we're committed to providing an immersive and diverse experience for all our players. Join us and explore the endless possibilities in our dynamic gaming environment!

**Contributions We welcome contributions from the community! If you'd like to contribute, please follow these guidelines:**

Fork the repository.

Create your branch: git checkout -b feature/yourchoice.

Commit your changes: git commit -m 'Added some [feature]'.

Push to the branch: git push origin feature/yourchoice.

Open a pull request.
