# munin-teamspeak3-plugin

## Features

* Log your TeamSpeak3 server's ...
  * current users count
  * current Away users + AFKed channel users count (AFK channel must be a single, and contains "afk" in channel name)

## Installation

1. Download "teamspeak" file.
2. Put "teamspeak" file into your Munin's plugin directory. (ex. `cp teamspeak /usr/lib/munin/plugins/`)
3. Write your config (To see details below)
4. Create the symlink to complete installation of this plugin (ex. `ln -s /usr/lib/munin/plugins/teamspeak /etc/munin/plugins/teamspeak`)
5. Reload your munin-node to activate this plugin.

## Config

Edit or create the config file with any name under `/etc/munin/plugin-conf.d` for munin-node, and add config like below:

```ini
...

[teamspeak*]
env.TEAMSPEAK3_HOST 127.0.0.1
env.TEAMSPEAK3_PORT 9987
env.TEAMSPEAK3_QUERY_PORT 10011
env.TEAMSPEAK3_QUERY_ID serveradmin
env.TEAMSPEAK3_QUERY_PASSWORD XXXXXXXX

...
```

## LICENSE
The MIT License (MIT)
Copyright (c) 2016 k5342

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the "Software"), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.