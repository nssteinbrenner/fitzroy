# Fitzroy

![example](images/example.png)

Fitzroy is a custom module for Waybar to check the weather, and render the information in a pretty format.

Currently, both PirateWeather and OpenWeatherMap's OneCall API are both supported.

## Installation
To configure Waybar, set up a `custom/fitzroy` block in your config.jsonc referring to the script.
Be sure to set the `return-type` to `json`.
```
{
    "modules-center": ["custom/fitzroy"],
    "custom/fitzroy": {
        "exec": "~/bin/fitzroy",
        "interval": 600,
        "return-type": "json",
    {
}
```

In your style.css file, you can refer to it by `#custom-fitzroy`:
```
#custom-fitzroy {
    color: #EBDBB2;
}
```

There is a configuration file `config.toml` where you can specify which APIs are enabled, as well as supply API keys, URLs, and customize the icons and colors.
See config.toml in this repository for an example.
