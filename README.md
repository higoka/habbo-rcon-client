# habbo-rcon-client
The frontend application for [habbo-rcon-server](https://github.com/higoka/habbo-rcon-server)

### Setup
1. Download this repo and extract it.
2. Open terminal and `cd` inside the folder then run `npm i`
3. Rename `.env.example` to `.env` and change the `API_HOST`. This should be the host where [habbo-rcon-server](https://github.com/higoka/habbo-rcon-server) is running.
4. Run `npm run-script build` to recompile the project to the latest updates.


Now the project is up-to-date. The only thing left is to host it.
Setup your webserver to use the `public` folder as the root directory.

### Compiling
When you change something inside `src/` folder you need to recompile the project.
To do so simply open a terminal and run `npm run-script build`.
