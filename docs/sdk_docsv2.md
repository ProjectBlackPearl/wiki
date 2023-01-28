<h1 class="title">SDK Documentation</h1>

Plugins can be written in any programming language that can be compiled to a native binary for either Windows, Linux, or MacOS. If possible, please provide a binary for all three of the aforementioned operating systems.

## Response Format

Plugins must output response data to a file named `results.json` using the following response schema:

```json
{
    "response": [
        { "title": "Game Title", "urls": ["https://example.com"] }
        { "title": "Game Title", "urls": ["https://example.com"] }
        { "title": "Game Title", "urls": ["https://example.com"] }
    ]
}
```

Plugins can return multiple URLs for each search result in order to support download mirrors, but we recommend returning a maximum of 4 URLs per search query for optimal performance and visuals.

## Arguments

Plugins must be able to format search queries into CLI commands using the following arguments:
- Game Name - The game name gathered from the search query.
- Result Location - The directory to save the `results.json` file to.

Example:

```bash
./plugin "minecraft" /home/user/Documents/
```