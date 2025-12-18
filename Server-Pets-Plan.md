# Discord Pet Bot - Development Steps

## Prerequisites
- [ ] Set up development environment
- [ ] Set up database (SQLite)

---

## Phase 1: Core Pet + Currency

### Step 1: Bot Foundation
- [ ] Create basic bot structure
- [ ] Set up command handler
- [ ] Implement slash commands
- [ ] Set up database connection
- [ ] Create user registration system

**Commands Added:**
- None (foundation only)

### Step 2: Currency System
- [ ] Create currency table in database
- [ ] Implement `/balance` command
- [ ] Implement `/work` command with cooldown
- [ ] Add currency transaction logging
- [ ] Create basic shop framework

**Commands Added:**
- `/balance` - Check your current currency balance
- `/work` - Earn currency by working (has cooldown)

### Step 3: Pet Species System
- [ ] Create pet species data structure
- [ ] Define species types (dogs, cats, birds, reptiles)
- [ ] Create species-specific message pools
- [ ] Implement message randomization system
- [ ] Test message variety for each species

**Commands Added:**
- None (backend system only)

### Step 4: Basic Pet System
- [ ] Create pet database table (id, user_id, species, name, level, stats, active_status)
- [ ] Implement `/awaken` command (basic version, no room influence yet)
- [ ] Allow user to name their pet during awakening
- [ ] Implement basic pet viewing command
- [ ] Add pet stat tracking (hunger, affection, level)

**Commands Added:**
- `/awaken` - Awaken a new pet from an egg and name it
- `/pet info` or `/mypet` - View your active pet's stats and info

### Step 5: Pet Interaction
- [ ] Implement `/feed` command
- [ ] Implement `/play` command
- [ ] Implement `/pet` command (for affection)
- [ ] Add XP/leveling system
- [ ] Create pet status display

**Commands Added:**
- `/feed` - Feed your pet to reduce hunger
- `/play` - Play with your pet to gain XP and affection
- `/pet` - Pet your pet to increase affection

### Step 6: Daycare/Inventory System
- [ ] Implement active/inactive pet status
- [ ] Create `/daycare` command to view all pets
- [ ] Implement `/swap` command to change active pet
- [ ] Ensure stats freeze when pet goes to daycare
- [ ] Test multi-pet management

**Commands Added:**
- `/daycare` - View all your pets in daycare/inventory
- `/swap [pet_name/id]` - Swap your active pet with one from daycare

### Step 7: Basic Shop
- [ ] Implement `/shop` command
- [ ] Add egg purchasing (different species)
- [ ] Add basic food items
- [ ] Implement purchase confirmation
- [ ] Test economy balance

**Commands Added:**
- `/shop [category]` - Browse items available for purchase (eggs, food, etc.)
- `/buy [item] [quantity]` - Purchase an item from the shop

### Phase 1 Testing Checkpoint
- [ ] Invite trusted friends to test
- [ ] Gather feedback on core loop
- [ ] Balance currency earning rates
- [ ] Fix bugs before Phase 2

---

## Phase 2: Rooms, Hunger, Achievements

### Step 8: Room System Foundation
- [ ] Create room database table
- [ ] Create furniture/decor database table
- [ ] Implement `/room` command to view current room
- [ ] Create basic room customization commands
- [ ] Add furniture placement system

**Commands Added:**
- `/room` - View your current room and placed furniture
- `/inventory furniture` - View your furniture inventory

### Step 9: Furniture Shop & Items
- [ ] Add furniture to shop
- [ ] Categorize items (calming, energetic, luxurious, etc.)
- [ ] Implement item effects metadata
- [ ] Create furniture inventory system
- [ ] Add `/place` and `/remove` furniture commands

**Commands Added:**
- `/place [furniture_item]` - Place a furniture item in your room
- `/remove [furniture_item]` - Remove a furniture item from your room
- `/shop furniture` - Browse furniture items (now shows effects)

### Step 10: Room Influence on Awakening
- [ ] Calculate room "mood" based on placed items
- [ ] Modify awakening algorithm to factor in room decor
- [ ] Display item effects in shop descriptions
- [ ] Test personality probability shifts
- [ ] Balance decor influence percentages

**Commands Added:**
- None (enhances existing `/awaken` command)

