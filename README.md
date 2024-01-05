# Laby Api Documentation
> [!NOTE]
> These docs are in no way associated with LabyMedia, some endpoints may be missing or incorrect.

> [!WARNING]
> The laby api is not made as a public api, stability of the api is not guaranteed.

## Player username to UUID 
**Endpoint:** `GET /api/v3/user/:username/uniqueId`

**Description:** This returns the UUID of an username.

**Request:**
```http
GET /api/v3/user/Notch/uniqueId
```

**Response:**
```json
{
    "uniqueId": "069a79f4-44e9-4726-a5be-fca90e38aaf5",
    "username": "Notch"
}
```

## Player UUID to profile 
**Endpoint:** `GET /api/v3/user/:uuid/profile`

**Description:** This returns the name, skin and cape history of an UUID.

**Request:**
```http
GET /api/v3/user/069a79f4-44e9-4726-a5be-fca90e38aaf5/profile
```

**Response:**
```json
{
    "uuid": "069a79f4-44e9-4726-a5be-fca90e38aaf5",
    "username": "Notch",
    "username_history": [
        {
            "username": "Notch",
            "changed_at": null,
            "accurate": true,
            "last_seen_at": "2023-12-11T17:03:45+00:00"
        }
    ],
    "textures": {
        "SKIN": [
            {
                "type": "SKIN",
                "image_hash": "f3fa11e8f7b48bf03174112285f04d99",
                "file_hash": "b77b847bd7db0dbeb86e9bc193b56ba2",
                "first_seen_at": "2022-08-14T14:10:35+00:00",
                "last_seen_at": "2023-12-11T17:03:45+00:00",
                "slim_skin": false,
                "active": true
            }
        ],
        "CLOAK": [
            {
                "type": "CLOAK",
                "image_hash": "63d21407ea2cbe6213e3c22f3be74ad5",
                "file_hash": "8a3b459f5fd17b28be473aa84b7e36ee",
                "first_seen_at": "2021-04-22T17:29:03+00:00",
                "last_seen_at": "2021-07-05T19:22:43+00:00"
            }
        ]
    }
}
```

## Player UUID to names
**Endpoint:** `GET /api/v3/user/069a79f4-44e9-4726-a5be-fca90e38aaf5/names`

**Description:** This returns the profile names of an UUID.

**Request:**
```http
GET /api/v3/user/:uuid/names
```

**Response:**
```json
[
    {
        "username": "Notch",
        "changed_at": null,
        "accurate": true,
        "last_seen_at": "2023-12-11T20:55:56+00:00"
    }
]
```

## Player UUID to snippet
**Endpoint:** `GET /api/v3/user/:uuid/snippet`

**Description:** This returns the profile snippet of an UUID.

**Request:**
```http
GET /api/v3/user/069a79f4-44e9-4726-a5be-fca90e38aaf5/snippet
```

**Response:**
```json
{
    "user": {
        "uuid": "069a79f4-44e9-4726-a5be-fca90e38aaf5",
        "username": "Notch"
    },
    "role": {
        "nice_name": "LabyMod+",
        "color_minecraft": "e"
    },
    "settings": {
        "background": "NONE"
    },
    "name_history": [
        {
            "username": "Notch",
            "changed_at": null,
            "accurate": true,
            "last_seen_at": "2023-12-11T19:02:46+00:00"
        }
    ],
    "badges": [
        {
            "uuid": "cb7f5156-2825-4064-8631-6423d76faf0f",
            "name": "Notch",
            "description": "The founder of Minecraft",
            "received_at": "2009-05-09T22:00:00+00:00"
        }
    ]
}
```

## Player UUID to badges
**Endpoint:** `GET /api/v3/user/:uuid/badges`

**Description:** This returns the profile badges of an UUID.

**Request:**
```http
GET /api/v3/user/069a79f4-44e9-4726-a5be-fca90e38aaf5/badges
```

