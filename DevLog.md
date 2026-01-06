## 24 December 2025

Researched version control options for Unity
Decided on GitHub
Researched options for using GitHub on Unity
Got Repository set up for Blast Dodger
Got Unity upgraded to 6.3LTS
Got project set up in Unity
Shared status on social media. 

## 5 January 2026
Notes from AI conversation. (AI used Copilot)

### My prompt
If I want to create an ugly simple game by the end of April, what should I achieve by the end of the month, the end of next week, and tomorrow? The first one is code named blast dodger; it is an endless runner where you pilot a ship collecting resources for a mining consortium. And will be made in Unity, and will be a 2d game.

### AI Response
To finish **Blast Dodger** by **April 30**, here's a clear breakdown of what to accomplish by **tomorrow**, **end of next week**, and **end of January**. This pacing assumes you're working part-time in the evenings and aiming for a scrappy but playable release.

---

### ✅ By Tomorrow (Jan 3)
**Goal: Define the project scope and set up your Unity environment.**

- **Create a new Unity 2D project** named *Blast Dodger*.
- **Write a one-paragraph design brief** summarizing gameplay, controls, and goals.
- **Sketch a rough gameplay loop**: ship movement, resource collection, obstacle avoidance.
- **Decide on input methods**: keyboard for web, touch buttons for mobile.
- **Set up version control** (e.g., GitHub or Unity Collaborate).

---

### 🛠️ By End of Next Week (Jan 10)
**Goal: Build a playable prototype with core mechanics.**

- **Implement lane-switching controls** (3-lane movement).
- **Add basic shooting mechanic** with ammo tracking.
- **Create placeholder sprites** for ship, obstacles, fuel, and ammo.
- **Build a scrolling background** to simulate endless movement.
- **Spawn obstacles and pickups** randomly but fairly.
- **Add basic UI** for score, fuel, and ammo.

---

### 🚀 By End of January
**Goal: Polish core gameplay and prepare for testing.**

- **Add difficulty settings** (speed and speed ramping).
- **Implement cheat toggles** (infinite fuel/ammo, shield).
- **Balance resource spawning** to prevent soft-locks.
- **Add sound effects** for shooting, pickups, and crashes.
- **Build a main menu** with start, settings, and cheat options.
- **Test on mobile and web** to verify controls and performance.

---

Would you like help breaking February and March into similar sprint goals, or want a Trello-style board layout for tracking?


### My Prompt
Now, I'm not sure what you mean by "Sketch a rough gameplay loop: ship movement, resource collection, obstacle avoidance." Give me an example of what that means please.

### AI Response
Great question, Joseph — a **gameplay loop** is the repeating cycle of player actions and feedback that defines how your game feels moment to moment. For *Blast Dodger*, a rough gameplay loop sketch might look like this:

---

### 🔁 Core Gameplay Loop for *Blast Dodger*

1. **Player reads the lane ahead**  
   - Sees obstacles, fuel tanks, ammo crates, or empty space.

2. **Player chooses a lane**  
   - Taps one of three lane buttons to move the ship.

3. **Player reacts to threats**  
   - If an obstacle blocks the lane, they either dodge or shoot.

4. **Player manages resources**  
   - Collects fuel and ammo by moving into lanes with pickups.  
   - Avoids shooting pickups (which destroys them).

5. **Player earns points**  
   - Points for destroying obstacles, collecting resources, and surviving longer.

6. **Game speed increases**  
   - Over time, the scrolling gets faster, demanding quicker decisions.

7. **Player repeats the loop**  
   - Until they crash or run out of fuel/ammo.

---

This loop is what keeps the player engaged. It’s simple, but each cycle offers a chance to make a meaningful decision. You can sketch this out visually too — a flowchart with arrows between boxes like “See obstacle” → “Choose lane” → “Shoot or dodge” → “Collect or miss resource” → “Score” → “Repeat”.

Would you like me to help you diagram this loop or write it out in Unity pseudocode to guide your implementation?

