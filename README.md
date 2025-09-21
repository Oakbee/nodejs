# Telegram Video Duplicate Remover Bot

A Telegram bot that processes videos to avoid duplicate content detection on social media platforms. Perfect for content creators who want to repost their own videos without being flagged by duplicate detection algorithms.

## Features

- 🎥 **Multi-format Support**: Handles MP4, MOV, AVI, MKV, WebM
- 🎨 **Smart Processing**: Applies multiple anti-duplicate techniques
- 🔧 **Automatic Processing**: Just send a video and get results
- 📱 **Telegram Integration**: Works directly in Telegram chats
- 🚀 **Fast Processing**: Efficient video processing pipeline

## Anti-Duplicate Techniques

The bot applies various techniques to make videos appear as new content:

### Visual Modifications
- **Subtle Cropping**: Removes 2-5% from edges randomly
- **Scale Adjustments**: Minor scaling changes (98-102%)
- **Color Grading**: Slight brightness, contrast, and saturation adjustments
- **Noise Addition**: Very subtle noise overlay
- **Sharpening/Blur**: Minor unsharp mask application

### Technical Modifications  
- **Metadata Removal**: Strips all original metadata
- **Quality Changes**: Slight CRF adjustments (22-24)
- **Frame Rate**: Minor FPS modifications
- **Compression**: Different encoding parameters
- **Border Addition**: Thin padding when beneficial

### Random Elements
- Processing parameters are randomized for each video
- Multiple processing paths available
- Ensures each output is unique

## Installation

1. Clone the repository:
   ```bash
   git clone <repository-url>
   cd telegram-video-bot
   ```

2. Install dependencies:
   ```bash
   npm install
   ```

3. Update the bot token in `src/bot.js` or set environment variables

4. Start the bot:
   ```bash
   npm start
   ```

## Usage

1. **Start the Bot**: Send `/start` to get welcome message
2. **Send Video**: Upload any video file to the bot
3. **Wait for Processing**: Bot will show progress updates
4. **Receive Result**: Get your processed video ready for reposting

### Commands
- `/start` - Welcome message and bot info
- `/help` - Usage instructions and features

## Supported Formats

- **Input**: MP4, MOV, AVI, MKV, WebM, Video Notes
- **Output**: MP4 (optimized for social media)

## Technical Details

- **Video Processing**: FFmpeg.wasm for browser-compatible processing
- **Telegram API**: Official Bot API integration
- **File Handling**: Temporary file management with cleanup
- **Error Handling**: Comprehensive error handling and user feedback

## Environment Variables

```bash
TELEGRAM_BOT_TOKEN=your_bot_token_here
DEBUG=false
MAX_FILE_SIZE=50MB
SUPPORTED_FORMATS=mp4,mov,avi,mkv,webm
```

## File Structure

```
src/
├── bot.js              # Main bot logic
├── videoProcessor.js   # Video processing engine
└── utils/
    ├── download.js     # File download utilities
    └── logger.js       # Logging system
```

## Contributing

1. Fork the repository
2. Create a feature branch
3. Make your changes
4. Submit a pull request

## License

MIT License - See LICENSE file for details

## Disclaimer

This bot is designed for legitimate use cases where content creators want to repost their own content. Users are responsible for complying with platform terms of service and copyright laws.