**Response:**
```json
[
    {
        "uuid": "cb7f5156-2825-4064-8631-6423d76faf0f",
        "name": "Notch",
        "description": "The founder of Minecraft",
        "received_at": "2009-05-09T22:00:00+00:00"
    }
]
```

## Player UUID to accounts 
**Endpoint:** `GET /api/v3/user/:uuid/accounts`

**Description:** This returns the profile linked accounts of an UUID.

**Request:**
```http
GET /api/v3/user/1dc85f66-6776-4f64-b3b5-c6f3f72155d8/accounts
```

**Response:**
```json
[
    {
        "user_name": "MentallyBurdened",
        "uuid": "66429d89-60f0-4084-8a14-1fae3f3510b4",
        "color_minecraft": null,
        "main": false
    },
    {
        "user_name": "BurdenedMentally",
        "uuid": "5363e2dd-a746-4dab-926c-6ef2f1fca31d",
        "color_minecraft": null,
        "main": false
    }
]
```


## Player UUID to socials
**Endpoint:** `GET /api/v3/user/:uuid/socials`

**Description:** This returns the profile socials of an UUID.

**Request:**
```http
GET /api/v3/user/22500b81-e889-4367-b83c-24c52914e2de/socials
```

**Response:**
```json
[
  {
    "name": "kacinas#6666",
    "service": "discord",
    "service_name": "Discord",
    "url": "https://discord.com/users/755452572680192101"
  },
  {
    "name": "gabija",
    "service": "spotify",
    "service_name": "Spotify",
    "url": "https://open.spotify.com/user/eoe6mmbaqhe0cqzsk5mzteuck"
  }
]
```



## Player UUID to friends
**Endpoint:** `GET /api/v3/user/:uuid/friends`

**Description:** This returns the profile friends of an UUID.

**Request:**
```http
GET /api/v3/user/1dc85f66-6776-4f64-b3b5-c6f3f72155d8/friends
```

```json
[
    {
        "uuid": "74843df9-40ad-4cbe-904c-2cee69ef7581",
        "user_name": "Northernside",
        "role_color": "e"
    },
    {
        "uuid": "c1d2e315-7c3a-4a97-8a8e-ffd188cad54d",
        "user_name": "PocketSage",
        "role_color": "e"
    },
    {
        "uuid": "3978b06d-f10f-474c-a44c-0cb1711e166d",
        "user_name": "flamyamy",
        "role_color": null
    }
]
```

## Player UUID to status
**Endpoint:** `GET /api/v3/user/:uuid/status`

**Description:** This returns the profile status of an UUID.

**Request:**
```http
GET /api/v3/user/1dc85f66-6776-4f64-b3b5-c6f3f72155d8/status
```

**Response:**
```json
{
    "status": "I should do my homework"
}
```

## Player UUID to views
**Endpoint:** `GET /api/v3/user/:uuid/views`

**Description:** This returns the monthly profile views of an UUID.

**Request:**
```http
GET /api/v3/user/1dc85f66-6776-4f64-b3b5-c6f3f72155d8/views
```

**Response:**
```json
{
    "views": 48
}
```

## Player UUID to hearts
**Endpoint:** `GET /api/v3/user/:uuid/heart`

**Description:** This returns the profile hearts of an UUID.

**Request:**
```http
GET /api/v3/user/1dc85f66-6776-4f64-b3b5-c6f3f72155d8/heart
```

**Response:**
```json
{
    "count": 0,
    "status": null
}
```

## Player UUID to emotes
**Endpoint:** `GET /api/v3/user/:uuid/emotes`

**Description:** This returns the labymod emotes of an UUID.

**Request:**
```http
GET /api/v3/user/1dc85f66-6776-4f64-b3b5-c6f3f72155d8/emotes
```

