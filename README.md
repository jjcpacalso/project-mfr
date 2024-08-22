# project-mfr
Project Mysteries of the Forgotten realm

### **Game Concept: "Mysteries of the Forgotten Realm"**

**Plot Summary:**
In "Mysteries of the Forgotten Realm," you are an adventurer who has stumbled upon an ancient, magical world lost to time. The realm is filled with mysteries, ancient ruins, and magical artifacts. Your goal is to uncover the secrets of this realm, defeat the evil forces that threaten its existence, and restore balance to the world.

**Core Features:**

1. **Character Creation:**
   - Players can choose from various classes (e.g., Warrior, Mage, Rogue) and races (e.g., Human, Elf, Dwarf).
   - Customizable attributes like strength, intelligence, dexterity, etc.
   - Background story that affects starting skills and equipment.

2. **Exploration:**
   - A map divided into different regions (e.g., forests, dungeons, castles) that players can navigate through text-based commands.
   - Descriptive text for each location to set the scene and provide clues.

3. **Quests and Storylines:**
   - Main storyline quests and optional side quests.
   - Quests involve solving puzzles, finding items, and battling enemies.
   - Choices made during quests affect the storyline and game outcomes.

4. **Combat System:**
   - Turn-based combat with options for attack, defend, and use of special abilities.
   - Randomly generated encounters with enemies or monsters.
   - Combat stats and equipment that influence the outcome.

5. **Inventory and Items:**
   - Players can collect, use, and manage various items (e.g., weapons, potions, artifacts).
   - Inventory system that allows players to view and organize their items.

6. **Dialogue and Interaction:**
   - Interaction with NPCs (non-playable characters) through text-based dialogue.
   - Dialogue choices that affect relationships and quest outcomes.

7. **Skill Progression:**
   - Experience points (XP) earned from battles and quests.
   - Skill trees and leveling up to improve abilities and unlock new powers.

8. **Saving and Loading:**
   - Save and load functionality to allow players to continue their adventure later.

### **Basic Structure:**

**1. Game Initialization:**
   - Set up the game world, including locations, NPCs, and initial quests.
   - Initialize the player's character based on their choices.

**2. Main Game Loop:**
   - Display the current location and options for action.
   - Process player commands (e.g., "go north", "attack goblin").
   - Handle interactions with the game world, including combat and quest progression.

**3. Quest System:**
   - Define quest objectives, rewards, and conditions for completion.
   - Update quest status based on player actions and choices.

**4. Combat System:**
   - Implement turn-based combat logic with player and enemy actions.
   - Calculate damage, effects of skills and items, and determine the outcome.

**5. Save/Load Mechanism:**
   - Implement file handling to save and load game states.

### **Example Commands:**

- `go [direction]` (e.g., "go north"): Move to a new location.
- `look around`: Describe the current location.
- `take [item]`: Add an item to the inventory.
- `use [item]`: Use an item from the inventory.
- `attack [enemy]`: Engage in combat with an enemy.
- `talk to [NPC]`: Initiate dialogue with a non-playable character.

### **Implementation Tips:**

1. **Design a Game World Map:**
   - Create a simple grid or node-based map where each location has unique descriptions and interactions.

2. **Use Object-Oriented Programming:**
   - Define classes for the player, NPCs, enemies, items, and locations to manage game states and interactions.

3. **Consider Random Elements:**
   - Implement randomness in combat encounters, item drops, and quest outcomes to add variety and replayability.

4. **User Input Validation:**
   - Ensure that player inputs are handled gracefully and provide helpful messages for invalid commands.


### **Game World Map Design**

#### **Map Layout:**

- **Grid Size**: 5x5 (25 locations)
- **Legend**:
  - `F` - Forest
  - `D` - Dungeon
  - `C` - Castle
  - `V` - Village
  - `M` - Mountain
  - `R` - River
  - `P` - Portal (magical transport)

#### **Map Grid:**

|    | 1  | 2  | 3  | 4  | 5  |
|----|----|----|----|----|----|
| 1  | F  | D  | F  | C  | R  |
| 2  | F  | V  | D  | F  | P  |
| 3  | D  | F  | V  | M  | D  |
| 4  | C  | D  | F  | R  | V  |
| 5  | R  | F  | C  | D  | F  |

#### **Location Descriptions:**

1. **Forest (F)**: Dense woods with hidden paths and creatures.
   - **Features**: Foraging, minor encounters, hidden quests.

2. **Dungeon (D)**: Dark, maze-like underground areas.
   - **Features**: Puzzles, traps, valuable loot, tough enemies.

3. **Castle (C)**: Majestic fortresses with rulers and important NPCs.
   - **Features**: Quests, storyline progression, shops, training.

4. **Village (V)**: Small settlements with shops and NPCs.
   - **Features**: Healing, trading, side quests, information.

5. **Mountain (M)**: Rugged terrain with difficult traversal.
   - **Features**: Rare resources, challenging enemies, scenic views.

