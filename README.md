# Laby API Documentation
> [!NOTE]
> These docs are in no way associated with LabyMedia, some endpoints may be missing or incorrect.

> [!WARNING]
> The Laby API is not made as a public API, stability of the API is not guaranteed.

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
**Endpoint:** `GET /api/v3/user/:uuid/names`

**Description:** This returns the profile names of an UUID.

**Request:**
```http
GET /api/v3/user/069a79f4-44e9-4726-a5be-fca90e38aaf5/names
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
    ...
]
```

## Player UUID to socials
**Endpoint:** `GET /api/v3/user/:uuid/socials`

**Description:** This returns the profile socials of an UUID.

**Request:**
```http
GET /api/v3/user/1dc85f66-6776-4f64-b3b5-c6f3f72155d8/socials
```

**Response:**
```json
[
    {
        "name": "n3liz",
        "service": "discord",
        "service_name": "Discord",
        "url": "https://discord.com/users/990552479659884564"
    },
    ...
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
    ...
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
    ...
]
```

## Player UUID to online status
**Endpoint:** `GET /api/v3/user/:uuid/online-status`

**Description:** This returns the labymod status of an UUID.

**Request:**
```http
GET /api/v3/user/1dc85f66-6776-4f64-b3b5-c6f3f72155d8/online-status
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
**Endpoint:** `GET /api/v3/badges`

**Description:** This returns all badges.

**Request:**
```http
GET /api/v3/badges
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
    ...
]
```

## Badge UUID to info
**Endpoint:** `GET /api/v3/badge/:uuid`

**Description:** This returns the info of a badge.

**Request:**
```http
GET /api/v3/badge/b9d1d993-8841-4346-8008-5a6ddc8bd688
```

**Response:**
```json
{
    "id": 32,
    "uuid": "b9d1d993-8841-4346-8008-5a6ddc8bd688",
    "name": "All Minecon capes",
    "description": "The account owns all existing Minecon capes"
}
```

## Badge UUID to players
**Endpoint:** `GET /api/badge/:uuid`

**Description:** This returns the UUIDs of players with the specified badge.

**Request:**
```http
GET /api/badge/b9d1d993-8841-4346-8008-5a6ddc8bd688
```

**Response:**
```json
[
    "53f7e4c8-9469-4829-997d-f9a522e04b95",
    ...
]
```

## Featured servers
**Endpoint:** `GET /api/v3/featured/servers`

**Description:** This returns featured servers.

**Request:**
```http
GET /api/v3/featured/servers
```

**Response:**
```json
[
    {
      "server_name": "hypixel",
      "nice_name": "Hypixel Network",
      "last_player_count": 56369,
      "max_players": 200000,
      "direct_ip": "mc.hypixel.net",
      "icon": "data:image/png;base64,"
    },
    ...
]
```

## Featured users
**Endpoint:** `GET /api/v3/featured/users`

**Description:** This returns featured users.

**Request:**
```http
GET /api/v3/featured/users
```

**Response:**
```json
[
    {
        "uuid": "34e57efa-5783-46c7-a9fc-890296aaba1f",
        "username": "LabyStudio",
        "name": "LabyStudio",
        "badges": [
            {
                "uuid": "ec16a378-c15b-4e6b-a856-d2220b98d3ae",
                "name": "Cape Collector",
                "description": "The account owns 4 different capes or more",
                "received_at": "2023-10-26T19:00:54+00:00"
            },
            ...
        ]
    },
    ...
]
```

## Statistics
**Endpoint:** `GET /api/v3/statistics`

**Description:** This returns database statistics.

**Request:**
```http
GET /api/v3/statistics
```

**Response:**
```json
{
    "minecraft": {
        "amount": 62724811,
        "velocity": 0.24818442749268
    },
    "labynet": {
        "amount": 57786385,
        "velocity": 0.0201997757824888,
        "contributions": []
    }
}
```
