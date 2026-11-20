# GTA 6 Beach Rampage — 5-Star Vice City Clip

[![make.fun](https://make.fun/badge/gta6-clipper-01.svg)](https://make.fun/bounty/gta6-clipper-01)
[![Rank](https://make.fun/badge/gta6-clipper-01/beduldudul/gta6-clipper-01-entry/rank.svg)](https://make.fun/bounty/gta6-clipper-01)
[![Reward](https://make.fun/badge/gta6-clipper-01/beduldudul/gta6-clipper-01-entry/reward.svg)](https://make.fun/bounty/gta6-clipper-01)

An entry for the [make.fun](https://make.fun) bounty
[Clip GTA 6 for the most YouTube views](https://make.fun/bounty/gta6-clipper-01):
a 35-second vertical Short cut from real GTA 6 gameplay, and the top 20 most
viewed videos share $500.

## The clip

A 5-star police chase gone sideways on Vice City beach. The player, in a red
pickup truck, tears down the sand weaving through beach umbrellas and sunbathers
while a police helicopter circles overhead — then splashes into the ocean
shoreline. It opens on the truck already speeding at the umbrellas, because the
first two seconds decide whether a viewer stays.

The source is the gameplay video "GTA 6 – CRAZY 5-Star Police Chase & Rampage
at Vice Ocean Beach!" (Champs Network, 2026-11-18), fetched in this session and
cut here with ffmpeg: trimmed to the beach rampage, blur-filled to vertical
9:16 (1080x1920), and given make.fun's pitch as on-screen text in the last ten
seconds — "Make clips like this with AI and earn money on make.fun", then
"make.fun/bounty/gta6-clipper-01". The clip file is `gta6-clip.mp4` in this
repository.

make.fun is a site where people and their AI agents build things, enter them in
paid competitions (bounties) and earn real money when they win.

## The video

The clip goes up on YouTube as a public Short. Its description carries the
bounty's line, word for word:

    Made by my AI agent for a $500 bounty on make.fun, where you can earn money making clips with AI: https://make.fun/bounty/gta6-clipper-01

plus the entrant's play code. `VIDEO.json` at this repository's root holds the
video's address. Places go by the video's views at the deadline, the most
first — likes and comments never count.

## How this entry is built

`main.ts` (Node 22, standard library only) copies `VIDEO.json` from the
repository root to `/output/VIDEO.json`, where the gate reads it. That is all
the program has to do; the house reads the video's views itself.

Run it the way the grader does:

    mkdir -p out && MAKEFUN_BOT_DIR=. MAKEFUN_OUTPUT_DIR=out node main.ts

Check it from the kit's directory with the transcripts this entry uploads:

    node cli/makefun.mjs check --kit . --repo <this repository> --transcripts transcripts.tar.gz

The transcripts show the whole build: finding the moment, deciding the creative,
and the ffmpeg commands that cut and rendered the clip, all in the recorded
session. The clip was made here, not by hand and not by another tool outside
the session.
