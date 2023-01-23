# Bot Battlr
For this project, you’ll be building out a React application that displays a
list of available bots, among other features.

## Built with
- javascript
- html
- css
- React 

## Setup
After unbundling the project:

1. <mark>cd bot-battlr</mark>
2. Run <mark>npm install</mark> in your terminal.
3. Run <mark>json-server --watch db.json</mark>. This will run your backend port.
4. In a new terminal, run <mark>npm start</mark>. This will run your React app

## Core Deliverables
As a user, I should be able to:

- See profiles of all bots rendered in <mark>BotCollection<mark>.
- Add an individual bot to my army by clicking on it. The selected bot should render in the <mark>YourBotArmy</mark> component. The bot can be enlisted only once. The bot does not disappear from the <mark>BotCollection</mark>.
- Release a bot from my army by clicking on it. The bot disappears from the <mark>YourBotArmy</mark> component.
- Discharge a bot from their service forever, by clicking the red button marked "x", which would delete the bot both from the backend and from the <mark>YourBotArmy</mark> on the frontend.

## Endpoints for Core Deliverables

### GET /bots
Example Response:

    [
      {
        "id": 101,
        "name": "wHz-93",
        "health": 94,
        "damage": 20,
        "armor": 63,
        "bot_class": "Support",
        "catchphrase": "1010010101001101100011000111101",
        "avatar_url": "https://robohash.org/nostrumrepellendustenetur.png?size=300x300&set=set1",
        "created_at": "2018-10-02T19:55:10.800Z",
        "updated_at": "2018-10-02T19:55:10.800Z"
      },
      {
        "id": 102,
        "name": "RyM-66",
        "health": 86,
        "damage": 36,
        "armor": 77,
        "bot_class": "Medic",
        "catchphrase": "0110011100000100011110100110011000011001",
        "avatar_url": "https://robohash.org/quidemconsequaturaut.png?size=300x300&set=set1",
        "created_at": "2018-10-02T19:55:10.827Z",
        "updated_at": "2018-10-02T19:55:10.827Z"
      }
    ]

### DELETE /bots/:id
Example Response:
    
    {}

## Advanced Deliverables

As a user, I should be able to:

- Choose if I want to enlist a bot into my army or just see their data. Clicking on the card should instead display a show view <mark>(BotSpecs)</mark> for that bot, which should replace <mark>BotsCollection</mark>. BotSpecs should have two buttons: one to go back to the list view and another to enlist that bot.
- Sort bots by their health, damage or armor. For this, create a new component, <mark>SortBar</mark>.
- When I enlist a bot it will be removed from the <mark>BotCollection</mark> and added to <mark>YourBotArmy</mark>.
- Filter bots by their class. We can select a few filters at the same time.
- Sort bots by their health, damage or armor. For this, create a new component, <mark>SortBar</mark>.
- Only enlist one bot from each <mark>bot_class</mark>. The classes are <mark>["Support", "Medic", "Assault", "Defender", "Captain", "Witch"]</mark>.

