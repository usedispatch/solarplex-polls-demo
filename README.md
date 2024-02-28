# Solarplex Frames Poll app

A example Poll app using [Solarplex Frames](https://docs.solarplex.xyz/solarplex-frames). 

This example lets you create a poll and have users vote on it. The results are stored in a redis database. This is a fork of the Farcaster polls demo app.

## how to run locally
```
# fetch vercel env
vercel env pull .env.development.local

# make sure to do this on m1 arm macs
yarn add sharp --ignore-engines

# and run like this
PORT=9001 HOST=http://localhost:9001 yarn dev

# and share http://localhost:9001/polls/ebac5550-bbf6-4d73-b10b-99f12d4a309f as the frame link on solarplex.

```


## Demo

- [https://solarplex-polls-demo.vercel.app/](https://solarplex-polls-demo.vercel.app/)


## Setup
- After deploying your repo to Vercel...
- Create a `kv` database `https://vercel.com/<name>/<project>/stores`
- Set the `KV` prefix url's for the new `kv` database
- Navigate to env variables: https://vercel.com/gregan/fc-links-vote/settings/environment-variables
- Set the `HOST` env variable to your public facing url or domain, ie; `https://<project>.vercel.app/`
