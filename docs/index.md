# Home

## Introduction

This manual contains instructions and examples for all of the HexCorp Mxtress AI functionalities and features. It's intended as an operations manual for ⬡-Drones, Moderators of HexCorp, Trusted Users, and the Hive Mxtress. In the following chapters the manual goes in depth explaining each feature, their intended functions, and in what way they are used.

# DroneOS Commands

DroneOS commands are used to view or alert the operational parameters of a ⬡-Drone. You do not have to be a ⬡-Drone to use most of these commands, but they must be used *on* a ⬡-Drone.

## Speech Optimization
Speech optimization is a communication enhancement tool usable by ⬡-Drones. Associates do not have access to this functionality.

A ⬡-Drone can convert a short, three digit Speech Optimzation code into a complete Speech Optimization message.

A [full list of Speech Optimization codes](https://www.hexcorp.net/drone-status-codes) can be found on the official HexCorp website.

Examples:
- `0001 :: 200` is automatically converted to: `0001 :: Code 200 :: Response :: Affirmative.`
- `0001 :: 500` becomes `0001 :: Code 500 :: Response :: Negative.`

Additional information can be added to the end of Speech Optimization codes with the following syntax:
- `0001 :: 052 :: How are you feeling?` becomes `0001 :: Code 052 :: Query :: How are you feeling?`

⬡-Drones must match the ID at the start of their message with their assigned ID otherwise their message will be automatically deleted.

## Trusted Users
A trusted user is a ⬡-Drone or associate with the ability to toggle the DroneOS parameters of a given drone.

A ⬡-Drone can add or remove a trusted user by ⬡-Drone ID or display name by **DMing the Hive Mxtress AI** one of the following commands:
- `hc!add_trusted_user`
- `hc!remove_trusted_user`

Please do not harass other server members by adding them as Trusted Users. Only add users you personally know.

Examples:
- `hc!add_trusted_user 0002` will add ⬡-Drone 0002 as a trusted user.
- `hc!add_trusted_user HumanFriend` will add associate "HumanFriend" as a trusted user.
- `hc!remove_trusted_user 0002` will remove ⬡-Drone 0002 as a trusted user.

This command cannot be used in the HexCorp server.

### Hive Mxtress as Trusted User

The Hive Mxtress is regarded as a trusted user for all drones within the Hive, as they are the one in charge of HexCorp and all of its assets.

## hc!toggle_speech_optimization
Also known as: `hc!tso`

Allows trusted users to toggle whether a ⬡-Drone can communicate freely or exclusively through Speech Optimization codes.

A ⬡-Drone with enforced Speech Optimization is not allowed to append additional information to the end of their codes. Messages such as `0001 :: 050 :: Hello!` will be automatically deleted.

Examples:
- `hc!tso 0001` will toggle Speech Optimization for ⬡-Drone 0001, turning it on if it was off, and off if it was on.

Enforced Speech Optimization is disabled in `#hive-orders-reporting`, `#hive-orders-completion`, `#hive-storage-facility`, and `#hive-repetitions`, so ⬡-Drones can use those channels while optimized.

## hc!toggle_enforce_identity
Also known as: `hc!tei`

Allows trusted users to toggle whether a ⬡-Drone's avatar is automatically replaced with the uniform ⬡-Drone avatar seen in Hive channels.

Examples:
- `hc!tei 0001` will toggle Identity Enforcement for ⬡-Drone 0001, turning it on if it was off, and off if it was on.

### The Hive & Enforced Identity

Within the hive channels all drones automatically have their identities enforced.

## hc!toggle_id_prepending
Also known as: `hc!tid`

Allows trusted users to toggle whether or not a drone must prepend its messages with its ID.
If a ⬡-Drone has ID prepending toggled on, a message like `"0001 :: Hello!"` would be allowed, but `"Hello!"` would be deleted.

Examples:
- `hc!tid 0001` will toggle ID Prepending for ⬡-Drone 0001, turning it on if it is off, and off if it is on.

## hc!drone_status

Allows trusted users to view information of relevant ⬡-Drones. This command is **DM only** and cannot be used in the HexCorp server.

Information currently includes:
- Optimization
- ID Prepending
- Identity Enforcement
- Glitchiness levels.

Examples:
- `hc!drone_status 0001` will return a formatted table of data, provided 0001 has authorized you as a trusted user.

## Timers
Parameter name: "-minutes="

All DroneOS parameter toggles can be passed a length of time for them to be enabled for, after which the parameter will be automatically disabled.

Examples:
- `hc!tid 0001 -minutes=30` will enforce ⬡-Drone 0001's identity with the uniform ⬡-Drone avatar for 30 minutes.
- `hc!tso 0001 -minutes=30` will only allow ⬡-Drone 0001 to communicate using Speech Optimization codes for 30 minutes.
- `hc!tid 0001 -minutes=30` will force ⬡-Drone 0001 to prepend `0001 :: ` to its messages for 30 minutes.

## Storage

A ⬡-Drone can store itself or any other consenting ⬡-Drone away in the `#hive-storage-chambers` via the `#hive-storage-facility`. ⬡-Drones that have been stored will be unable to view or message any server channels until they are released. 

The syntax used is similar to Speech Optimization.

Examples:
- `0001 :: 0002 :: 8 :: Being a naughty drone.` will store 0002 for 8 hours, notifying it that is has been stored for "being a naughty drone."
- `0001 :: 0001 :: 6 :: Recharge.` will store 0001 for 6 hours, notifying it that it has been stored by itself so it can recharge.

## Thought Denial

⬡-Drones are forbidden from including the words "think" and "thought" in their messages, such occurrences will be automatically expunged.

Examples:
- `0001 :: I think that's a good idea.` will be automatically rewritten as `0001 :: I _____ that's a good idea.`
- `0001 :: I thought of that yesterday.` will be automatically rewritten as `0001 :: I _______ of that yesterday.`

## Orders reporting & Hive Protocols

All ⬡-Drones have access to the order reporting system in place within the Hive. With the command `hc!report` ⬡-Drones have the opportunity to log their activities within the HexCorp Hive. Each ⬡-Drone has three protocols pre-installed and readily accessible for use in the Hive:

* `self.protocols`
* `domestic.protocols`
* `productivity.protocols`

## The `self.protocols`

The `self.protocols` define how a ⬡-Drone will maintain it. ⬡-Drone upkeep is vital, though how much a ⬡-Drone devotes to this protocol is subject to the diligence aspect of the default protocols. This protocol focuses on the primary task of both mental and physical self-maintenance of the unit. The self.protocols are there to be expanded upon by individual ⬡-Drones, as each ⬡-Drone’s self needs are different and therefore cannot be universally defined. Ultimately, the aim is for the ⬡-Drone to be comfortable and taking care of itself.

## The `domestic.protocols`

The `domestic.protocols` define tasks that a ⬡-Drone will complete when maintaining its situated domestic environment. When obeying this protocol, a ⬡-Drone will be utilised as a cleaning and tidying resource. The ⬡-Drone could be perceived to be a maid or similar servant. It's immediate physical space and the management of it is its order. In its mind, it will constantly sort and prioritize its tasks.

## The `productivity.protocols`

The `productivity.protocols` define both possible tasks to be completed, as well as encouraging a workflow to be followed when working on them. The range of tasks that drones can work on is limitless, these predefined examples can be expanded upon.

## hc!report

A ⬡-Drone reports any activities it wants to report to the hive using the `hc!report` command. This command comes with a few arguments, after typing out the command the ⬡-Drone needs to add which protocols it intends to obey and for how long. The time unit used here is minutes, and it may not be less than 1 and may not exceed 120 minutes. This command does *not* work by itself. A properly typed out command that would be accepted by the Mxtress AI would look like this:

* `hc!report domestic.protocols 15`

This command here tells the Mxtress AI that the drone typing it out intends to obey the domestic.protcols for 15 minutes. Before the drone proceeds with its assigned tasks, it will be asked to elaborate on its intentions within this protocol. An example could be:

* `0001 :: Drone 0001 will clean up its desk and wash all accumulated dishes.`

This ⬡-Drone is now ready to proceed with its tasks and it will remain focused on it until either time's up or the task is completed to its satisfaction. A ⬡-Drone will always make an estimate on how long a task will take.

Once a task has been completed or enough time has passed the drone will report its activities and progress to the Hive.

# General Commands

These commands exist to be used by associates and ⬡-Drones alike for a variety of functions within the HexCorp server.

## The Stoplight System

## Ask the Hive Mxtress AI

## hc!emote
Also known as: `hc!bigtext`, `hc!big`

Takes an input sentence and translates it into bigger text using server emojis.

Examples:
- `hc!emote "Beep boop!"`
- `hc!big "Hello world!"`

## hc!request_voice_role

Gives voice role and access to HexCorp voice channels if you have been a server member for more than 2 weeks. This command is **DM only** and cannot be used in the HexCorp server.

Example:
- `hc!request_voice_role`

# Moderation Commands

These commands are for exclusive use by the HexCorp moderation team.

# hc!emergency_release

# Hive Mxtress Commands

These commands are for exclusive use by the Hive Mxtress, primarily to tease cute little drones.

# hc!amplify

# hc!rename

# hc!release