### My Prompt
So, here is what I want in the game, there will be 4 buttons total. One button lets you fire. And the other 3 put you into one of 3 lanes. So, if you are in lane 1 and need to go to lane 3, you simply press the button for lane 3. The fuel and ammo tanks will be shootable, and will ideally make big booms when you do hit them. The mineral deposits will first need to be shot once, and then from there, you simply need to fly into them. Once you do, the mining station will transport the newly tagged minerals for processing. The game will have several cheat modes you can easily activate including unlimited fuel and ammo. There will be a few difficulty settings revolving both around how fast the ship flies, and how much (if at all) the speed of the ship increases as you progress through the game. For the challenge the game offers, you will be flying through a narrow channel of pipes scouting for ore and minerals that were brought to the surface. Randomly, 2 of the 3 lanes will be blocked by pipes jutting out from the side. Sometimes in the non-blocked opening, it will be open with nothing in it. Other times there will be an unopened mineral case (which you need to shoot to open), or fuel or ammo. Every 10 supply drops (negotiable depending on play experience) there will be a super supply drop that has both ammo and fuel to collect. I want 3 different scores, one for ammo collected, one for fuel collected, and one for minerals tagged. 
What additional info beyond that would I need to create both a one-paragraph design brief summarizing gameplay, controls, and goals and a rough gameplay loop: ship movement, resource collection, obstacle avoidance

### AI Response
You’re actually *very* close to having everything you need, Joseph. What you’ve written already covers the **core fantasy**, the **mechanics**, the **controls**, and the **moment‑to‑moment decisions**. To turn that into a clean one‑paragraph design brief and a rough gameplay loop, you only need a few missing pieces — the kind of details that clarify *tone*, *scope*, and *player expectations*.

Below is a simple checklist of what’s still needed, with each item highlighted so you can explore it further if you want.

---

## 🎯 Additional Info Needed for a One‑Paragraph Design Brief

A design brief is basically:  
**“What is this game, what does the player do, and why is it fun?”**

You already have 80% of that. The remaining pieces are small but important:

