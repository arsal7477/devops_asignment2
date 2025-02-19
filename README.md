# Automating Collaborative Development Workflow Using Bash Scripting

## Introduction
This Bash script automates Git commits, pushes changes, and notifies collaborators via email.

## Prerequisites
- Git installed (`git --version`)
- cURL installed (`curl --version`)
- SendGrid API Key (from [SendGrid](https://sendgrid.com/))
- jq installed (`jq --version`)
- inotify-tools installed (`inotifywait --help`)

## Installation
1. Clone this repository:
   ```bash
   git clone https://github.com/yourusername/auto-dev-workflow.git
   cd auto-dev-workflow

2. Configure the config.cfg file with:
- Repository path
- File/directory to monitor
- Git remote & branch
- SendGrid API key & sender email
- List of collaborators' emails


3. Make the script executable:
 ```bash
  chmod +x monitor_and_push.sh
```

4. Run the script:
   ```
   ./monitor_and_push.sh &
## How It Works

- Monitors a specified directory for changes.
- Uses SHA-256 checksum to detect modifications.
- Auto-commits and pushes changes to GitHub.
- Sends an email notification via SendGrid.

## Error Handling

- Handles Git push failures.
- Validates SendGrid API response.

## Example Usage

To test:
```
echo "New update" >> /path/to/monitor/sample.txt
```

## Troubleshooting

- Ensure correct file paths in config.cfg.
- Check Git remote & branch settings.
- Validate SendGrid API key.


### Name: Arsalan Khan
### Regno: 2022115
### Development Operations Assignment: 2

# End...
