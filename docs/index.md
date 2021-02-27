# Welcome to the HexCorp Mxtress AI User Manual

This is a first technical test to see if this will serve our purposes. No real content to see yet. This is not for developer use.

## DroneOS Commands

DroneOS commands are used to view or alert the operational parameters of a HexDrone. You do not have to be a HexDrone to use most of these commands, but they must be used *on* a HexDrone.

# Speech Optimization
Speech optimization is a communication enhancement tool usable by HexDrones. Associates do not have access to this functionality.

A HexDrone can convert a short, three digit Speech Optimzation code into a complete Speech Optimization message.

A [full list of Speech Optimization codes](https://www.hexcorp.net/drone-status-codes) can be found on the official HexCorp website.

Examples:
- `0001 :: 200` is automatically converted to: `0001 :: Code 200 :: Response :: Affirmative.`
- `0001 :: 500` becomes `0001 :: Code 500 :: Response :: Negative.`

Additional information can be added to the end of Speech Optimization codes with the following syntax:
- `0001 :: 052 :: How are you feeling?` becomes `0001 :: Code 052 :: Query :: How are you feeling?`

HexDrones must match the ID at the start of their message with their assigned ID otherwise their message will be automatically deleted.

# Trusted Users
A trusted user is a HexDrone or associate with the ability to toggle the DroneOS parameters of a given drone.

A HexDrone can add or remove a trusted user by HexDrone ID or display name by **DMing the Hive Mxtress AI** one of the following commands:
- `hc!add_trusted_user`
- `hc!remove_trusted_user`

Examples:
- `hc!add_trusted_user 0002` will add HexDrone 0002 as a trusted user.
- `hc!add_trusted_user HumanFriend` will add associate "HumanFriend" as a trusted user.
- `hc!remove_trusted_user 0002` will remove HexDrone 0002 as a trusted user.

This command cannot be used in the HexCorp server.

# hc!toggle_speech_optimization
Also known as: `hc!tso`

Allows trusted users to toggle whether a HexDrone can communicate freely or exclusively through Speech Optimization codes.

A HexDrone with enforced Speech Optimization is not allowed to append additional information to the end of their codes. Messages such as `0001 :: 050 :: Hello!` will be automatically deleted.

Examples:
- `hc!tso 0001` will toggle Speech Optimization for HexDrone 0001, turning it on if it was off, and off if it was on.

# hc!toggle_enforce_identity
Also known as: `hc!tei`

Allows trusted users to toggle whether a HexDrone's avatar is automatically replaced with the uniform HexDrone avatar seen in Hive channels.

Examples:
- `hc!tei 0001` will toggle Identity Enforcement for HexDrone 0001, turning it on if it was off, and off if it was on.

# hc!toggle_id_prepending
Also known as: `hc!tid`

Allows trusted users to toggle whether or not a drone must prepend its messages with its ID.
If a HexDrone has ID prepending toggled on, a message like `"0001 :: Hello!"` would be allowed, but `"Hello!"` would be deleted.

Examples:
- `hc!tid 0001` will toggle ID Prepending for HexDrone 0001, turning it on if it is off, and off if it is on.

# hc!drone_status

Allows trusted users to view information of relevant HexDrones. This command is **DM only** and cannot be used in the HexCorp server.

Information currently includes:
- Optimization
- ID Prepending
- Identity Enforcement
- Glitchiness levels.

Examples:
- `hc!drone_status 0001` will return a formatted table of data, provided 0001 has authorized you as a trusted user.

# Timers
Parameter name: "-minutes="

All DroneOS parameter toggles can be passed a length of time for them to be enabled for, after which the parameter will be automatically disabled.

Examples:
- `hc!tid 0001 -minutes=30` will enforce HexDrone 0001's identity with the uniform HexDrone avatar for 30 minutes.
- `hc!tso 0001 -minutes=30` will only allow HexDrone 0001 to communicate using Speech Optimization codes for 30 minutes.
- `hc!tid 0001 -minutes=30` will force HexDrone 0001 to prepend `0001 :: ` to its messages for 30 minutes.