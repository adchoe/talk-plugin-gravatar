# talk-plugin-gravatar

A simple Talk plugin to display Talk users' Gravatar avatars with as much
privacy as possible. The plugin acts as a proxy to gravatar and never directly
reveal the md5sum of a talk user's email. This avoids two key privacy concerns
normally faced when using gravatar:

1. Leaking emails to any visitor via md5sums in Gravatar URLs
2. Visitors' referer header passed to Gravatar leaking specific pages being visited

## Installation

Add the plugin to the `plugins.default.json` file or create a `plugins.json`
file and add it there. See the [Coral Talk plugin docs](https://docs.coralproject.net/talk/plugins/)
for details about adding plugins.


Example `plugins.json` file:

```json
{
  "server": [
    {"talk-plugin-gravatar": "^0.1.3"}
  ],
  "client": [
    {"talk-plugin-gravatar": "^0.1.3"}
  ]
}
```

Then run `./bin/cli plugins reconcile` for source installs or an appropriate
command for your talk installation to make the plugin available.

## Demonstration

<div id="coral_talk_stream"></div>
<script src="https://talk.snorre.io/static/embed.js" async onload="
  Coral.Talk.render(document.getElementById('coral_talk_stream'), {
    talk: 'https://talk.snorre.io/'
  });
"></script>
