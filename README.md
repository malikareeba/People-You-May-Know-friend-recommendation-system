# People-You-May-Know-friend-recommendation-system
People You May Know – A Python-based friend recommendation system that suggests potential friends based on mutual connections. Perfect for learning social network algorithms and building lightweight recommendation engines.

# People You May Know Recommendation System

A Python project that recommends potential friends to users based on their mutual connections. Inspired by social media platforms, it identifies friends-of-friends who a user might know.

## Features

- Loads user and page data from a JSON file (`data.json`)
- Computes friend recommendations based on mutual friends
- Ranks suggestions by number of shared connections
- Lightweight and easy to extend

## Dataset

The project uses a JSON structure with:

- **Users**: Each user has an `id`, `name`, list of `friends`, and `liked_pages`
- **Pages**: Pages that users like

Example snippet of `data.json`:

```json
{
    "users": [
        {"id": 1, "name": "Amit", "friends": [2, 3], "liked_pages": [101]},
        {"id": 2, "name": "Priya", "friends": [1, 4], "liked_pages": [102]}
    ],
    "pages": [
        {"id": 101, "name": "Python Developers"},
        {"id": 102, "name": "Data Science Enthusiasts"}
    ]
}
```
How It Works

Load user data from data.json

For a given user, find all direct friends

Check friends of those friends

Recommend users who are not already friends, ranked by number of mutual friends



