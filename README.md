# Today I learned

---

### Categories

- [Javascript](#javascript)
- [Mac](#mac)
- [Server](#server)

---

### Javascript

#### Merge/extend properties of two objects

Similar to jQuery or Underscore extend, but you can do it with pure Javascript.

```
function extend(a, b) {
	for( var key in b ) { 
		if( b.hasOwnProperty( key ) ) {
			a[key] = b[key];
		}
	}
	return a;
}
```
Then you use it like this:

```
var defaults = {validate: false, limit: 5};
var options = {validate: true};

// we extend empty objects so that we do not mutate the defaults object.
var settings = extend({}, defaults);

// If we just want to extend the settings object, we don't need to store into a new variable
extend(settings, options);

// or you can just extend defaults and options directly and save it to settings var.
var settings = extend(defaults, options)
```

Thanks to [Codrops](http://tympanus.net/codrops/) tutorials for this.

---

### Mac

#### Keyboard Shortcut to Open Emoji Insert

On any text editor, press `Ctrl + ⌘ + space` to open up Emoji & Special Characters window.

---

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
