[![Contributors][contributors-shield]][contributors-url]
[![Issues][issues-shield]][issues-url]
[![Donate][donate-shield]][donate-url]
[![GitHub][license-badge]][license-url]
[![CodeFactor][codefactor-badge]][codefactor-url]

### 2bored2wait

[This is a fork of the original with my personal improvements](https://github.com/themoonisacheese/2bored2wait)\
A proxy to wait out 2b2t.org's way too long queue. Includes a small webserver a REST-like API for external control

[Report Bug](https://github.com/themoonisacheese/2bored2wait/issues) | [Request Feature](https://github.com/themoonisacheese/2bored2wait/issues)

<details closed="closed">
<summary>Table of Contents</summary><p>

1. [About The Project](#about-the-project)
   - [Built With](#built-with)
2. [Getting Started](#getting-started)
   - [Prerequisites](#prerequisites)
   - [Installation](#installation)
3. [How to use](#how-to-use)
4. [Configuration](#configuration)
5. [Roadmap and known issues](#roadmap-and-known-issues)
6. [Contributing](#contributing)
7. [License](#license)
8. [Testing](#testing)

</p></details>

<!-- ABOUT THE PROJECT -->

## About The Project

A proxy to wait out 2b2t.org's way too long queue.
The ETA is calculated based on position in the queue. This results in better ETA most of the time.

### Built With

- [Node](https://nodejs.org)
- [Npm](https://npmjs.com)
- [Mc Proxy](https://www.npmjs.com/package/@rob9315/mcproxy)
- [Boxen](https://www.npmjs.com/package/boxen)
- [Config](https://www.npmjs.com/package/config)
- [Discord.js](https://www.npmjs.com/package/discord.js)
- [Everpolate](https://www.npmjs.com/package/everpolate)
- [Luxon](https://www.npmjs.com/package/luxon)
- [Minecraft Protocol](https://www.npmjs.com/package/minecraft-protocol)
- [Mineflayer AntiAFK](https://www.npmjs.com/package/mineflayer-antiafk)
- [Node Json Minify](https://www.npmjs.com/package/node-json-minify)
- [Open](https://www.npmjs.com/package/open)
- [Particles.js](https://www.npmjs.com/package/particles.js)
- [RSS Parser](https://www.npmjs.com/package/rss-parser)
- [Nexe](https://www.npmjs.com/package/nexe)

<!-- GETTING STARTED -->

# Getting Started

To get a local copy up and running follow these simple steps.

## Prerequisites

Please optain all required items

- A discord bot (optional) ([detailed instructions](https://discordpy.readthedocs.io/en/stable/discord.html))

## Installation

Read the code to ensure I'm not stealing your credentials. I'm not, but you shouldn't take my word for it. If you don't know how to read it, downloading stuff off the internet and giving it your password is probably a bad idea anyway.

### Installing via bash

```bash
git clone https://github.com/GoodPro712/2bored2wait && cd 2bored2wait
nano ./config/default.json
npm install
npm start
```

### Docker

1. Read the code to ensure I'm not stealing your credentials. I'm not, but you shouldn't take my word for it. If you don't know how to read it, downloading stuff off the internet and giving it your password is probably a bad idea anyway.
2. `docker run -d -p 80:8080 -p 25565:25565 -e NODE_CONFIG='{"username":"user@domain.com","mcPassword":"password","updatemessage":"n","BotToken":""}' 2bored2wait/2bored2wait:latest`. The docker image is automatically up to date after each push to this repo. Docker images are available for `amd64` and `arm64` among other platforms.
3. Open a browser and navigate to http://localhost
4. Press the "Start queuing" button. The queue position indicator auto-updates, but sometimes it takes a while to start counting (like 1 min).
5. Once the queue reaches a low number, connect to the Minecraft server at address `localhost`.
6. After you log off, click the "stop queuing" button. This is really important, as you will not actually disconnect from 2b2t until you do that.

If you want to change the configuration or you don't want your credentials in the bash history you will have to mount config/local.json manually.

# Configuration

- You can change all credentials and whether you want update messages by simply editing the values in local.js or deleting that file.

# How to use

1. Read the code to ensure I'm not stealing your credentials. I'm not, but you shouldn't take my word for it. If you don't know how to read it, downloading stuff off the internet and giving it your password is probably a bad idea anyway.
2. Run `npm start`
3. It will now ask for your Minecraft email and password (or permission to use saved launcher data instead). If you want update messages then you need to type Y otherwise N. If you are using the discord bot you need to add your token. Then answer Y or N if you want to save your Minecraft credentials. If you answer N you will need to re-enter your Minecraft login information into the console each time you start the program.
4. Refer to Commands on how to use 2b2w from the console. Otherwise keep on reading for the web interface.
5. Now open a browser and navigate to http://localhost: your web port here (default 80).
6. Press the "Start queuing" button. The queue position indicator auto-updates, but sometimes it takes a while to start counting (like 1 min).
7. Once the queue reaches a low number, connect to the Minecraft server at address `localhost`.
8. After you log off, click the "stop queuing" button. This is really important, as you will not actually disconnect from 2b2t until you do that.

## Commands

All commands can be used through discord or simply typed in the console window.

- `start` will start the queue. It takes between 15-30 seconds for the bot to update with the queue position.
- `start 14:00` will start at 2pm.
- `play 8:00` will try to calculate the right time to join so you can play at 8:00
- `update` will send an update to the current channel with your position and ETA.
- `stop` will stop the queue.

<!-- ROADMAP -->

# Roadmap and known issues

See the [open issues](https://github.com/themoonisacheese/2bored2wait/issues) for a list of proposed features (and known issues).

- Starting the queue will revoke your Minecraft token. this means that you will not be able to join normal Minecraft servers until you restart the game
- If you connect after the queue is finished or reconnect the proxy will send cached data. Otherwise you would fly in an empty world. However not all data will be resend. You can move out of render distance (I find going through a nether portal works best) and return to fix this issue. Sometimes the client renders a cached chunk with a blank texture.

<!-- CONTRIBUTING -->

## Contributing

Contributions are what make the open source community such an amazing place to be learn, inspire, and create. Any contributions you make are **greatly appreciated**.

1. Fork the Project
2. Create your Feature Branch (`git checkout -b feature/AmazingFeature`)
3. Commit your Changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the Branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

<!-- LICENSE -->

## License

Distributed under the GPL-3.0 License. See [`LICENSE`][license-url] for more information.

<!-- ACKNOWLEDGEMENTS -->

<!-- MARKDOWN LINKS & IMAGES -->
<!-- https://www.markdownguide.org/basic-syntax/#reference-style-links -->

[contributors-shield]: https://img.shields.io/github/contributors/goodpro712/2bored2wait.svg
[contributors-url]: https://github.com/goodpro712/2bored2wait/graphs/contributors
[issues-shield]: https://img.shields.io/github/issues/themoonisacheese/2bored2wait.svg
[issues-url]: https://github.com/themoonisacheese/2bored2wait/issues
[donate-shield]: https://img.shields.io/badge/donate-paypal-green.svg
[donate-url]: https://paypal.me/themoonisacheese?locale.x=fr_FR
[codefactor-badge]: https://www.codefactor.io/repository/github/goodpro712/2bored2wait/badge
[codefactor-url]: https://www.codefactor.io/repository/github/goodpro712/2bored2wait
[license-badge]: https://img.shields.io/github/license/goodpro712/2bored2wait 
[license-url]: https://github.com/GoodPro712/2bored2wait/blob/master/LICENSE