### Step 11: Personality System
- [ ] Create personality trait definitions
- [ ] Implement personality assignment during awakening
- [ ] Store personality traits in pet database
- [ ] Display personality traits in pet info
- [ ] Create personality-specific stat modifiers

**Commands Added:**
- None (enhances existing `/mypet` and `/awaken` commands)

### Step 12: Comfort Item Lock
- [ ] Implement comfort item selection during awakening
- [ ] Store locked item reference in pet database
- [ ] Create mood drain calculation system
- [ ] Apply slower drain when comfort item is placed
- [ ] Display locked item in pet info

**Commands Added:**
- None (enhances existing `/mypet` command to show locked item)

### Step 13: Enhanced Hunger System
- [ ] Refine hunger decay rates
- [ ] Implement personality-based hunger differences
- [ ] Add hunger warnings before pet refuses interaction
- [ ] Block interactions when too hungry
- [ ] Test with different personality types

**Commands Added:**
- None (enhances existing interaction commands)

### Step 14: Auto-Feed System
- [ ] Create savings wallet system (separate from main balance)
- [ ] Implement `/autofeed` setup command
- [ ] Create auto-feed budget configuration
- [ ] Implement automatic food purchasing
- [ ] Add auto-feed status notifications

**Commands Added:**
- `/autofeed setup [budget]` - Set up auto-feed system with budget amount
- `/autofeed status` - Check auto-feed configuration and remaining budget
- `/autofeed disable` - Turn off auto-feed system
- `/wallet` - View main balance and savings wallet separately

### Step 15: Story Events
- [ ] Create event system framework
- [ ] Design 3-5 starter events (park, pizza place, beach, etc.)
- [ ] Implement event triggers
- [ ] Create event memory items as rewards
- [ ] Add memory items to room decor options

**Commands Added:**
- `/event` or `/adventure` - Trigger/view available story events
- None (events may trigger automatically during interactions)

### Step 16: Event Memory Item Effects
- [ ] Link memory items to their origin events
- [ ] Implement event preference bonuses
- [ ] Track which events pets enjoy more
- [ ] Test event frequency with Curious personality
- [ ] Balance event rewards

**Commands Added:**
- None (enhances existing event system)

### Step 17: Achievement System
- [ ] Create achievement database table
- [ ] Define achievement categories (Easy, Medium, Hard, Event)
- [ ] Implement achievement tracking
- [ ] Create `/achievements` command
- [ ] Add achievement rewards (currency/items)
- [ ] Implement achievement notifications

**Commands Added:**
- `/achievements` - View all achievements and your progress
- `/achievements [category]` - Filter achievements by difficulty/type

### Phase 2 Testing Checkpoint
- [ ] Test room customization flow
- [ ] Verify personality influences work correctly
- [ ] Test auto-feed system thoroughly
- [ ] Balance event frequency and rewards
- [ ] Get feedback on achievement variety

---

## Phase 3: Gambling + Pet Worry + Shelter (Opt-in)

### Step 18: Server Settings System
- [ ] Create server settings database table
- [ ] Implement permission checking (Manage Server/Bot)
- [ ] Create `/settings` command for admins
- [ ] Add gambling enable/disable toggle
- [ ] Test permission system

**Commands Added:**
- `/settings` - [Admin] View and modify server settings
- `/settings gambling [enable/disable]` - [Admin] Toggle gambling features

### Step 19: Gambling Commands
- [ ] Implement `/coinflip` command
- [ ] Implement `/dice` command
- [ ] Implement `/slots` command (optional)
- [ ] Add gambling cooldowns
- [ ] Create gambling transaction logs

**Commands Added:**
- `/coinflip [bet_amount] [heads/tails]` - Flip a coin and bet on the outcome
- `/dice [bet_amount] [number]` - Roll a die and bet on the result
- `/slots [bet_amount]` - Play slot machine (optional)

### Step 20: Gambling Tracking System
- [ ] Track net gambling wins/losses per user
- [ ] Create threshold system for warnings
- [ ] Implement session tracking
- [ ] Store gambling stats in database
- [ ] Create gambling history view

**Commands Added:**
- `/gambling stats` - View your gambling statistics and history

### Step 21: Pet Emotional Response to Gambling
- [ ] Create pet worry/stress level system
- [ ] Implement warning stage (early concern)
- [ ] Add species-specific warning messages
- [ ] Implement personality modifiers (Anxious warns earlier)
- [ ] Create DM notification system

