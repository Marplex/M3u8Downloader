<h1 align="center">M3u8 Downloader</h1><br>
<p align="center">
🎥️ A simple python command-line utility which downloads m3u8 playlists in a single file.<br>
This is a forked repo and adds support to AES segment decryption
</p>
<br>


## Install


```bash
git clone https://github.com/Marplex/M3u8Downloader.git
cd ./M3u8Downloader
python3 setup.py install
```

## Usage

Download m3u8 playlist to single file output (file:// protocol is also supported)

```bash
m3u8-dl HLS_URL OUTPUT.ts
```

Download with custom headers.
-u specify the base url when `#EXTINF hls-720p0.ts` has no base url
-r specify referer

```bash
m3u8-dl HLS_URL OUTPUT.ts -u https://example.com/ -r https://example.com
```

Restore last session if the task was interrupted

```bash
m3u8-dl --restore
```

Specify how many segments should be downloaded in parallel

```bash
m3u8-dl -t 10
```

For more details

```bash
m3u8-dl --help
```