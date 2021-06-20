# rapgod.me

## Set Up

1. Clone repository
1. Run `npm install`
1. Copy and rename `.env.example` to `.env`
1. Run `npm run postinstall` (optional)
1. Run `npm run dev` (development mode) or `npm start` (production mode)
1. Open the page in your browser (https://localhost:3000). It will list all the active polls.
1. Type in the username and password found in `.env`

## Available Routes

- http://localhost:3000/create to create a new poll
- http://localhost:3000/newest to show the results of the newest poll
- http://localhost:3000/vote/{poll_id} to vote in a poll
- http://localhost:3000/poll/{poll_id} to show the results of a poll
- http://localhost:3000/qrcode to show a qrcode with the url to newest poll

## Additional URL-Parameters

- monotone=boolean
  - applies a reduced color scheme for voting bars
  - ignored if _overlay=true_ is used
- simple=boolean
  - applies a basic font type
- overlay=boolean
  - overwrites _monotone_ parameter
  - applies a compact view especially for live streams / OBS

Example usage

```
/poll/{poll_id}?monotone=true&simple=true&overlay=true
```