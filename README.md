# Calendar Link Generator

A free, open-source alternative to AddEvent for generating calendar invitation links in email marketing campaigns.

## Problem Solved

Many businesses use services like [AddEvent](https://www.addevent.com/) to add "Add to Calendar" buttons in their marketing emails. These services charge monthly fees for a relatively simple feature.

**This tool solves that problem by:**
- Generating calendar links for Google Calendar, Office 365, and Outlook.com
- Providing ready-to-use HTML code for email templates (Mailchimp, etc.)
- Working completely offline with no dependencies
- Being 100% free and open source

## Features

| Feature | Description |
|---------|-------------|
| Multi-platform support | Google Calendar, Office 365, Outlook.com |
| Timezone support | Australia (Sydney, Melbourne, Brisbane, Perth), China, Hong Kong, Singapore |
| One-click copy | Copy generated HTML code to clipboard instantly |
| Live preview | See how the calendar icons will look before using |
| No installation | Just open the HTML file in any browser |
| Offline capable | Works without internet connection |
| Mailchimp compatible | Generated HTML works perfectly in Mailchimp email templates |

## How to Use

### Step 1: Open the Tool
Double-click `calendar-link-generator.html` to open it in your browser.

### Step 2: Fill in Event Details
- **Event Title**: The name of your event
- **Date**: Event date
- **Start/End Time**: Event duration
- **Timezone**: Select appropriate timezone
- **Location**: (Optional) Event venue or "Online"
- **Description**: Event details, agenda, etc.

### Step 3: Generate & Copy
1. Click **"Generate HTML Code"**
2. Preview the result at the bottom
3. Click **"Copy to Clipboard"**

### Step 4: Use in Mailchimp
1. In Mailchimp email editor, add a **"Code"** content block
2. Paste the copied HTML code
3. Done!

## Screenshot

The tool generates calendar icons that look like this in emails:

```
        Add event to calendar

    [Google] [Office 365] [Outlook]
```

When recipients click an icon, they are taken directly to their calendar with event details pre-filled.

## Supported Calendar Platforms

| Platform | Icon | Link Format |
|----------|------|-------------|
| Google Calendar | ![Google](https://cdn.addevent.com/libs/imgs/icon-emd-share-google-t1.png) | `calendar.google.com/calendar/render?action=TEMPLATE&...` |
| Office 365 | ![Office365](https://cdn.addevent.com/libs/imgs/icon-emd-share-office365-t1.png) | `outlook.office.com/calendar/action/compose?rru=addevent&...` |
| Outlook.com | ![Outlook](https://cdn.addevent.com/libs/imgs/icon-emd-share-outlook-t1.png) | `outlook.live.com/calendar/action/compose?rru=addevent&...` |

## Technical Details

### Calendar Link Formats

**Google Calendar:**
```
https://calendar.google.com/calendar/render?action=TEMPLATE
&text={title}
&dates={YYYYMMDDTHHmmss}/{YYYYMMDDTHHmmss}
&details={description}
&location={location}
&ctz={timezone}
```

**Outlook (Office 365 & Outlook.com):**
```
https://outlook.office.com/calendar/action/compose?rru=addevent
&subject={title}
&startdt={ISO8601 datetime with timezone}
&enddt={ISO8601 datetime with timezone}
&body={description}
&location={location}
```

### Why Not Apple Calendar / Yahoo?

- **Apple Calendar**: Requires hosting an `.ics` file on a server. Can be added if you have web hosting.
- **Yahoo Calendar**: Lower usage in business contexts. Can be added if needed.

## Use Cases

- Event registration confirmation emails
- Webinar invitation emails
- Meeting reminder emails
- Workshop/training announcement emails
- Any email where you want recipients to easily add an event to their calendar

## License

MIT License - Free to use, modify, and distribute.

## Contributing

Feel free to submit issues and pull requests for:
- Additional calendar platform support
- More timezone options
- UI/UX improvements
- Bug fixes

## Credits

Calendar icons provided by [AddEvent CDN](https://www.addevent.com/) (publicly available assets).
