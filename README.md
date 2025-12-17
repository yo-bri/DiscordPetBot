# Server Pets

Collect and raise virtual pets
Play minigames/gamble for virtual currency
Room design to decorate for the pet
Story for pets ("events")
Friend people to visit, gift, and play with their pets

Schedule events for your pet to remind you about
Build a relation with your pet (optional setting to have it decrease over time)
Achievements
Server-wide bets with the currency

# Currency

Earn currency via
* Gambling (if enabled by server)
* Working
* Official server story polls/events
* Contribution to the bot
* Gifting
* Selling things

Spend currency via
* Gambling (if enabled by server)
* Official server story polls/events entry cost
* Gifting
* Buying furniture
* Buying pets
* Reclaiming pets from shelter

# Pets

* Rarity for different pets
* Pets come in eggs you awaken (not hatch)
* If enabled pets lose stats like affection over time with no interaction
* Pets react based on events and room decor
* Chatting, working, etc, levels up your pet
* Pets are cross-server
* Only one pet can be active at a time
* Inactive pets can be sent to daycare/inventory
* Stats freeze completely while pets are in daycare (no decay)
* Swapping between active pet and daycare is free with no cooldown
* **Stressed/distressed pets cannot be sent to daycare** - they won't go out of fear

## Pet Awakening & Room Influence

* Room decor at time of awakening influences personality trait probabilities
* Decor items display what effects they have on awakening
* System uses Decor + Randomness - you can influence but not guarantee outcomes
* Event memory items make their event origins more liked by the pet

**Item Effects Display:**
* Primary effect: influence on personality traits (e.g. "Calming aura - slightly increases chance of Laid-back trait")
* Secondary effect: event preference bonuses (e.g. "Pets awakened near this item enjoy beach events more")
* Rarity affects strength of influence

**Decor Influence Tiers:**
* Base: 100% random personality pool
* 1-3 relevant items: +5-10% chance for related traits
* 4-6 items: +15-20% chance
* 7+ items (themed room): +25-30% chance (still not guaranteed)
* Event items: +5% to specific event enjoyment on top

**Example Room Setup:**
"Cozy Reading Nook" with soft lighting, bookshelves, plush carpet
* Increases Laid-back/Curious trait odds
* Pet enjoys library/bookstore events more
* Still might get different personality, just less likely

## Comfort Item Lock System

* When a pet awakens, they "lock" one specific item from the room
* The locked item is based on which item had strongest influence during awakening
* While the locked item is placed in the room, that pet's mood/affection drains slower
* Locked item preference is permanent for that pet
* Creates strategic room design: balance aesthetics with pet's comfort needs
* Different pets will have different locked items, requiring room adjustments when swapping

**Example:**
Curious cat awakened in room with telescope locks the telescope as their comfort item. While telescope is in the room, cat's mood drains slower. Player must keep telescope placed or accept normal drain rate.

## Pet Species & Message Pools

Each pet species has its own unique reaction text pool with distinct emotional tones:

* **Dogs:** Loyal, worried, supportive messages
* **Cats:** Distant, passive-aggressive reactions
* **Birds:** Dramatic, expressive responses
* **Reptiles:** Calm, factual observations

Species-specific messages used for:
* Gambling warnings
* Hunger complaints
* Shelter messages
* Event reactions
* General interactions

## Pet Personalities System

* Pets are assigned 2-3 personality traits when awakened
* Traits are influenced by room decor but include randomness
* Traits subtly modify existing systems (no hard punishments)
* Personalities add flavor, not punishment
* No personality creates permanent disadvantages
* All consequences remain reversible

**Example Personality Traits:**
* **Anxious** – Reacts faster to risky behavior, warns earlier but forgives faster
* **Laid-back** – Affection decays slower, complains about hunger later
* **Social** – Gains more affection from friend visits
* **Curious** – Triggers events more often, increased decor/event interactions
* **Greedy** – Enjoys gifts more
* **Lazy** – Complains about hunger later

**Personality × System Modifiers:**
* Personalities influence how systems respond, not whether they exist
* Anxious pets give earlier gambling warnings but forgive faster
* Social pets gain extra affection from friends
* Curious pets increase room decor interactions
* Laid-back pets have slower affection decay
* Too many bright/flashy decors may increase odds of awakening an Anxious pet

## Pet Gambling Protection System

* **Server admins can fully disable gambling** (requires Manage Server / Manage Bot permissions)
* Gambling commands are hidden when disabled server-wide
* Pet gambling-related reactions automatically disabled if gambling is off
* Clear message displayed when gambling is unavailable

**When gambling is enabled:**

**Warning Stages:**
1. **Early warnings** - Pet expresses concern (can still swap to daycare)
2. **Refusal to interact** - Pet won't engage (can still swap to daycare)
3. **Distressed/Scared state** - Pet CANNOT be sent to daycare out of fear (locked in)
4. **Shelter** - Pet taken if situation not resolved