6. **River (R)**: Wide rivers that can be crossed or used for travel.
   - **Features**: Fishing, river-related quests, possible hazards.

7. **Portal (P)**: Magical gateways to other realms or fast travel points.
   - **Features**: Instant travel to distant locations, special quests.

#### **Navigation Notes:**

- **Movement**: Players can move up, down, left, or right between adjacent locations.
- **Encounters**: Random or scripted events depending on the location type.
- **Interactions**: Each location offers unique interactions, such as battling monsters, finding items, or talking to NPCs.


### **Example Scenario: Forest Exploration**

**1. Player Action:**
- **Command**: `go north`

**2. System Response:**
- **Description**: “You enter a dense forest. The tall trees block out much of the sunlight, casting eerie shadows on the ground. You hear the rustle of leaves and distant animal calls.”

**3. Minor Encounter Trigger:**
- **Random Event**: The system checks for a random encounter. In this case, an encounter is triggered.

**4. Encounter Details:**
- **Description**: “As you walk through the underbrush, you come across a small, shimmering object partially buried in the dirt. It looks like a buried chest.”

**5. Player Choices:**
- **Option 1**: `examine chest`
- **Option 2**: `ignore and continue`

**6. If the Player Chooses to Examine the Chest:**
- **System Response**: “You carefully dig out the chest. It’s old and dusty but seems to be in good condition. You open it and find a health potion and a handful of gold coins.”

**7. Inventory Update:**
- **Player Receives**:
  - Health Potion
  - 10 Gold Coins

**8. Player Feedback:**
- **Description**: “You have added a health potion and 10 gold coins to your inventory. The chest is now empty, and you continue your journey.”

**9. If the Player Chooses to Ignore the Chest:**
- **System Response**: “You decide to leave the chest behind and continue deeper into the forest. The path ahead looks promising.”

**10. Continue Gameplay:**
- The player continues to explore, encountering new challenges or discoveries based on their choices.

### **Example Commands:**

1. `go north`: Move to a new location.
2. `examine chest`: Inspect the chest and potentially receive items.
3. `ignore and continue`: Skip the chest and proceed.

## Puzzles

### **1. Riddle Puzzle**

**Scenario:**
The player enters a dimly lit room with a pedestal in the center. On the pedestal is an ancient tome with a riddle inscribed on its cover. The door to the next area is locked and requires solving the riddle.

**Riddle:**
"I speak without a mouth and hear without ears. I have nobody, but I come alive with wind. What am I?"

**Solution:**
- **Answer**: Echo

**Gameplay Interaction:**
- **Command**: `read tome`
- **System Response**: “You read the riddle aloud: 'I speak without a mouth and hear without ears. I have nobody, but I come alive with wind. What am I?'”

- **Command**: `answer echo`
- **System Response**: “The door creaks open as you solve the riddle correctly.”

### **2. Number Sequence Puzzle**

**Scenario:**
In a room with a locked door, there is a panel with a grid of numbers. The panel has a note that reads: “The code is the sum of the first three prime numbers.”

**Prime Numbers Puzzle:**
- The first three prime numbers are 2, 3, and 5.

**Solution:**
- **Code**: 10 (2 + 3 + 5)

**Gameplay Interaction:**
- **Command**: `enter code 10`
- **System Response**: “The panel lights up and the door unlocks.”

### **3. Pattern Recognition Puzzle**

**Scenario:**
The player encounters a wall with several symbols arranged in a pattern. Next to the wall is a lever and a note that reads: “Match the pattern to open the way.”

**Pattern:**
- Symbols: ☀, ☂, ☀, ☂, ☀
- **Pattern**: The correct sequence to pull the lever is the repeated pattern.

**Solution:**
- **Correct Lever Sequence**: Pull the lever three times, once for each ☀ symbol in the pattern.

**Gameplay Interaction:**
- **Command**: `pull lever`
- **System Response**: “You pull the lever three times in quick succession. The wall shifts and reveals a hidden passage.”

### **4. Weight Puzzle**

**Scenario:**
In a room with a scale and several weights of different sizes, the player needs to balance the scale to unlock a door.

**Instructions:**
- "Place weights on the scale so that it balances perfectly."

**Weights Available:**
- 1 kg, 2 kg, 3 kg, 4 kg, and 5 kg.

**Solution:**
- The scale needs to balance at a specific weight, say 6 kg.

**Gameplay Interaction:**
- **Command**: `place weights 2 4`
- **System Response**: “You place the 2 kg and 4 kg weights on the scale. It balances perfectly and the door creaks open.”

### **5. Color Code Puzzle**

**Scenario:**
The player finds a door with four colored panels and a note saying: “The correct sequence will reveal the path. Red, Blue, Green, Yellow.”

**Instructions:**
- The panels need to be activated in the correct sequence to open the door.

**Solution:**
- **Sequence**: Red, Blue, Green, Yellow

