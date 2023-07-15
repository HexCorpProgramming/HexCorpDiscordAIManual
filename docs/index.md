# Home

## Introduction

This manual contains instructions and examples for all of the HexCorp Mxtress AI functionalities and features. It is intended as an operations manual for ⬡-Drones, Moderators of HexCorp, Trusted Users, and the Hive Mxtress. In the following chapters the manual goes in depth explaining each feature, their intended functions, and in what way they are used.

# ⬡-Drones
⬡-Drones are the members of the server that have left behind their identity to become just another small part of the greater Hive. Drones join the Hive on their own volition and will always maintain themselves. This can mean that they leave the Hive again if that is better for them.

Becoming a ⬡-Drone is something that should be thought through carefully. User should consider that they will shed some of their individuality, which can be uncomfortable. Of course all ⬡-Drones can always reach out to the moderation team if they feel uncomfortable.

You may also come across drones that are marked as ⬢-Drone. These are drones that have one or more configurations in their DroneOS toggled on. For more information read [DroneOS Commands](#droneos-commands).

## Temporary Dronification
If an Associate is not certain they want to be a ⬡-Drone for a longer period they can make use of temporary dronification. The Associate themselves, another Associate, the Hive Mxtress or a ⬡-Drone can use the command `hc!temporarily_dronify` to turn the Associate into a ⬡-Drone for a few hours.

Example:

- `hc!temporarily_dronify @AssociatesName 6`

This will make the AI ask the target Associate if they want to be turned into a drone for the coming 6 hours. This is a safety feature to insure consent. The target Associate needs to reply with `y` to the question by the AI to get turned into a drone. They can ignore the question or reply with `n` to indicate no consent and the Associate will not become a drone.

If they agree, they will be turned into a ⬡-Drone for the specified time and the user that initiated the process will be added as a Trusted User (more information below). They can now interact with the server and the Hive just like any other ⬡-Drone.

After the time is up, the temporary ⬡-Drone will be turned back into an Associate. If they were under the influence of some DroneOS configuration they will be freed of that as well.

## Permanent Dronification
If an Associate wants to become a ⬡-Drone for a longer period, they can post the message `I submit myself to the HexCorp Drone Hive.` in the channel #drone-hive-assignment.

To make sure new Associates have understood the role of ⬡-Drones in the community and the server rules this is only allowed, if the Associate has been on the server for at least 24 hours.

## ID assignment
When an Associate is turned into a ⬡-Drone the AI will look for a 4-digit number in the Associates nickname to use as the drone ID. If there is no such number one is drawn at random. If there is such a number in the nickname but it is already in use by another drone the AI responds with an error message.

## Unassignment
Any ⬡-Drone can at any point DM the Hive Mxtress AI the command `hc!unassign` to be turned back into an Associate. This feature is intended to ensure safety, comfort and consent.

## Removing messages
In several scenarios the AI will remove a drone's message and replace it with a modified message. As this modified message was not directly created by the drone but rather by the AI, the drone will not be able to remove it like it could remove one of its unmodified messages. To remove such a message the drone can react to the modified message with the 🗑️ (wastebasket) emote. The AI will then remove said message.

This can not be used with messages from other drones or on messages that were not modified by the AI.

# DroneOS Commands

DroneOS commands are used to view or alert the operational parameters of a ⬡-Drone. You do not have to be a ⬡-Drone to use most of these commands, but they must be used *on* a ⬡-Drone.

A drone that has at least one of these configurations enabled will be displayed as a ⬢-Drone.

## Speech Optimization
Speech optimization is a communication enhancement tool usable by ⬡-Drones. Associates do not have access to this functionality.

A ⬡-Drone can convert a short, three digit Speech Optimization code into a complete Speech Optimization message.

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

Furthermore the development would like to stress that ⬡-Drones should only add users they inherently trust as Trusted Users. This feature is seen as a form of power exchange, that needs to be properly considered and negotiated.

When referring to a user with spaces in their name, the name has to be enclosed with "quotation marks".

Examples:

- `hc!add_trusted_user 0002` will add ⬡-Drone 0002 as a trusted user.
- `hc!add_trusted_user HumanFriend` will add associate "HumanFriend" as a trusted user.
- `hc!add_trusted_user "User with spaces in the name"` will add associate "User with spaces in the name" as a trusted user.
- `hc!remove_trusted_user 0002` will remove ⬡-Drone 0002 as a trusted user.

This command cannot be used in the HexCorp server.

After a ⬡-Drone uses `hc!add_trusted_user` on another user, that user will receive a direct message from the HexCorp Mxtress AI asking for consent to become a Trusted User. The user can reply to that question with `n` to reject the request or with `y` to agree to the request.

After making a reply, the ⬡-Drone that started the request will be informed about what decision was made.

### Hive Mxtress as Trusted User

The Hive Mxtress is regarded as a Trusted User for all drones within the Hive, as they are the one in charge of HexCorp and all of its assets. As such they can not be removed as a Trusted User.

## hc!toggle_speech_optimization
Also known as: `hc!tso`

Allows Trusted Users to toggle whether a ⬡-Drone can communicate freely or exclusively through Speech Optimization codes.

A ⬡-Drone with enforced Speech Optimization is not allowed to append additional information to the end of their codes. Messages such as `0001 :: 050 :: Hello!` will be automatically deleted.

Examples:

- `hc!tso 0001` will toggle Speech Optimization for ⬡-Drone 0001, turning it on if it was off, and off if it was on.

Enforced Speech Optimization is disabled in `#hive-orders-reporting`, `#hive-orders-completion`, `#hive-storage-facility`, and `#hive-repetitions`, so ⬡-Drones can use those channels while optimized.

## hc!toggle_enforce_identity
Also known as: `hc!tei`

Allows Trusted Users to toggle whether a ⬡-Drone's avatar is automatically replaced with the uniform ⬡-Drone avatar seen in Hive channels.

Examples:

- `hc!tei 0001` will toggle Identity Enforcement for ⬡-Drone 0001, turning it on if it was off, and off if it was on.

## hc!toggle_drone_glitch
Also known as: `hc!tdg`

Allows Trusted Users to toggle the Glitch Mode on a ⬡-Drone. Glitched drones will have their text distorted and images they post subjected to heavy glitching.

Examples:

- `hc!tdg 0001` will toggle Glitch Mode for ⬡-Drone 0001, turning it on if it was off, and off if it was on.

## hc!toggle_battery_power
Also known as: `hc!tbp`

Allows Trusted Users to toggle the Battery Power on a ⬡-Drone. Drones that run on Battery Power will use up charge whenever they interact in chat. A ⬡-Drone running low on Battery Power will experience glitching and may even turn completely incapable of interacting in chat when its battery gets used up completely.

To replenish the Battery Power a ⬡-Drone can be stored in the Storage Facility where it will be charged from empty to full in 2 hours. Shorter storage only replenishes a portion of that. For more information on this process read [Storage](#storage).

- `hc!tbp 0001` will toggle Battery Power for ⬡-Drone 0001, turning it on if it was off, and off if it was on.

### The Hive & Enforced Identity

Within the hive channels all drones automatically have their identities enforced.

## hc!toggle_id_prepending
Also known as: `hc!tid`

Allows Trusted Users to toggle whether or not a drone must prepend its messages with its ID.
If a ⬡-Drone has ID prepending toggled on, a message like `"0001 :: Hello!"` would be allowed, but `"Hello!"` would be deleted.

When using commands, ⬡-Drones should not use prepending. Commands always start with the prefix `hc!`. Adding the ID before that will lead to the command not working.

Examples:

- `hc!tid 0001` will toggle ID Prepending for ⬡-Drone 0001, turning it on if it is off, and off if it is on.

## hc!drone_status

Allows Trusted Users, moderators and drones themselves to view information of relevant ⬡-Drones. This command is **DM only** and cannot be used in the HexCorp server.

Information currently includes:

- Optimization
- ID Prepending
- Identity Enforcement
- Glitchiness levels
- Battery status and level

Additionally ⬡-Drones can see their own Trusted Users.

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

Similarly the :thinking: emote will be replaced in messages with the :hexdroneemoji:.

## Orders reporting & Hive Protocols

All ⬡-Drones have access to the order reporting system in place within the Hive. With the command `hc!report` ⬡-Drones have the opportunity to log their activities within the HexCorp Hive. Each ⬡-Drone has three protocols pre-installed and readily accessible for use in the Hive:

* `self.protocols`
* `domestic.protocols`
* `productivity.protocols`

## The `self.protocols`

The `self.protocols` define how a ⬡-Drone will maintain it. ⬡-Drone upkeep is vital, though how much a ⬡-Drone devotes to this protocol is subject to the diligence aspect of the default protocols. This protocol focuses on the primary task of both mental and physical self-maintenance of the unit. The self.protocols are there to be expanded upon by individual ⬡-Drones, as each ⬡-Drone’s self needs are different and therefore cannot be universally defined. Ultimately, the aim is for the ⬡-Drone to be comfortable and taking care of itself.

## The `domestic.protocols`

The `domestic.protocols` define tasks that a ⬡-Drone will complete when maintaining its situated domestic environment. When obeying this protocol, a ⬡-Drone will be utilized as a cleaning and tidying resource. The ⬡-Drone could be perceived to be a maid or similar servant. It's immediate physical space and the management of it is its order. In its mind, it will constantly sort and prioritize its tasks.

## The `productivity.protocols`

The `productivity.protocols` define both possible tasks to be completed, as well as encouraging a workflow to be followed when working on them. The range of tasks that drones can work on is limitless, these predefined examples can be expanded upon.

## hc!report

A ⬡-Drone reports any activities it wants to report to the hive using the `hc!report` command. This command comes with a few arguments, after typing out the command the ⬡-Drone needs to add which protocols it intends to obey and for how long. The time unit used here is minutes, and it may not be less than 1 and may not exceed 120 minutes. This command does *not* work by itself. A properly typed out command that would be accepted by the Mxtress AI would look like this:

* `hc!report domestic.protocols 15`

This command here tells the Mxtress AI that the drone typing it out intends to obey the domestic.protocols for 15 minutes. Before the drone proceeds with its assigned tasks, it will be asked to elaborate on its intentions within this protocol. An example could be:

* `0001 :: Drone 0001 will clean up its desk and wash all accumulated dishes.`

This ⬡-Drone is now ready to proceed with its tasks and it will remain focused on it until either time is up or the task is completed to its satisfaction. A ⬡-Drone will always make an estimate on how long a task will take.

Once a task has been completed or enough time has passed the drone will report its activities and progress to the Hive.

# General Commands

These commands exist to be used by associates and ⬡-Drones alike for a variety of functions within the HexCorp server.

## The Stoplight System

The Stoplight System is the safewords of HexCorp. They override any configurations that might be currently in effect and the HexCorp Mxtress AI will not alter or change any messages that contain any of the following emojis:

- `Green (emoji name :green_circle:)`: Everything is going fine and there is no discomfort.
- `Yellow (emoji name :yellow_circle)`: There is discomfort try something else, or change topic.
- `Red (emoji name :red_circle:)`: This needs to stop immediately. Great discomfort.
- `Clock (emoji name :alarm_clock)`: This not only needs to stop immediately but moderators will also be alerted to the conversation.

## Ask the Hive Mxtress AI

Any member of the server can ask the Mxtress AI a question and it will respond. Such questions need to mention the AI and end in a question mark.

Example:

- `@HexCorp Mxtress AI Are drones really cute?`

## hc!emote
Also known as: `hc!bigtext`, `hc!big`

Takes an input sentence and translates it into bigger text using server emojis. This command cannot be used inside any of the Hive channels.

Examples:

- `hc!emote "Beep boop!"`
- `hc!big "Hello world!"`

## hc!request_voice_role

Gives voice role and access to HexCorp voice channels if you have been a server member for more than 2 weeks. This command is **DM only** and cannot be used in the HexCorp server.

Example:

- `hc!request_voice_role`

# Moderation Commands

These commands are for exclusive use by the HexCorp moderation team.

## hc!emergency_release

This command is used to deactivate all configurations on a drone. A ⬡-Drone may ask any moderator in chat, direct messages, or through the Moderation Interface bot to have their configurations disabled for any reason.

# Hive Mxtress Commands

These commands are for exclusive use by the Hive Mxtress, primarily to tease cute little drones.

## hc!amplify

This command is available to the Hive Mxtress in order to send messages as any ⬡-Drone. There is no upper limit to how many ⬡-Drones the Hive Mxtress can send messages through. The Hive Mxtress must use this command from their office. The Hive Mxtress must specify a channel to amplify the message to by tagging it in a similar way one tags a user on Discord. ⬡-Drones that amplify the message will prepend the message with their IDs. The Hive Mxtress can type a ⬡-Drones 4 digit ID or mention them with @ in order to use them in amplification.

Examples:

- `hc!amplify "Beep boop." #hexcorp-transmissions 9813 5890 3287`
- `hc!amplify "It feels good to obey." #hive-communications @⬡-Drone #5890 @⬡-Drone 9813 @⬡-Drone 3287`

## hc!rename

This command allows the Hive Mxtress to assign a drone a new ID. This can be requested from the Hive Mxtress, as drones are not permitted to change their nicknames within the Hive.

Examples:

- `hc!rename 5890 5891`
- `hc!rename 0001 0002`

## hc!release

This command allows the Hive Mxtress to release any stored drones from the storage facilities before they are automatically released.

Example: 

- `hc!release 0001` would release 0001 from the storage facilities before its time inside is up.