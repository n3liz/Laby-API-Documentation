# Laby Api Documentation
> [!NOTE]
> These docs are in no way associated with LabyMedia, some endpoints may be missing or incorrect.

## Username to UUID 
- ### `GET /api/v3/user/:username/uniqueId`
- This returns the UUID of an username.

```json
{
    "uniqueId": "069a79f4-44e9-4726-a5be-fca90e38aaf5",
    "username": "Notch"
}
```

## UUID to profile 
- ### `GET /api/v3/user/:uuid/profile`
- This returns the name, skin and cape history of an UUID.

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

## UUID to names
- ### `GET /api/v3/user/:uuid/names`
- This returns the profile names of an UUID.
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

## UUID to snippet
- ### `GET /api/v3/user/:uuid/snippet`
- This returns the profile snippet of an UUID.

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

## UUID to badges
- ### `GET /api/v3/user/:uuid/badges`
- This returns the profile badges of an UUID.

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

## UUID to accounts 
- ### `GET /api/v3/user/:uuid/accounts`
- This returns the profile linked accounts of an UUID.

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

## UUID to friends
- ### `GET /api/v3/user/:uuid/friends`
- This returns the profile friends of an UUID.

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

## UUID to status
- ### `GET /api/v3/user/:uuid/status`
- This returns the profile status of an UUID.

```json
{
    "status": "I should do my homework"
}
```

## UUID to views
- ### `GET /api/v3/user/:uuid/views`
- This returns the profile views of an UUID.

```json
{
    "views": 48
}
```

## UUID to hearts
- ### `GET /api/v3/user/:uuid/heart`
- This returns the profile hearts of an UUID.

```json
{
    "count": 0,
    "status": null
}
```

## UUID to emotes
- ### `GET /api/v3/user/:uuid/emotes`
- This returns the labymod emotes of an UUID.
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

## UUID to online status
- ### `GET /api/v3/user/:uuid/online-status`
- This returns the labymod status of an UUID.

```json
{
    "online":false,
    "status":"OFFLINE"
}
```

## UUID to game stats
- ### `GET /api/v3/user/:uuid/game-stats`
- This returns the labymod statistics of an UUID.

```json
{
    "first_joined": "2023-02-02T19:42:33+00:00",
    "last_online": "2023-12-11T06:35:00+00:00"
}
```
