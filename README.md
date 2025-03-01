# Widevine Ripper (WVRipper)

Widevine Ripper (WVRipper) is a command-line tool for downloading and processing media content from various streaming services.

## Features
- Supports multiple streaming services, including Netflix, Amazon, AppleTV, DisneyPlus, and more.
- Allows customization of video resolution, audio, subtitles, and file output.
- Supports multiple audio and subtitle languages.
- Provides various proxy and VPN options.
- Supports scheduling and preset saving for downloads.

## Installation

To use WVRipper, ensure you have Python installed and set up the necessary dependencies:

```bash
pip install -r requirements.txt
```

## Usage

### Basic Command

```bash
python wvripper.py --service <content_url_or_id> [options]
```

### Arguments

| Argument | Short | Description |
|----------|-------|-------------|
| `content` |  | Content URL or ID |
| `--service` |  | Select the service name (e.g., NETFLIX, AMAZON, DISNEYPLUS) |
| `--quality` | `-q` | Set video resolution (default: 1920) |
| `--output` | `-o` | Set download folder |
| `--folder` | `-f` | Set external folder for final .mkv file |
| `--nv` | `--no-video` | Skip downloading video |
| `--na` | `--no-audio` | Skip downloading audio |
| `--ns` | `--no-subs` | Skip downloading subtitles |
| `--episode` | `-e` | Set episode number(s) to download (default: `1~`) |
| `--season` | `-s` | Set season number to download |
| `--keep` |  | Keep temporary files after muxing |
| `--audio-language` | `-al` | Specify audio languages (comma-separated) |
| `--subtitle-language` | `-sl` | Specify subtitle languages (comma-separated) |
| `--prompt` | `-p` | Enable Yes/No prompt when grabbing URLs |
| `--license` | `--keys` | Perform a license key check and exit |
| `--select` |  | Select A/V/S manually when URL is grabbed |
| `--smart-select` |  | Select A/V/S automatically using an algorithm |
| `--audio-profile` | `-ap` | Configure audio codec (e.g., AAC, AC3, EAC3, ATMOS) |
| `--video-profile` | `-vp` | Configure video codec (e.g., AVC, HEVC, HDR, DOLBY_VISION) |
| `--cdn` |  | Configure AppleTV CDN (e.g., ap1, ap, ak) |
| `--no-aria2c` |  | Do not use `aria2c.exe` as main downloader |
| `--no-chapters` | `-nc` | Skip downloading chapters |
| `--asin` |  | Download from Amazon using ASIN |
| `--android` |  | Enable Android mode for Amazon |
| `--sd` |  | Download SD quality for Amazon (Linux users) |
| `--region` |  | Set Amazon region (e.g., uk, de, us, jp) |
| `--vpn` |  | Use VPN proxy (NordVPN, PrivateVPN, TorGuardVPN) |
| `--no-proxy` |  | Disable proxy when downloading |
| `--watcher` |  | Watcher for HBO Max |
| `--upload` | `-u` | Enable upload with packer |
| `--trackers` |  | Choose trackers (e.g., iptorrents, torrentday) |
| `--type` |  | Define content type (movie or episode) |
| `--desc` |  | Pass a description file |
| `--seed` |  | Seed torrent after upload |
| `--local-seed` |  | Seed locally created torrent |
| `--group` | `-gr` | Set group name |
| `--tag-style` | `-ts` | Set naming tag style |
| `--mkvmerge-extras` | `-mkve` | Add extra commands for `mkvmerge.exe` |
| `--mkvmerge-defaults` | `-mkvd` | Set default A/V/S tracks for .mkv |
| `--no-mux` |  | Skip muxing |
| `--schedule` |  | Schedule downloads |
| `--enable-file-assister` |  | Enable file assisting for downloads |
| `--save-preset` |  | Save custom arguments for later use |
| `--load-preset` |  | Load saved custom arguments |
| `--thread` |  | Enable thread downloading |
| `--credit` |  | Download Disney+ content with credits |
| `--shaka-decrypt` |  | Decrypt AppleTV 4K content (video only) |
| `--rental` |  | Set iTunes rental ID |

### Example Commands

Download a 1080p video from Netflix with English audio and subtitles:
```bash
python wvripper.py <content_id> --service NETFLIX --quality 1080 --audio-language en --subtitle-language en
```

Download a full season from Amazon with a specific ASIN:
```bash
python wvripper.py --service AMAZON --asin B08XYZ123 --season 1
```

Use NordVPN with a specific host while downloading:
```bash
python wvripper.py <content_id> --nordvpn-host localhost:8081
```

## Contributing
Feel free to open issues or submit pull requests for improvements.

## License
This project is licensed under an appropriate license based on its intended use.