**Commands Added:**
- None (enhances existing gambling commands with pet reactions)

### Step 22: Pet Refusal Stage
- [ ] Implement interaction blocking at refusal stage
- [ ] Create refusal messages (species-specific)
- [ ] Allow daycare swapping at this stage
- [ ] Add commands to check pet stress level
- [ ] Test warning progression

**Commands Added:**
- `/pet stress` or enhanced `/mypet` - View pet's stress/worry level

### Step 23: Distressed State System
- [ ] Create distressed flag in database
- [ ] Block daycare transfers when distressed
- [ ] Implement "pet won't leave" messages
- [ ] Create recovery mechanic (working, not gambling)
- [ ] Test distressed state restrictions

**Commands Added:**
- None (modifies existing `/swap` command behavior)

### Step 24: Shelter System
- [ ] Create shelter database table
- [ ] Implement automatic shelter transfer
- [ ] Calculate reclaim fee (based on rarity/attachment)
- [ ] Create cooldown period before reclaim
- [ ] Store shelter entry reason/timestamp

**Commands Added:**
- None (automatic system, pets transferred when threshold reached)

### Step 25: Shelter Recovery
- [ ] Implement `/shelter` command to view pets in shelter
- [ ] Create `/reclaim` command
- [ ] Verify stats are preserved
- [ ] Send periodic "pet misses you" messages
- [ ] Implement repeat offender cost increases

**Commands Added:**
- `/shelter` - View your pets currently in shelter
- `/reclaim [pet_name/id]` - Pay to reclaim a pet from shelter

### Step 26: Community Service System (Optional)
- [ ] Create work requirement tracking
- [ ] Implement mandatory work commands for repeat offenders
- [ ] Track completion of community service
- [ ] Allow reclaim only after completion
- [ ] Test escalation system

**Commands Added:**
- `/community_service` - View required work tasks before reclaiming pet

### Phase 3 Testing Checkpoint
- [ ] Test gambling disable functionality per server
- [ ] Verify warning progression works correctly
- [ ] Test daycare blocking when distressed
- [ ] Balance shelter reclaim costs
- [ ] Get feedback on emotional response system

---

## Phase 4: Social Systems

### Step 27: Friends System
- [ ] Create friends database table (user_id, friend_id, status)
- [ ] Implement `/friend add` command
- [ ] Create friend request/accept system
- [ ] Implement `/friend list` command
- [ ] Add `/friend remove` command

**Commands Added:**
- `/friend add [@user]` - Send a friend request to another user
- `/friend accept [@user]` - Accept a pending friend request
- `/friend list` - View your friends list
- `/friend remove [@user]` - Remove a friend from your list
- `/friend requests` - View pending friend requests

### Step 28: Pet Visiting
- [ ] Implement `/visit [friend]` command
- [ ] Show friend's active pet
- [ ] Allow basic interactions with friend's pet
- [ ] Track visit history
- [ ] Apply Social personality bonus

**Commands Added:**
- `/visit [@user]` - Visit a friend's pet
- `/visit history` - View your recent visits

### Step 29: Gifting System
- [ ] Implement `/gift [friend] [item/currency]` command
- [ ] Add confirmation prompts
- [ ] Create captcha for large gifts (anti-bot)
- [ ] Log all gift transactions
- [ ] Test Greedy personality bonus

**Commands Added:**
- `/gift [@user] [amount] currency` - Gift currency to a friend
- `/gift [@user] [item_name]` - Gift an item to a friend

### Step 30: Friend Activity Features
- [ ] Show friend's recent activity
- [ ] Implement care actions for friend's pets
- [ ] Add gift suggestions based on friend's needs
- [ ] Create notification system for gifts received
- [ ] Test social features end-to-end

**Commands Added:**
- `/friend activity [@user]` - View a friend's recent activity
- `/care [@user]` - Help care for a friend's pet (feed/play while they're away)

### Phase 4 Testing Checkpoint
- [ ] Test friend system edge cases
- [ ] Verify gifting security measures work
- [ ] Test visit system with various personalities
- [ ] Balance social rewards
- [ ] Get feedback on social features

---

## Polish & Launch Preparation