**Response:**
```json
[
    {
        "emote_id": 40,
        "name": "Freezing",
        "rare": false
    },
    {
        "emote_id": 47,
        "name": "Chicken",
        "rare": false
    },
    {
        "emote_id": 122,
        "name": "Airplane",
        "rare": false
    },
    {
        "emote_id": 149,
        "name": "Fall",
        "rare": false
    },
    {
        "emote_id": 209,
        "name": "Sweat Wipe",
        "rare": false
    },
    {
        "emote_id": 314,
        "name": "Magic Trick",
        "rare": false
    }
]
```

## Player UUID to online status
**Endpoint:** `GET /api/v3/user/:uuid/online-status`

**Description:** This returns the labymod status of an UUID.

**Request:**
```http
GET /api/v3/user/1dc85f66-6776-4f64-b3b5-c6f3f72155d8/emotes
```

**Response:**
```json
{
    "online":false,
    "status":"OFFLINE"
}
```

## Player UUID to game stats
**Endpoint:** `GET /api/v3/user/:uuid/game-stats`

**Description:** This returns the labymod statistics of an UUID.

**Request:**
```http
GET /api/v3/user/1dc85f66-6776-4f64-b3b5-c6f3f72155d8/game-stats
```

**Response:**
```json
{
    "first_joined": "2023-02-02T19:42:33+00:00",
    "last_online": "2023-12-11T06:35:00+00:00"
}
```

## Badges
**Endpoint:** `GET /api/badges`

**Description:** This returns all badges.

**Request:**
```http
GET /api/badges
```

