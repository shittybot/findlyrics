<div align="center">
  <h1>findlyrics</h1>
  <p>A simple package to fetch lyrics from Genius API.</p>
  <p>
  <a href="https://www.npmjs.com/package/findlyrics"><img src="https://img.shields.io/npm/v/findlyrics?maxAge=3600" alt="NPM version" /></a>
  <p>
  <p>
    <a href="https://www.npmjs.com/package/findlyrics"><img src="https://nodei.co/npm/findlyrics.png?downloads=true&stars=true" alt="NPM Banner"></a>
  </p>

  <p>This package was originally used only for my personal needs to fetch lyrics from Genius API using my discord bot, but then I decided to make this package open source and let everyone use it.</p>
  </div>
  <br>

  ## Install
```sh
npm install findlyrics
# or
yarn add findlyrics
```

## Example
```js
const findLyrics = require("findlyrics"); // Import
const { AttachmentBuilder } = require("discord.js");

client.on("interactionCreate", async (message) => {
    
    let apiKey = "GENIUS_API_KEY"; // Your Genius API Key
    let songName = "SONG_NAME"; // Song Name

    await findLyrics(apiKey, songName);

    const lyrics = findLyrics.lyrics;

    interaction.channel.send({
        content: lyrics,
    });
});

client.login("token");
```

## Usage

| Option                 | Type                   | Description                                                                                                 |
|------------------------|------------------------|-------------------------------------------------------------------------------------------------------------|
| apiKey                | String                  | Genius API Key to fetch the lyrics from their API. <br> https://genius.com/api-clients                      |
| songName              | String                  | Song name to fetch the lyrics.                                                                              |                                                                           |




