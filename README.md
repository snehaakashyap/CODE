
> **Before submitting feature requests or expecting personalized support, please understand this project exists purely as a community resource.** If you value what's been created, the best way to show appreciation is by contributing code, documentation, or helping other users.

> ## 🔑 API KEY INFORMATION - UPDATED
>
> We have tested and confirmed that **both Gemini and OpenAI APIs work properly** with the current version. If you are experiencing issues with your API keys:
>
> - Try deleting your API key entry from the config file located in your user data directory
> - Log out and log back in to the application
> - Check your API key dashboard to verify the key is active and has sufficient credits
> - Ensure you're using the correct API key format (OpenAI keys start with "sk-")
>
> The configuration file is stored at: `C:\Users\[USERNAME]\AppData\Roaming\interview-coder-v1\config.json` (on Windows) or `/Users/[USERNAME]/Library/Application Support/interview-coder-v1/config.json` (on macOS)




- Toggle Window Visibility: [Control or Cmd + B]
- Move Window: [Control or Cmd + Arrow keys]
- Take Screenshot: [Control or Cmd + H]
- Delete Last Screenshot: [Control or Cmd + L]
- Process Screenshots: [Control or Cmd + Enter]
- Start New Problem: [Control or Cmd + R]
- Quit: [Control or Cmd + Q]
- Decrease Opacity: [Control or Cmd + []
- Increase Opacity: [Control or Cmd + ]]
- Zoom Out: [Control or Cmd + -]
- Reset Zoom: [Control or Cmd + 0]
- Zoom In: [Control or Cmd + =]



## Prerequisites

- Node.js (v16 or higher)
- npm or bun package manager
- OpenAI API Key
- Screen Recording Permission for Terminal/IDE
  - On macOS:
    1. Go to System Preferences > Security & Privacy > Privacy > Screen Recording
    2. Ensure that CodeInterviewAssist has screen recording permission enabled
    3. Restart CodeInterviewAssist after enabling permissions
  - On Windows:
    - No additional permissions needed
  - On Linux:
    - May require `xhost` access depending on your distribution

## Running the Application

### Quick Start

1. Clone the repository:

```bash
git clone https://github.com/greeneu/interview-coder-withoupaywall-opensource.git
cd interview-coder-withoupaywall-opensource
```

2. Install dependencies:

```bash
npm install
```

3. **RECOMMENDED**: Clean any previous builds:

```bash
npm run clean
```

4. Run the appropriate script for your platform:

**For Windows:**
```bash
stealth-run.bat
```

**For macOS/Linux:**
```bash
# Make the script executable first
chmod +x stealth-run.sh
./stealth-run.sh
```


To create installable packages for distribution:

**For macOS (DMG):**
```bash
# Using npm
npm run package-mac

# Or using yarn
yarn package-mac
```

**For Windows (Installer):**
```bash
# Using npm
npm run package-win

# Or using yarn
yarn package-win
```

The packaged applications will be available in the `release` directory.

**What the scripts do:**
- Create necessary directories for the application
- Clean previous builds to ensure a fresh start
- Build the application in production mode
- Launch the application in invisible mode

### Notes & Troubleshooting

- **Window Manager Compatibility**: Some window management tools (like Rectangle Pro on macOS) may interfere with the app's window movement. Consider disabling them temporarily.

- **API Usage**: Be mindful of your OpenAI API key's rate limits and credit usage. Vision API calls are more expensive than text-only calls.

- **LLM Customization**: You can easily customize the app to include LLMs like Claude, Deepseek, or Grok by modifying the API calls in `ProcessingHelper.ts` and related UI components.

- **Common Issues**:
  - Run `npm run clean` before starting the app for a fresh build
  - Use Ctrl+B/Cmd+B multiple times if the window doesn't appear
  - Adjust window opacity with Ctrl+[/]/Cmd+[/] if needed
  - For macOS: ensure script has execute permissions (`chmod +x stealth-run.sh`)


