# Svelte Single File
This is a template repository focused on building small web apps. When you build this project the resulting file is a single `index.html` with all assets inlined. While I made this project with the focus of building/minting HTML NFTs, it really could be used for anything.

## Get Started
Clone and `npm install` this repo on your computer. Next we will need to setup a dev command, but first I need to explain app configs.

## App Configs
Build configs let you use the same code and components to build multiple versions of the same experience. For example, I released 3 versions of Bitsweeper that were different color themes and board sizes. The underlying code for all of the games is exactly the same, all that changes is the game/build config that's passed into them which looks rougly like the following.

```json
{
    "theme" : "var(--color-red)",
    "title" : "Red Edition",
    "size": 4,
    "poison": [
        [1,1],
        [0,3],
        [3,2],
        [3,0]
    ]
}
```

A config can include anything your want, any settings or details you want to pass to your app. The only requirement is that it is a valid JSON file.

#### Config Files
Config files need to be placed in the `config` folder. There is a default empty config already setup at `config/default.json`. You can use/edit this one or add additional configs as you need.

#### Add Config File
To add a config file, add a new `.json` file to the `config` folder.

#### Link Config File
How the app determines which config file to use is based on the script you start the project with. See `package.json`, notice how under the `scripts` property there are some scripts that start with `dev:` and `build:`? To build with a specific config file, all you have to do is make sure you add another script where the name of your file comes after the `:`. The `vite` and `vite build` values should be the same for all dev/build scripts.