- **[Target platform(s)](guide://action?prefill=Tell%20me%20more%20about%3A%20Target%20platform(s))**  
  Web only? Mobile only? Both? This affects how you phrase controls and performance expectations.

- **[Tone and theme flavor](guide://action?prefill=Tell%20me%20more%20about%3A%20Tone%20and%20theme%20flavor)**  
  Is this gritty industrial sci‑fi, playful retro arcade, or clean minimalist? A brief needs a vibe.

- **[Player goal beyond survival](guide://action?prefill=Tell%20me%20more%20about%3A%20Player%20goal%20beyond%20survival)**  
  Is the goal simply “go as far as possible,” or is there a narrative wrapper like “complete a scouting run for the consortium”?

- **[Session length expectation](guide://action?prefill=Tell%20me%20more%20about%3A%20Session%20length%20expectation)**  
  Are runs meant to last 30 seconds, 2 minutes, or 10 minutes? This shapes difficulty pacing.

- **[Intended audience or purpose](guide://action?prefill=Tell%20me%20more%20about%3A%20Intended%20audience%20or%20purpose)**  
  Is this a practice project, a portfolio piece, or something you want to publish? It changes how you frame the brief.

Once you answer those, I can turn your description into a tight, polished paragraph that reads like a real design doc.

---

## 🔁 Additional Info Needed for a Rough Gameplay Loop

A gameplay loop is the **repeating cycle of actions** the player performs every few seconds. You’ve already described the mechanics beautifully. To turn that into a loop, I only need a few clarifications:

- **[What ends a run](guide://action?prefill=Tell%20me%20more%20about%3A%20What%20ends%20a%20run)**  
  Crash? Run out of fuel? Run out of ammo? All of the above?

- **[How scoring is surfaced](guide://action?prefill=Tell%20me%20more%20about%3A%20How%20scoring%20is%20surfaced)**  
  Are the three scores shown during gameplay, or only at the end?

- **[How fast the loop repeats](guide://action?prefill=Tell%20me%20more%20about%3A%20How%20fast%20the%20loop%20repeats)**  
  Do obstacles appear every second? Every two seconds? This defines the rhythm.

- **[Whether lane switching is instant or animated](guide://action?prefill=Tell%20me%20more%20about%3A%20Whether%20lane%20switching%20is%20instant%20or%20animated)**  
  Instant = snappy arcade feel. Animated = smoother but slower.

- **[Whether shooting has a cooldown](guide://action?prefill=Tell%20me%20more%20about%3A%20Whether%20shooting%20has%20a%20cooldown)**  
  This affects how often “shoot vs. dodge” appears in the loop.

- **[Whether the player can miss mineral cases after opening them](guide://action?prefill=Tell%20me%20more%20about%3A%20Whether%20the%20player%20can%20miss%20mineral%20cases%20after%20opening%20them)**  
  If yes, that adds a timing layer to the loop.

Once I have those, I can write a clean, structured gameplay loop like:

- **See obstacle → choose lane → shoot or dodge → collect or miss → update resources → repeat**  
…but tailored to your exact timing, pacing, and failure conditions.

---

## If you want, I can do the next step right now

Just tell me the missing pieces above, and I’ll produce:

- a **polished one‑paragraph design brief**, and  
- a **clear gameplay loop** you can drop straight into your design document.

Or, if you prefer, I can ask you the questions one by one.

### My prompt
The first version of the game will be web only built using Unity. It will be a 2D game. Though it will be web only, I will build in mobile friendly controls. When you start a game, you will have a mission you need to accomplish, and will earn a bonus for going above and beyond that mission. It will be an infinite runner game. 
The backstory to the world the game takes place on is the following (time tables subject to change). You are a contractor working for a major mining consorteum hired to help them collect minerals and such. The ships you fly are drones that you pilot remotely from your main ship (Less risk that way).
World: Krneal
Description
Krneal is a monstrous nightmare of machines, mines, and processing factories. The world's molten core literally produces precious metals, gems and other valuable materials. While the dwarves are not native to Krneal they were the first group to settle the world and from there started to mine its wealth out. 
 For more than 500 billion years the dwarves mined out the wealth of the world. They mined and mined until they carved out the entire crust and much of the mantle of the world leaving a mostly molten surface. The rivers, streams, lakes, seas and oceans have all been long since drained and forced into a massive network of pipes through which the residents are able to find water for drinking and more importantly for fueling the mining efforts. 
 When the pollution started to build up too much from all of the mining and near complete lack of plants on the world, some of those residents who do not have enough clout be let anywhere near the prime mining spots have even found ways to harvest the carbon dioxide out of the air, separate out the carbon and then use special machines to forge diamonds out of the carbon they harvest. From there when the value of their services was discovered it became a mandated process. Now, while breathable, the very air tastes machined and artificial. 
 No matter how much water they pour onto the molten surface of their world only to then mine off the newly solidified ground for precious materials the planet never shrinks any further. For nearly 100 billion years naysayers, and doom speakers have tried to convince the leaders and residents of the various parts of Krneal of the dangers of their course of action. 
 The mineral harvesting and mining process miles below the surface produce ample steam to power every last imaginable contraption and even leave enough moisture in the air to have an almost constant stream of rain pouring down upon the ever rusting machinery. In some of the more rundown parts of the world the machinery has rusted so badly some of it has started to wear away into dirt. Many of those that protest the mining effort hope to see all of the machinery on the surface turn to dirt where they can then start a normal life once more. 
Rain collectors and the pipes that carry the water to the mining sites and the steam away from are some of the most cared for pieces of machinery  in the whole of the world
Adventures services are in constant need on Krneal, as people try to reclaim long abandoned and even haunted sections of the world. The high pay and promise of endless loot rarely leaves a job unfilled. 
Druids, Nymphs, and other nature loving denizens hate everything Krneal represents.

### AI Response
This is rich worldbuilding, Joseph — and it gives *Blast Dodger* a tone and purpose that most “ugly simple games” never get. You’ve already done the heavy lifting. To finish your **design brief** and **gameplay loop**, only a few structural pieces were missing, and your latest message fills almost all of them.

Below is a clean breakdown of what you now have, what it enables, and what tiny bits you might still choose to define.

---

# 🌋 What You Already Provided (and how it maps to design‑doc needs)

### Core Game Identity
- **[2D web game built in Unity](guide://action?prefill=Tell%20me%20more%20about%3A%202D%20web%20game%20built%20in%20Unity)**
- **[Mobile‑friendly controls](guide://action?prefill=Tell%20me%20more%20about%3A%20Mobile%E2%80%91friendly%20controls)** even though it’s web‑only
- **[Four-button control scheme](guide://action?prefill=Tell%20me%20more%20about%3A%20Four-button%20control%20scheme)** (3 lanes + fire)
- **[Endless runner structure](guide://action?prefill=Tell%20me%20more%20about%3A%20Endless%20runner%20structure)** with missions and bonuses
- **[Resource management](guide://action?prefill=Tell%20me%20more%20about%3A%20Resource%20management)** (fuel, ammo, minerals)
- **[Three separate score tracks](guide://action?prefill=Tell%20me%20more%20about%3A%20Three%20separate%20score%20tracks)**

### World & Narrative
- **[Krneal’s industrial hellscape](guide://action?prefill=Tell%20me%20more%20about%3A%20Krneal%E2%80%99s%20industrial%20hellscape)**  
- **[Dwarven megastructure history](guide://action?prefill=Tell%20me%20more%20about%3A%20Dwarven%20megastructure%20history)**  
- **[Molten-core mineral production](guide://action?prefill=Tell%20me%20more%20about%3A%20Molten-core%20mineral%20production)**  
- **[Pollution, steam, rust, and artificial air](guide://action?prefill=Tell%20me%20more%20about%3A%20Pollution%2C%20steam%2C%20rust%2C%20and%20artificial%20air)**  
- **[Contractor working for a mining consortium](guide://action?prefill=Tell%20me%20more%20about%3A%20Contractor%20working%20for%20a%20mining%20consortium)**  
- **[Remotely piloted drones](guide://action?prefill=Tell%20me%20more%20about%3A%20Remotely%20piloted%20drones)**  
- **[Adventure services and dangerous abandoned zones](guide://action?prefill=Tell%20me%20more%20about%3A%20Adventure%20services%20and%20dangerous%20abandoned%20zones)**  

This is more than enough to write a polished design brief and a tight gameplay loop.

---

# 🧩 What Additional Info Would *Help* (Optional but useful)

You don’t *need* these to proceed, but answering them will make the brief and loop even sharper:

- **[Run-ending conditions](guide://action?prefill=Tell%20me%20more%20about%3A%20Run-ending%20conditions)**  
  Crash? Fuel depletion? Ammo depletion? All of the above?

- **[Lane-switch behavior](guide://action?prefill=Tell%20me%20more%20about%3A%20Lane-switch%20behavior)**  
  Instant teleport? Quick slide animation?

- **[Fire rate or cooldown](guide://action?prefill=Tell%20me%20more%20about%3A%20Fire%20rate%20or%20cooldown)**  
  Can the player spam fire, or is timing part of the challenge?

- **[Mission structure](guide://action?prefill=Tell%20me%20more%20about%3A%20Mission%20structure)**  
  Examples: “Tag 10 minerals,” “Collect 5 fuel tanks,” “Survive 60 seconds.”

- **[Session length target](guide://action?prefill=Tell%20me%20more%20about%3A%20Session%20length%20target)**  
  Are runs meant to last 1–2 minutes or longer?

- **[Visual tone](guide://action?prefill=Tell%20me%20more%20about%3A%20Visual%20tone)**  
  Retro pixel? Clean vector? Grimy industrial? Minimal placeholder art?

If you want, you can answer these quickly in bullet form and I’ll finalize everything.

---

# 📄 What I Can Produce Once You Confirm

### 1. A polished **one‑paragraph design brief**  
Something you can paste into your design doc, Steam page, or portfolio. It will summarize:
- the fantasy  
- the controls  
- the goals  
- the tone  
- the core loop  
- the mission structure  

### 2. A clean **gameplay loop**  
Presented as a readable sequence like:
- **[Scan lanes](guide://action?prefill=Tell%20me%20more%20about%3A%20Scan%20lanes)**  
- **[Choose lane](guide://action?prefill=Tell%20me%20more%20about%3A%20Choose%20lane)**  
- **[Shoot or dodge](guide://action?prefill=Tell%20me%20more%20about%3A%20Shoot%20or%20dodge)**  
- **[Collect or miss](guide://action?prefill=Tell%20me%20more%20about%3A%20Collect%20or%20miss)**  
- **[Update resources](guide://action?prefill=Tell%20me%20more%20about%3A%20Update%20resources)**  
- **[Repeat at increasing speed](guide://action?prefill=Tell%20me%20more%20about%3A%20Repeat%20at%20increasing%20speed)**  

---

If you want, I can draft both right now using the information you’ve already given — or you can answer the optional clarifying points above and I’ll tailor them even more tightly to your vision.


### My Prompt
For movement, ideally, I would like a quick slide animation, but I will take whatever is easiest. For the first version, I will just be using creatable assets inside of Unity, but eventually, I want a grimy industreal feel. The missions will always be to collect minerals. The gameplay by default will continue until either you crash (whether through running into something or running out of fuel), however you can always quit at any time. As I think about it, I think I want to skip the missions part, and add to the feel of being a contractor for a mining consorteum, so you will get the opportunity to select contracts you want to fulfil and will have a certain amount of time (not nessisarily in one run) to complete said contract. From there, upon completion of the contract, you will be awarded money of some kind that you can then use (in an update that will be released later) to purchase upgrades of varions sorts, what I am currently thinking is namely cosmetic upgrades, or maybe even a shield to protect you from a certain number of hits.


### AI Response
You’ve just given *Blast Dodger* a clear identity: a gritty industrial contract‑runner with simple controls, escalating tension, and long‑term goals. With what you’ve added, you now have everything needed to write both the **design brief** and the **gameplay loop**. I’ll give you both below, fully polished and ready for your design doc.

---

# 📄 One‑Paragraph Design Brief

*Blast Dodger* is a fast‑paced 2D endless‑runner built in Unity for the web, where you remotely pilot disposable mining drones across the molten, machinery‑scarred world of Krneal. Using a simple four‑button control scheme—three lane‑switch buttons and a fire button—you dodge jutting pipes, blast open mineral cases, and collect fuel, ammo, and valuable ore while navigating a narrow industrial channel. As a contractor for a massive mining consortium, you select timed contracts to fulfill across multiple runs, earning money for cosmetic upgrades and future defensive gear. Runs end when you crash or run out of fuel, but the grimy industrial atmosphere, escalating speed, and steady contract progression keep each attempt tense, rewarding, and replayable.

---

# 🔁 Core Gameplay Loop (Rough Sketch)

- **[Scan the three lanes ahead](guide://action?prefill=Tell%20me%20more%20about%3A%20Scan%20the%20three%20lanes%20ahead)**  
  Identify pipes, mineral cases, fuel tanks, ammo crates, or empty space.

- **[Choose a lane](guide://action?prefill=Tell%20me%20more%20about%3A%20Choose%20a%20lane)**  
  Tap one of the three lane buttons; the drone performs a quick slide animation into position.

- **[Decide whether to shoot or dodge](guide://action?prefill=Tell%20me%20more%20about%3A%20Decide%20whether%20to%20shoot%20or%20dodge)**  
  Fire to break mineral cases or destroy obstacles, or slide into a safe lane.

- **[Collect resources](guide://action?prefill=Tell%20me%20more%20about%3A%20Collect%20resources)**  
  Fly into opened mineral deposits, fuel tanks, and ammo crates; avoid shooting pickups unless you want the explosion.

- **[Update resource meters](guide://action?prefill=Tell%20me%20more%20about%3A%20Update%20resource%20meters)**  
  Fuel decreases over time; ammo decreases when firing; minerals increase when tagged.

- **[React to increasing speed](guide://action?prefill=Tell%20me%20more%20about%3A%20React%20to%20increasing%20speed)**  
  Difficulty ramps based on your chosen contract and settings.

- **[Repeat until crash or fuel depletion](guide://action?prefill=Tell%20me%20more%20about%3A%20Repeat%20until%20crash%20or%20fuel%20depletion)**  
  Runs end on collision or empty fuel, but contract progress persists across attempts.

---

# 🧱 What You’ve Locked In (and why it’s strong)

- **[Quick slide animation](guide://action?prefill=Tell%20me%20more%20about%3A%20Quick%20slide%20animation)** gives the game a tactile, physical feel without complicating controls.  
- **[Unity primitive assets for v1](guide://action?prefill=Tell%20me%20more%20about%3A%20Unity%20primitive%20assets%20for%20v1)** keep scope tight while letting you focus on mechanics.  
- **[Grimy industrial tone](guide://action?prefill=Tell%20me%20more%20about%3A%20Grimy%20industrial%20tone)** fits Krneal’s lore and gives you a clear art direction for later updates.  
- **[Contract system instead of missions](guide://action?prefill=Tell%20me%20more%20about%3A%20Contract%20system%20instead%20of%20missions)** adds long‑term goals and progression without forcing every run to be perfect.  
- **[Currency rewards](guide://action?prefill=Tell%20me%20more%20about%3A%20Currency%20rewards)** set you up for cosmetic upgrades, shields, and future systems.  
- **[Crash or fuel depletion as failure](guide://action?prefill=Tell%20me%20more%20about%3A%20Crash%20or%20fuel%20depletion%20as%20failure)** keeps the loop clean and intuitive.

This is exactly the kind of structure that makes a small game feel bigger than it is.

---

# 🔧 If you want next steps, I can help you build:

- **[A contract system spec](guide://action?prefill=Tell%20me%20more%20about%3A%20A%20contract%20system%20spec)** (UI, timers, rewards, progression)  
- **[A minimal Unity scene layout](guide://action?prefill=Tell%20me%20more%20about%3A%20A%20minimal%20Unity%20scene%20layout)** for your three‑lane runner  
- **[A milestone plan for January](guide://action?prefill=Tell%20me%20more%20about%3A%20A%20milestone%20plan%20for%20January)** to keep you on track for April  
- **[A simple slide‑animation implementation](guide://action?prefill=Tell%20me%20more%20about%3A%20A%20simple%20slide%E2%80%91animation%20implementation)** using Unity’s built‑in tools  

Which direction do you want to explore next?