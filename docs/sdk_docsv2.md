<h1 class="title">SDK Documentation</h1>

Plugins can be written in any language if they can be compiled to a native binary, but there are some exceptions, those being: [Python](https://www.python.org) and [Lua](https://www.lua.org)

## Response Format

A plugin also has to return the data like the example below

```json
{
    "response": [
        { "title": "Game Title", "urls": ["https://example.com"] }
        { "title": "Game Title", "urls": ["https://example.com"] }
        { "title": "Game Title", "urls": ["https://example.com"] }
    ]
}
```

<blockquote id="info">
    <span>Info</span>
    <p>The data above has to be inside a file named results.json</p>
</blockquote>

it's data onto a file called `results.json` with this format

On the `urls` array, you can include an unlimited amount of URL's, but we recommend from 1 to a max of 4 urls

## Arguments

The plugin executable has to have a few CLI arguments, those being the game name and a location in that order: Game Name, Cache Location

Example:

```bash
./plugin "0ad" /home/user/Documents/
```
