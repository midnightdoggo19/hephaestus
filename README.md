# Hephaestus
A python script to try and download as many neoforge mods on a given Minecraft version, from Modrinth. Named for the Greek god of blacksmiths.

The script is not perfect, and currently will miss a lot of mods. This is definitely not playable, it may have some XML content in some of the jar files, download duplicates, and miss plenty of mods. If you're actually trying to play this later on... good luck.
**The creator is not liable for any misuse with any APIs involved!**

## Usage
This script is split up into 2 different scripts, so we don't have to rescrape all of the mod links if the download fails.
First run `get_links.py`, this will get the links and store them in jars.csv, then run the `download_jars.py` to download the jars. Afterwards, you'll see a `mods` directory populated with different jar files.

If you wish to remove any XML files (created by url encoded issues on Modrinth leading to Access Denied.) you can run the follow bash command:
```
rm $(file mods/* | grep XML | cut -f1 -d":")
```
