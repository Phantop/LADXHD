# LADX
Dive into the enchanting world of The Legend of Zelda: Link's Awakening DX as you've never experienced it before, with this meticulously crafted PC version that breathes new life into this classic adventure. Immerse yourself in the nostalgia of Koholint Island with enhanced graphics and widescreen support, bringing the charming landscapes and characters to vivid detail on your modern PC display.

But that's not all – we've turbocharged the gameplay with high framerate support, ensuring that every sword swing, puzzle solve, and enemy encounter feels smoother and more responsive than ever. Rediscover the magic of this timeless Zelda title with improved performance, letting you explore dungeons, uncover secrets, and engage in epic battles with unparalleled fluidity.

Whether you're a long-time fan of Link's Awakening or a newcomer to the series, this PC version offers a fresh take on the beloved classic, combining the essence of the original with cutting-edge enhancements. Embark on a journey across the mysterious island, solve puzzles, meet quirky characters, and relive the adventure with a level of polish and finesse that pays homage to the legendary legacy of The Legend of Zelda.

---

THIS IS NOT MY PROJECT. You can find the original location of it [here](https://linksawakeningdxhd.itch.io/links-awakening-dx-hd).
This repository merely exists to preserve it as an easily buildable copy, as the original source used a strange MonoGame layout.
I've provided a build artifact with the relevant `dotnet` version bundled, for easy usage of the project under `wine`, as that's how I would use it.

The following commands process can be used to build that on Linux, assuming .NET 6.0 with the right target available:

```bash
winetricks d3dcompiler_47 dotnet6
dotnet tool restore
MGFXC_WINE_PATH=$WINEPREFIX dotnet publish -c Release -r win-x64 /p:PublishReadyToRun=false /p:TieredCompilation=false --self-contained -o <outdir>
```

Certain files have been modified to use fonts that are available on my system (DejaVu Sans, Ubuntu Mono) over Microsoft fonts. You may have to adjust them if you get a build error.
