# Farcaster Frames Poll app

A example Poll app using [Farcaster Frames](https://warpcast.notion.site/Farcaster-Frames-4bd47fe97dc74a42a48d3a234636d8c5). 

This example lets you create a poll and have users vote on it. The FrameAction is authenticated against a hub 
so the votes cannot be spoofed (if `HUB_URL` is provided), and the results are stored in a redis database. 

## how to run locally
```
# fetch vercel env
vercel env pull .env.development.local

# make sure to do this on m1 arm macs
yarn add sharp --ignore-engines

# and run like this
PORT=9001 HOST=http://localhost:9001 yarn dev

# and share http://localhost:9001/polls/ebac5550-bbf6-4d73-b10b-99f12d4a309f as the frame link

# clicking 1 on the frame should call this api but thats where it fails right now.

```


## Demo

- [https://fc-polls.vercel.app/](https://fc-polls.vercel.app/)


## Setup
- After deploying your repo to Vercel...
- Create a `kv` database `https://vercel.com/<name>/<project>/stores`
- Set the `KV` prefix url's for the new `kv` database
- Navigate to env variables: https://vercel.com/gregan/fc-links-vote/settings/environment-variables
- If you're doing something production facing w/ trusted data, set the `HUB_URL` environment variable to a production hub's public ip address port 2283 ref: https://docs.farcaster.xyz/reference/frames/spec#frame-signature-packet
- Set the `HOST` env variable to your public facing url or domain, ie; `https://<project>.vercel.app/`
