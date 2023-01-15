<h1 class="title">SDK Documentation</h1>

<blockquote id="warning">
    <span>Warning</span>
    <p>This page has been deprecated, please read <a href="./docs/sdk_docsv2">this</a> instead</p>
</blockquote>

The plugin SDK is written in C# and it looks like this

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace PluginName
{
    internal class PluginName : Project_Black_Pearl.SDK.PBPPlugin
    {
    }
}
```

Inside the class you will put options to make your plugin, those same options are listed under [Options](#Options)

## Response Format

The response format for a Scraper is written in JSON an looks like this

```json
{
	"response": [
		{
			"Title": "Game1",
			"URL1": ["example.com"],
			"URL2": [],
			"URL3": [],
			"URL4": []
		},
		{
			"Title": "Game2",
			"URL1": ["example.com"],
			"URL2": [],
			"URL3": [],
			"URL4": []
		}
	]
}
```

## Options

| Option                        | Value                                                                                 | Optional                       |
| ----------------------------- | ------------------------------------------------------------------------------------- | ------------------------------ |
| Title                         | Has to be a String                                                                    | No                             |
| Type                          | Currently only supports "Binary"                                                      | No                             |
| isPrefetch                    | Set to `true` if it uses a Prefetch scraper, otherwise set to false                   | Yes                            |
| FirstPayloadScraper           | Path to the prefetch scraper, Only set the value if `isPrefetch` is `true`            | Yes                            |
| FirstPayloadType              | Type of the prefetch scraper, Only supports Binary and set if `isPrefetch` is `true`  | Yes                            |
| ScraperPath                   | Path to the scraper                                                                   | No                             |
| URL1Image - URL4Image         | Path to the URL image (Example: URL is Mediafire so it would link to a Mediafire Img) | Only URL1Image is required     |
| URL1Type - URL4Type           | Title to be displayed on the DL page                                                  | Only URL1Type is required      |
| URL1Validator - URL4Validator | Validades the URL sent through the scraper with this one                              | Only URL1Validator is required |

So an example of a valid plugin code would be like this

```csharp
namespace KoolPlugin
{
    internal class KoolPlugin : Project_Black_Pearl.SDK.PBPPlugin
    {
         public string Title => "KoolPlugin";
         public string Type => "Binary";

         public bool isPrefetch => false;
         public string FirstPayloadScraper => "";
         public string FirstPayloadType => "";

         public string ScraperPath => "C:\Scrapers\KoolScraper.exe";

         public string URL1Image => "C:\Image\Example.jpg";
         public string URL1Type => "Example";
         public string URL1Validator => "";

         public string URL2Image => "C:\Image\Example.jpg";
         public string URL2Type => "Example";
         public string URL2Validator => "";

         public string URL3Image => "C:\Image\Example.jpg";
         public string URL3Type => "Example";
         public string URL3Validator => "";

         public string URL4Image => "C:\Image\Example.jpg";
         public string URL4Type => "Example";
         public string URL4Validator => "";
    }
}
```