**System Details:**
* If you gamble too much with a net loss, the pet will both DM you and reply to the interaction
* Pet reactions vary based on species and personality
* Warning message: "YOUR PET IS FEELING NEGLECTED. TRY WORKING TO LOWER ITS FEAR"
* Continued gambling losses will cause the pet to refuse interactions (grace period/final warning stage)
* Pet becomes distressed and **cannot be swapped to daycare** - must resolve situation
* If gambling addiction continues, pet services will take your pet to a shelter
* Pets can be reclaimed from shelter by paying a reclaim fee (scales based on rarity/attachment)
* Pets retain their level, affection, and stats while in shelter - you don't lose progress
* Bot sends periodic "Your pet misses you" updates while they're in shelter (species-specific messages)
* Optional cooldown period before reclaiming (e.g. 24 hours) to add weight to the consequence
* Repeat offenders face increased reclaim costs or community service tasks (required work commands)

# Rooms

* Background when viewing your pet
* Different items in the room give different events a chance at appearing
* Different items allow new ways to play with your pet
* Themed furniture sets can unlock special interactions
* Curious pets have increased chance of triggering room-based events
* Room decor influences personality during awakening
* Active pet's locked comfort item should be placed for slower mood drain
* Items display their effects on personality and event preferences
* Event memory items can be placed as room decor

# Friends

- Custom friend system
- Visit friends to take care of their pets
- Give friends gifts (money, items, eggs, etc)
- Social personality pets gain bonus affection from visits

# Achievements

- Achievements are given on completing an action, e.g. get your first pet, make your first friend, first visit, etc.
- Achievements give cash or item rewards depending on difficulty (Easy, Medium, Hard, Event)

# Moderation

- Log ALL gifts, trades, purchases, pet reclaims, shelter transfers, gambling actions, pet swaps, etc.
- Admin transfers via external bot running on the same server to prevent any abuse
- Re-create a captcha system when gifting large sums of money, or rare items/pets
- Always allow people to see their own logs
- Server admins can disable/enable gambling with proper permissions

# Additional Systems

## Daycare/Inventory System
- Only one pet can be active at a time
- Inactive pets are stored in daycare/inventory
- Stats completely freeze while in daycare (no decay, no progress)
- Free swapping with no cooldown between active pet and daycare
- **Exception: Stressed/distressed pets cannot be sent to daycare** - they refuse out of fear
- Players can view daycare pets' personality traits and locked items before swapping
- Prevents neglect of collection while encouraging active pet engagement

## Auto-Feed System
- Auto-feed fillers available as a rent-like system
- Automatically buys food from a dedicated budget (savings wallet)
- Prevents inactive players from losing all their money when gone
- Savings wallet is separate from total balance
- Lazy pets complain about hunger later than other personalities

## Hunger System
- Pets will not interact with you if they're too hungry
- Forces player engagement with the economy
- Auto-feed system can handle this automatically if set up
- Response timing varies by personality (lazy pets are more patient)

## Story Events
- Extra side content for pets (e.g. visiting the park, going to the pizza place in town)
- Events give collectible items like "memories" 
- Memory items can be placed in rooms (e.g. park flowers, pizza chew toy)
- Adds narrative depth and collection goals
- Curious pets trigger events more frequently
- Pets awakened near event memory items enjoy those events more

# Development Roadmap (Phased Feature Rollout)

Not all systems launch at once. Playtesting handled by trusted dev friends before public rollout.

## Phase 1: Core Pet + Currency
- Basic pet system (awakening, feeding, interaction)
- Currency earning (working, basic tasks)
- Simple inventory system
- Basic species differences (visual + message pools)
- Daycare/inventory system with pet swapping

## Phase 2: Rooms, Hunger, Achievements
- Room decoration system
- Room influence on awakening
- Comfort item lock system
- Hunger mechanics
- Auto-feed system
- Achievement framework
- Story events with memory items

## Phase 3: Gambling + Pet Worry + Shelter (Opt-in)
- Server-controlled gambling toggle
- Pet emotional response system
- Shelter/reclaim mechanics
- Personality system introduction
- Species-specific reactions to gambling
- Distressed pet daycare restriction

## Phase 4: Social Systems
- Friends system
- Pet visiting
- Gifting mechanics
- Social personality trait effects

# Design Philosophy

* **Affection decay is OPT-IN** - new players should be stress-free
* **Core systems encourage healthy engagement** without punishment for breaks
* **Pet emotional responses create attachment and personality**
* **Economic systems have safeguards** against exploitation
* **Consequences are meaningful but reversible**
* **Personalities add flavor, not punishment** - no irreversible outcomes tied to personality
* **Server admins have control** over controversial features like gambling
* **Phased rollout ensures quality** - test and refine before expanding
* **Species and personalities create variety** without creating unfair advantages/disadvantages
* **One active pet at a time** - simplifies management while encouraging collection
* **Free swapping with frozen stats** - player-friendly collection system
* **Room design matters** - environmental storytelling through decor influence and comfort items
* **Transparency in systems** - players can see what items do before using them