**Response:**
```json
[
    {
        "id": 25,
        "uuid": "849ecc93-e70b-11eb-8891-d67b6288368f",
        "name": "Duplicate Name",
        "description": "The name of the user exists twice in the Minecraft database"
    },
    {
        "id": 4,
        "uuid": "ababd9c9-4679-495b-b4cf-6abaecb8780f",
        "name": "1 millionth LabyMod user",
        "description": "1 millionth user who started LabyMod"
    },
    {
        "id": 21,
        "uuid": "6c906e28-1985-48e5-bc6e-71871d4d467e",
        "name": "Indev Account",
        "description": "User bought the game during the INDEV development phase of Minecraft (2009-12-23 - 2010-02-26)"
    },
    {
        "id": 5,
        "uuid": "775463d9-9451-4591-839b-b48f970501da",
        "name": "2 millionth LabyMod user",
        "description": "2 millionth user who started LabyMod"
    },
    {
        "id": 10,
        "uuid": "7e6e788e-5aed-48c0-89e5-496f507af63b",
        "name": "Streak II",
        "description": "Reached a streak of 730 days. That's two years!"
    },
    {
        "id": 8,
        "uuid": "205cedeb-5751-4f12-97e6-7108d043a191",
        "name": "Cosmetic Collector",
        "description": "The user has as many cosmetics (or more) as are currently for sale in the LabyMod shop right now."
    },
    {
        "id": 12,
        "uuid": "c4ff9256-7a6f-4382-ba6d-2d0a68c9dbe2",
        "name": "First registered LabyMod user",
        "description": "First user in the database who logged in with LabyMod"
    },
    {
        "id": 23,
        "uuid": "2aaaaec5-b64d-4f11-8e15-5bf7b866c0ff",
        "name": "Alpha Account",
        "description": "User bought the game during the ALPHA development phase of Minecraft (2010-06-30 - 2010-12-19)"
    },
    {
        "id": 1,
        "uuid": "cbcf5a7c-d325-4c5e-b918-adbc98343195",
        "name": "LabyMod Staff",
        "description": "Owned by all people who are in the LabyMod staff team"
    },
    {
        "id": 35,
        "uuid": "cc1ca024-d872-41be-b7b3-143469f5cc89",
        "name": "Music Composer",
        "description": "The user has its own music disc in Minecraft"
    },
    {
        "id": 30,
        "uuid": "4f8cb11e-5871-487c-bf33-78b1e7a51628",
        "name": "First name change",
        "description": "First known name change of a Minecraft account"
    },
    {
        "id": 22,
        "uuid": "2ef6f19a-84cb-43f9-a18d-404d95f74abc",
        "name": "Infdev Account",
        "description": "User bought the game during the INFDEV development phase of Minecraft (2010-02-27 - 2010-06-29)"
    },
    {
        "id": 31,
        "uuid": "19269c18-428a-4cc1-8992-045a2ce7fc4f",
        "name": "Upside down!",
        "description": "The player appears upside down in the game"
    },
    {
        "id": 16,
        "uuid": "e6f95adf-f67c-4e80-a5ce-71632d9e6f7e",
        "name": "Oldest known account",
        "description": "Oldest known Minecraft account on this page"
    },
    {
        "id": 2,
        "uuid": "cb7f5156-2825-4064-8631-6423d76faf0f",
        "name": "Notch",
        "description": "The founder of Minecraft"
    },
    {
        "id": 11,
        "uuid": "6188c82e-65fd-413c-b7d5-aa02ed5220b8",
        "name": "Streak III",
        "description": "Reached a streak of 1095 days. That's three years!"
    },
    {
        "id": 34,
        "uuid": "ec16a378-c15b-4e6b-a856-d2220b98d3ae",
        "name": "Cape Collector",
        "description": "The account owns 4 different capes or more"
    },
    {
        "id": 40,
        "uuid": "f1529609-6d8c-48bf-ad4f-160d51424136",
        "name": "Contributor 1M",
        "description": "This user has contributed at least 1,000,000 new UUIDs to the laby.net database."
    },
    {
        "id": 15,
        "uuid": "ce1e18de-2b71-4f3e-9390-ff0e0267a829",
        "name": "Invalid name",
        "description": "Minecraft name contains an invalid character or is too long"
    },
    {
        "id": 28,
        "uuid": "9c5dfe59-0265-11ec-8891-d67b6288368f",
        "name": "Addon Developer",
        "description": "The user developed an addon for LabyMod which got published in the addon store"
    },
    {
        "id": 38,
        "uuid": "2d4cb121-97af-4c4c-9bae-eedbde831e18",
        "name": "Contributor 10K",
        "description": "This user has contributed at least 10,000 new UUIDs to the laby.net database."
    },
    {
        "id": 36,
        "uuid": "87fb1dde-0d16-410f-9991-399230bfd161",
        "name": "Name Sniper",
        "description": "The user changed the name in the first minute when the name change feature was introduced. This officially makes the user one of the first users to change their name. (2015-02-04 10:11:00 GMT)"
    },
    {
        "id": 3,
        "uuid": "a4d53924-7fa7-4d27-bda7-dd88ab72d10e",
        "name": "Translator",
        "description": "Translated 100 proofed strings for LabyMod into another language"
    },
    {
        "id": 33,
        "uuid": "bf18559d-0666-11ec-8891-d67b6288368f",
        "name": "Tag Contributor",
        "description": "The player has added more than 100 approved tags or voted for 1000 approved tags on skins or cloaks"
    },
    {
        "id": 41,
        "uuid": "b28c0122-c31c-4c7e-86c4-e29d42cec639",
        "name": "Gamescom 2023",
        "description": "This user solved the puzzles at Gamescom 2023 and has met the LabyMod team."
    },
    {
        "id": 32,
        "uuid": "b9d1d993-8841-4346-8008-5a6ddc8bd688",
        "name": "All Minecon capes",
        "description": "The account owns all existing Minecon capes"
    },
    {
        "id": 13,
        "uuid": "cf1a4143-536b-426a-b3da-3f25f75d011f",
        "name": "Highest Streak",
        "description": "User has the highest LabyMod streak"
    },
    {
        "id": 19,
        "uuid": "a5b3473c-6ff2-4ae4-b839-1a6b7299abf7",
        "name": "Gift by Mojang",
        "description": "Received a unique cosmetic or cape by Mojang"
    },
    {
        "id": 26,
        "uuid": "30cf1005-c1b1-4577-a231-6034f9ecb580",
        "name": "Most name changes",
        "description": "The user has the most name changes with their Minecraft account"
    },
    {
        "id": 18,
        "uuid": "fa886cfe-209c-46eb-ad1f-92d7f0bc979c",
        "name": "Short name",
        "description": "The Minecraft name of the user has only one or two characters"
    },
    {
        "id": 7,
        "uuid": "6a7fde84-8b75-4efc-87d5-d87d1d4ab13a",
        "name": "4 millionth LabyMod user",
        "description": "4 millionth user who started LabyMod"
    },
    {
        "id": 6,
        "uuid": "31cd1b60-c311-4e47-9356-0438b54d2733",
        "name": "3 millionth LabyMod user",
        "description": "3 millionth user who started LabyMod"
    },
    {
        "id": 39,
        "uuid": "94165579-5c52-4a66-ad78-0d3676b98cc1",
        "name": "Contributor 100K",
        "description": "This user has contributed at least 100,000 new UUIDs to the laby.net database."
    },
    {
        "id": 9,
        "uuid": "84b62975-c8ea-4bc1-a40c-c697794719db",
        "name": "Streak I",
        "description": "Reached a streak of 365 days. That's an entire year!"
    },
    {
        "id": 17,
        "uuid": "629b36dc-5c0b-4a3c-85bf-ea111954f6fa",
        "name": "Mojang Staff",
        "description": "User is a Mojang employee"
    },
    {
        "id": 27,
        "uuid": "2f5b32ed-f040-11eb-8891-d67b6288368f",
        "name": "Previously invalid name",
        "description": "The user has an invalid name in their past name history"
    },
    {
        "id": 42,
        "uuid": "801238c1-6530-11ee-879f-7203584a0c68",
        "name": "Nitro Booster",
        "description": "This user is currently boosting the laby.net discord server."
    },
    {
        "id": 14,
        "uuid": "667735b8-1d60-40aa-a378-2f76765025ae",
        "name": "OG Name",
        "description": "The Minecraft name of the user is either a well-known first name, one of the most commonly used English words (including Fruits, Animals, Sports, ...) or a word known from Minecraft.\nhttps://github.com/LabyMod/og-names"
    },
    {
        "id": 20,
        "uuid": "d7971a18-f065-4306-878b-03ada3d1892e",
        "name": "Classic Account",
        "description": "User bought the game during the CLASSIC development phase of Minecraft (2009-05-16 - 2009-12-22)"
    },
    {
        "id": 24,
        "uuid": "460d76ab-bc4d-453e-9a62-3ff57f7bf285",
        "name": "Beta Account",
        "description": "User bought the game during the BETA development phase of Minecraft (2010-12-20 - 2011-11-17)"
    },
    {
        "id": 37,
        "uuid": "10394114-ea16-4978-bb1e-f59e13e2499d",
        "name": "Invalid UUID",
        "description": "The user has an invalid UUID. It does not comply with the UUIDv4 standard."
    },
    {
        "id": 29,
        "uuid": "bec8cd00-a3d5-4992-9c91-0d1db9c3f2be",
        "name": "All emotes",
        "description": "The user owns all existing LabyMod emotes"
    }
]
```

## Badge UUID to player UUID(s)
**Endpoint:** `GET /api/badge/:uuid`

**Description:** This returns the UUID(s) of players with the specified badge.

**Request:**
```http
GET /api/badge/b9d1d993-8841-4346-8008-5a6ddc8bd688
```

**Response:**
```json
[
    "53f7e4c8-9469-4829-997d-f9a522e04b95",
    "1ccef50b-f6ae-4542-b1a9-d434384a5b25",
    "30135bad-a576-4477-8dd6-61c9f5dd5839"
]
```

**Note** For some unknown reason, the Translator badge doesn't work here.
