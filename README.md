# QBittorrent - The Pirate Bay Search Plugins

A collection of QBittorrent search engine plugins for The Pirate Bay, utilizing the ApiBay.org API.

## Plugins

### Main Search Plugin
- **thepiratebay.py** - General search plugin for The Pirate Bay

### Top 100 Plugins
- **thepiratebay_top100hdmovies.py** - Top 100 HD Movies
- **thepiratebay_top100hdtv.py** - Top 100 HD TV Shows
- **thepiratebay_top1004kmovies.py** - Top 100 4K Movies
- **thepiratebay_top1004ktv.py** - Top 100 4K TV Shows

## Features

### Published Date
All plugins now populate the `pub_date` field with the torrent's upload timestamp, allowing you to see when each torrent was added to The Pirate Bay.

### Uploader Status Badges
Torrents are now marked with color-coded badges to indicate uploader status:
- 🟢 **VIP Uploaders** - Verified VIP members
- 🟣 **Trusted Uploaders** - Trusted community members

These badges help you quickly identify 'reliable' sources.

## Why Separate Top 100 Plugins?

The Top 100 plugins are implemented as **separate plugins** rather than categories within a single plugin for the following reasons:

### 1. QBittorrent Category System Limitations
QBittorrent's `supported_categories` parameter is designed for **filtering search results** by content type (Movies, TV, Music, etc.). When a user searches with a category selected, the plugin filters the API results accordingly.

### 2. Top 100 Lists Are Not Search-Based
The Top 100 lists work fundamentally differently:
- They fetch from **fixed API endpoints** (`data_top100_207.json`, `data_top100_208.json`, etc.)
- They return **predetermined lists** that don't depend on search queries
- They **ignore the search term** entirely - you always get the same Top 100 list

## API Source

All plugins use the [ApiBay.org](https://apibay.org/) API, which provides:
- Search functionality
- Precompiled Top 100 lists by category
- Torrent metadata (size, seeders, leechers, upload date, uploader status)

## Acknowledgement

Thanks to [@LightDestory](https://github.com/LightDestory) for the original TPB plugin that [thepiratebay.py](thepiratebay.py) is based on.