### Step 31: Economy Balancing
- [ ] Review all currency sources and sinks
- [ ] Adjust work command rewards
- [ ] Balance shop prices
- [ ] Test progression rate
- [ ] Prevent inflation issues

**Commands Added:**
- None (balancing existing systems)

### Step 32: User Experience
- [ ] Add helpful error messages
- [ ] Create tutorial/onboarding flow
- [ ] Implement `/help` command with categories
- [ ] Add command cooldown indicators
- [ ] Improve visual formatting of responses

**Commands Added:**
- `/help [command/category]` - View help documentation and command list
- `/tutorial` - Start the new user tutorial (optional)

### Step 33: Admin Tools
- [ ] Create admin dashboard commands
- [ ] Implement economy monitoring tools
- [ ] Add user moderation commands
- [ ] Create backup/restore functionality
- [ ] Test admin external bot integration

**Commands Added:**
- `/admin stats` - [Admin] View server economy statistics
- `/admin user [@user]` - [Admin] View detailed user information
- `/admin transfer [@user] [amount]` - [Admin] Manual currency adjustments (via external bot)
- `/admin backup` - [Admin] Trigger database backup

### Step 34: Performance Optimization
- [ ] Optimize database queries
- [ ] Implement caching where appropriate
- [ ] Test with multiple concurrent users
- [ ] Monitor memory usage
- [ ] Optimize command response times

**Commands Added:**
- None (backend optimization)

### Step 35: Documentation
- [ ] Write user guide
- [ ] Create admin documentation
- [ ] Document all commands
- [ ] Write setup instructions for server admins
- [ ] Create FAQ

**Commands Added:**
- None (documentation only)

### Step 36: Security & Privacy
- [ ] Review data storage practices
- [ ] Implement rate limiting
- [ ] Add input validation everywhere
- [ ] Test for SQL injection vulnerabilities
- [ ] Review bot permissions

**Commands Added:**
- `/privacy` - View data privacy policy and what data is stored
- `/data delete` - Request account data deletion (GDPR compliance)

### Step 37: Beta Testing
- [ ] Recruit larger beta test group
- [ ] Monitor for bugs and exploits
- [ ] Gather comprehensive feedback
- [ ] Make final balance adjustments
- [ ] Fix critical issues

**Commands Added:**
- `/feedback [message]` - Submit feedback during beta (optional)
- `/bug [description]` - Report bugs during beta (optional)

### Step 38: Launch
- [ ] Deploy to production server
- [ ] Create bot listing on top.gg (optional)
- [ ] Announce launch
- [ ] Monitor first 24-48 hours closely
- [ ] Be ready for hotfixes

**Commands Added:**
- None (deployment)

---

## Post-Launch

### Ongoing Maintenance
- [ ] Monitor bot uptime
- [ ] Regular database backups
- [ ] Track user feedback
- [ ] Fix bugs as reported
- [ ] Plan future content updates

### Future Content Ideas
- [ ] Seasonal events
- [ ] New pet species
- [ ] Additional furniture sets
- [ ] New story events
- [ ] Expanded personality traits
- [ ] Pet breeding system (maybe?)
- [ ] Pet competitions/leaderboards

---

## Command Summary by Phase

**Phase 1 (Core):**
- `/balance`, `/work`, `/awaken`, `/mypet`, `/feed`, `/play`, `/pet`, `/daycare`, `/swap`, `/shop`, `/buy`

**Phase 2 (Rooms & Progression):**
- `/room`, `/inventory`, `/place`, `/remove`, `/autofeed`, `/wallet`, `/event`, `/achievements`

**Phase 3 (Gambling & Shelter):**
- `/settings`, `/coinflip`, `/dice`, `/slots`, `/gambling`, `/shelter`, `/reclaim`, `/community_service`

**Phase 4 (Social):**
- `/friend`, `/visit`, `/gift`, `/care`

**Polish:**
- `/help`, `/tutorial`, `/admin`, `/privacy`, `/data`, `/feedback`, `/bug`

**Total Commands:** ~40-45 commands

---

## Notes

**Time Estimates:**
- Phase 1: 2-3 weeks
- Phase 2: 3-4 weeks
- Phase 3: 2-3 weeks
- Phase 4: 1-2 weeks
- Polish & Launch: 1-2 weeks

- **Total:** ~10-14 weeks for full release (Not including breaks)
