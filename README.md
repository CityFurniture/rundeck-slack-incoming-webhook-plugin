rundeck-slack-incoming-webhook-plugin
======================

Sends rundeck notification messages to a slack channel.  This plugin  is based on [rundeck-slack-plugin](https://github.com/bitplaces/rundeck-slack-plugin)(based on run-hipchat-plugin).

Installation Instructions
-------------------------

See the [Included Plugins | Rundeck Documentation](http://rundeck.org/docs/plugins-user-guide/installing.html#included-plugins "Included Plugins") for more information on installing rundeck plugins.

## Download jarfile

1. Download jarfile from [releases](https://github.com/higanworks/rundeck-slack-incoming-webhook-plugin/releases).
2. copy jarfile to `$RDECK_BASE/libext`

## Build

1. build the source by gradle.
2. copy jarfile to `$RDECK_BASE/libext`

## Configuration

This plugin uses Slack incoming-webhooks. Create a new webhook and copy the provided url.

The only required configuration settings are:

- `WebHook URL`: Slack incoming-webhook URL. Can be set at either the project level
   by editing the project properties file, or can be overridden at the notification level

- `Custom template`: Can be used to apply a custom template to a specific notification.
   The template will be loaded from `/etc/rundeck`
   
### Custom notification templates

In case you need to customize the notifications, it's possible to do so by copying the
default templates from `src/resources/templates` to `/etc/rundeck` on the rundeck server.

The plugin will first try to read the template from `/etc/rundeck` first and, if not found, from itself.

## Slack message example.

On success.

![on success](on_success.png)

On failure.

![on failure](on_failure.png)

## Contributors
*  Original [hbakkum/rundeck-hipchat-plugin](https://github.com/hbakkum/rundeck-hipchat-plugin) author: Hayden Bakkum @hbakkum
*  Original [bitplaces/rundeck-slack-plugin](https://github.com/bitplaces/rundeck-slack-plugin) authors
    *  @totallyunknown
    *  @notandy
    *  @lusis
*  @sawanoboly