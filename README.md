# Light Times by Sun Angle

A single-page web tool for outdoor and wildlife photographers. Pick a place and a date and it lists the morning and evening times for each light phase, based on the sun's angle above the horizon.

## What it shows

| Phase | Sun angle |
|---|---|
| Astronomical twilight | -18° to -12° |
| Nautical twilight | -12° to -6° |
| Civil twilight | -6° to 0° |
| Blue hour | -6° to -4° |
| Golden hour | -4° to +6° |
| Bird-in-flight window (clear sky) | +6° to +30° |

It also shows sunrise and sunset (with compass bearings), solar noon and the sun's height then, daylight length, and, if you enter a time of day, the sun's compass bearing and height at that moment.

## Locations

- Built-in presets, sorted alphabetically: American Prairie Reserve (Buffalo Camp, Montana), Conowingo Dam, Danube Delta (Romania), Denali National Park, Everglades National Park, Galápagos Islands (Ecuador), Grand Teton National Park, Hawk Mountain, Kakadu National Park (Australia), Kaziranga National Park (India), Miami, New York, Pantanal (Brazil), Serengeti National Park (Tanzania), Valley Forge Park, and Yellowstone National Park. Edit the `PRESETS` object and the dropdown in `index.html` to add your own.
- Or enter a US ZIP code, `latitude, longitude`, a place name, or a postal code.
- Or tap "Use my current location".

## How it works

- The sun math is the NOAA solar position algorithm, implemented in plain JavaScript with no libraries. It runs entirely in the browser.
- Times are shown in the location's own timezone, so daylight saving time is handled automatically.
- Lookups for ZIP codes, place names, and timezones use [Zippopotam.us](https://zippopotam.us) and [Open-Meteo](https://open-meteo.com) when you enter something other than a preset. Presets and coordinates need no network for the sun math.

## Notes

- Assumes a flat horizon. Trees and hills change your real light.
- Bearings are degrees clockwise from true north, not magnetic north.
- Sunrise and sunset use -0.833° to account for atmospheric refraction.

## Appearance

The page uses a dark theme on every device.

## Run locally

Open `index.html` in a browser, or serve the folder with any static web server.
