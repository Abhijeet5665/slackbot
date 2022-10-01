# slackbot
slackbot code with socketmode

### Running a Socket Mode app  
If you use Socket Mode for running your app, SocketModeHandler is available for it.

import os
from slack_bolt import App
from slack_bolt.adapter.socket_mode import SocketModeHandler

# Install the Slack app and get xoxb- token in advance
app = App(token=os.environ["SLACK_BOT_TOKEN"])

# Add functionality here

if __name__ == "__main__":
    # Create an app-level token with connections:write scope
    handler = SocketModeHandler(app, os.environ["SLACK_APP_TOKEN"])
    handler.start()
Run the app this way:

export SLACK_APP_TOKEN=xapp-***
export SLACK_BOT_TOKEN=xoxb-***
python app.py

# SLACK_SIGNING_SECRET is not required
# Running ngrok is not required
