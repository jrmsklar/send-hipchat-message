Send HipChat Messages via Ruby Script
====================

Use this repository if you wish to send HipChat messages to any given room via a Ruby script.

Description
---

This is used to send the "Get Up!" notifications every 15 minutes. We use this to remind us to stand up, stretch out, and maybe walk around, every 15 minutes throughout the work day.

Usage
---

This uses [Ruby Gems](https://rubygems.org/), along with [Bundler](http://bundler.io/) for dependency management. See the websites for isntallation instructions.

You must create your own `.env` file and store it in the root of this repository in order for the script(s) to work as expected. The script(s) use [dotenv](https://github.com/bkeepers/dotenv) to load the environment variables. The `.env` file is *not*, and should not be in source control.

The format for the `.env` file should be as follows:

Use the script `send_message_to_room.rb` to send a message to any room. This script requires 2 command line arugments:

- 1st argument is the room XXMP JID (which can be found on the HipChat web client)
- 2nd argument is the message text

Example:

```bash
ruby send_message_to_room.rb 12345_roomname@conf.hipchat.com "Get up and stretch."
```