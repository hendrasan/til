# Today I learned

---

### Categories

- [Mac](#mac)
- [Server](#server)

---

### Mac

#### Keyboard Shortcut to Open Emoji Insert

On any text editor, press `Ctrl + ⌘ + space` to open up Emoji & Special Characters window.

### Server

#### Crontab special keywords

Usually when you create a cronjob, you input something like this:

`0 * * * * /command/to/execute`

Apparently, there are some special keywords you can use as shortcuts. They are:

- @reboot        Run once, at startup.
- @yearly        Run once a year, equivalent to `0 0 1 1 *`.
- @annually      (same as @yearly)
- @monthly       Run once a month, equivalent to `0 0 1 * *`.
- @weekly        Run once a week, equivalent to `0 0 * * 0`.
- @daily         Run once a day, equivalent to `0 0 * * *`.
- @midnight      (same as @daily)
- @hourly        Run once an hour, equivalent to `0 * * * *`.

So you can just type `@daily /command/to/execute` instead of `0 0 * * * /command/to/execute`

---

# About

This is a collection of stuffs I just learned or came across on the internet
that I think are useful.

[thoughtbot](https://github.com/thoughtbot/til) started this long ago, so credits to them.
