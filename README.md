# QuickFill

![QuickFill demo](quickfill-demo.gif)

A small, free Chrome extension that keeps the things you keep retyping one click away: your address, phone number, class schedule, todos and notes.

## Features

- **Details**: store your name, email, phone, address and any custom fields. Click a row to copy it, or press **Insert** to fill the form field you selected on the page.
- **Email**: add your Gmail accounts once (by email address or account number like `/u/5/`) and open any inbox in one click, no more profile picker and account switching.
- **Schedule**: upload a picture of your weekly class timetable and view it any time, including full size in a new tab.
- **Todo**: a simple checklist. Add tasks, tick them off, clear the finished ones.
- **Notes**: a plain text pad with a Save button. It also auto-saves, so nothing is lost if the popup closes.
- **Settings** (the small gear, top right): choose your accent colour (presets or any hex code) and Auto, Light or Dark mode.

## How to use

1. Open QuickFill and go to **Details**. Click **Edit**, fill in your information, and press **Save**.
2. To copy a value, click its row.
3. To fill a form, click the field on the web page first, open QuickFill, then press **Insert** next to the value. If no field is selected, QuickFill copies the value instead.

## Privacy

Everything is stored locally in your browser using `chrome.storage.local`. The Email tab only opens `mail.google.com` links in a new tab. It never reads your Gmail or your Google login. QuickFill makes no network requests, has no analytics, no accounts and no server. Your data never leaves your computer.

## Security: please read

QuickFill is built for everyday details like addresses, phone numbers and student IDs. **Do not store passwords, card numbers, bank details, or national ID or passport numbers in it.**

- Data is stored as **plain text** in your Chrome profile. It is not encrypted, so anyone with access to your computer or profile (or malware running on it) could read it.
- A website can read anything that gets inserted into one of its form fields. Only use Insert on sites you trust.
- Values you copy go to your system clipboard, which clipboard managers and other apps may be able to see.
- Install QuickFill only from this repository or an official release. Unofficial copies could contain changed code.

The extension loads no remote code and uses no third-party libraries. If you find a security problem, please open an issue or contact the maintainer.

## Permissions

| Permission | Why it is needed |
| --- | --- |
| `storage`, `unlimitedStorage` | Save your details, schedule image, todos and notes locally |
| `activeTab`, `scripting` | Insert a value into the form field you selected, only when you press Insert |

## Project structure

```
manifest.json        extension config (Manifest V3)
popup.html/css/js    the popup interface and logic
viewer.html/js       full-size schedule viewer
icons/               extension icons
quickfill-demo.gif   demo shown above
```

## Contributing

Issues and pull requests are welcome. Ideas for improvement:

- Backup and restore of your data (export and import)
- Optional passcode lock with encryption
- Multiple profiles (for example personal and work)
- Keyboard shortcuts for favourite fields
- Firefox support

To work on it, load the folder as an unpacked extension (see Install), edit the files, and press the reload button on `chrome://extensions`.

## License

[MIT](LICENSE)


buymeacoffee.com/usmans.pk