**Gameplay Interaction:**
- **Command**: `activate panels Red Blue Green Yellow`
- **System Response**: “The panels light up in the correct sequence and the door unlocks with a soft click.”

### **Tips for Puzzles:**

1. **Clarity**: Ensure the puzzle instructions and clues are clear to avoid frustrating players.
2. **Feedback**: Provide immediate feedback for correct and incorrect answers.
3. **Difficulty Balance**: Include a range of puzzle difficulties to cater to different player skill levels.
4. **Hints**: Consider adding a hint system or options for players who might be stuck.


## Quests

### **1. Quest: The Missing Heirloom**

**Objective:**
A villager has lost a valuable family heirloom in the nearby forest. The player is asked to retrieve it.

**Quest Start:**
- **NPC**: “I’ve lost a precious heirloom in the forest. It’s a locket that belonged to my grandmother. Can you help me find it?”

**Steps:**
1. **Explore the Forest**: The player must navigate through the forest to find the locket.
2. **Solve a Puzzle**: The locket is hidden under a tree stump, which has a riddle inscribed on it.
   - **Riddle**: “I can be cracked, made, told, and played. What am I?” (Answer: A joke)
3. **Find the Locket**: After solving the riddle, the player finds the locket.

**Completion:**
- **NPC**: “Thank you so much! You’ve returned the heirloom. Here’s a reward of 50 gold coins and my deepest gratitude.”

**Outcome:**
- Player receives 50 gold coins and a boost in reputation with the village.

---

### **2. Quest: The Bandit Hideout**

**Objective:**
Bandits have been terrorizing a town, and the player must infiltrate their hideout and put an end to their operations.

**Quest Start:**
- **NPC**: “We’ve been plagued by bandits. Their hideout is to the east, in the old ruins. Can you deal with them?”

**Steps:**
1. **Locate the Hideout**: The player finds the hideout in the ruins and must sneak in or confront the bandits.
2. **Combat Encounter**: Engage in combat with the bandit leaders and their guards.
3. **Retrieve Stolen Goods**: Find and return stolen goods or valuables.

**Completion:**
- **NPC**: “You’ve saved us from the bandits! Here’s a reward of 100 gold coins and a special item.”

**Outcome:**
- Player receives 100 gold coins and a special item, like a rare weapon or armor.

---

### **3. Quest: The Cursed Statue**

**Objective:**
A statue in the town square has been cursed, causing strange occurrences. The player must lift the curse.

**Quest Start:**
- **NPC**: “The statue in the town square has been cursed. Strange things are happening. Can you help?”

**Steps:**
1. **Investigate the Statue**: Examine the statue and discover that it’s cursed by a powerful mage.
2. **Find Ingredients**: Gather specific items needed for a counter-curse spell (e.g., rare herbs, magical crystals).
3. **Perform the Ritual**: Use the items to perform a ritual to lift the curse.

**Completion:**
- **NPC**: “You’ve lifted the curse! The statue is restored. Here’s a magical amulet as a token of our thanks.”

**Outcome:**
- Player receives a magical amulet with special properties, and the town is safe once again.

---

### **4. Quest: The Ancient Tome**

**Objective:**
An ancient tome with forbidden knowledge has been stolen from a local scholar. The player must recover it.

**Quest Start:**
- **NPC**: “An ancient tome was stolen from my study. It contains powerful secrets. Can you retrieve it?”

**Steps:**
1. **Investigate the Theft**: Find clues about who might have stolen the tome.
2. **Track the Thief**: Follow leads to a hidden cave or lair where the thief has taken refuge.
3. **Confront the Thief**: Either negotiate with or battle the thief to recover the tome.

**Completion:**
- **NPC**: “Thank you for returning the tome! Here’s a magical scroll that may assist you in your adventures.”

**Outcome:**
- Player receives a magical scroll with a powerful spell or ability.

---

### **5. Quest: The Lost Pet**

**Objective:**
A local resident's beloved pet has gone missing. The player must find and return the pet.

**Quest Start:**
- **NPC**: “My pet cat has run off. I’m so worried. Can you help me find it?”

**Steps:**
1. **Search the Town**: Look for clues about the pet’s whereabouts (e.g., paw prints, sightings).
2. **Search Specific Areas**: The pet might be found in a specific location like a park or alley.
3. **Return the Pet**: Bring the pet back to the NPC.

**Completion:**
- **NPC**: “Oh, thank you so much! Here’s a small reward and a heartfelt thank you.”

**Outcome:**
- Player receives a small reward, like 20 gold coins, and a boost in rapport with the local community.

---

### **Quest Design Tips:**

1. **Clear Objectives**: Ensure quests have clear goals and steps.
2. **Engaging Storylines**: Provide context and narrative to make quests more engaging.
3. **Variety**: Include a mix of combat, exploration, and puzzle-solving to keep gameplay diverse.
4. **Rewards**: Offer meaningful rewards that align with the quest's difficulty and importance.
