# Service Status Monitor

A simple, lightweight service status monitor that displays real-time uptime and availability of major internet services. Similar to Downdetector, but much simpler.

## Features

- Real-time status monitoring of 10 major internet services
- Clean, modern dark-themed UI
- Summary dashboard showing operational/issues/outage counts
- Auto-refresh every 60 seconds
- Manual refresh button
- Responsive design for mobile devices
- No backend required - runs entirely in the browser

## Monitored Services

| Service | Status Page |
|---------|-------------|
| GitHub | githubstatus.com |
| Cloudflare | cloudflarestatus.com |
| Discord | discordstatus.com |
| Reddit | redditstatus.com |
| Dropbox | status.dropbox.com |
| Twilio | status.twilio.com |
| Datadog | status.datadoghq.com |
| Bitbucket | bitbucket.status.atlassian.com |
| npm | status.npmjs.org |
| Vercel | vercel-status.com |

## Usage

Simply open `index.html` in any modern web browser:

```bash
# Open directly in browser
open index.html

# Or serve with a simple HTTP server
python3 -m http.server 8000
# Then visit http://localhost:8000
```

## How It Works

The app fetches status information from public Statuspage.io APIs that many major services use. These APIs return JSON data with status indicators:

- **Operational** (green): All systems working normally
- **Degraded** (yellow): Minor issues or degraded performance
- **Major Outage** (red): Significant service disruption
- **Unknown** (gray): Unable to fetch status

## Technical Details

- Single HTML file with embedded CSS and JavaScript
- No dependencies or build process required
- Uses native `fetch()` API for HTTP requests
- CORS-enabled status endpoints
- Responsive CSS Grid/Flexbox layout

## Browser Support

Works in all modern browsers:
- Chrome, Firefox, Safari, Edge (latest versions)

## License

MIT