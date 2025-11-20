---
layout: post
title:  "Experiments in AI-assisted code generation"
date:   2025-11-20 11:36:30 +0300
categories: web site
---

# Rebuilding C64 Classics With AI

## Experiment 
Lately I've been experimenting with using AI tools to help rebuild classic Commodore 64 games in modern web technologies. As a small personal challenge, and with a bit of nostalgia, I tried to create new React versions of two old favorites of mine. 

One of them was "Archon" that mixes chess and arena combat. The other was "Herrat ja Narrit", which is a simple but suprisingly hooking Finnish game some might remember. 


## AI is surprisingly good, but not plug-and-play
AI (Claude 4.5 with MS Code and GitHub) was able to:
- Generate React components and game loops
- Suggest state management implementations
- Outline architecture for rendering boards, sprites, and interactions
- Translate gameplay descriptions into working logic

However, neither game worked out of the box. The issues had to do mostly with storing the states and I had to walk the AI through corrections step by step. What was suprising was Claude's ability to insert debug logs in the code, ask me to run the program, copy-paste the logs to it and then it was able to figure out what was going on. These are definitely getting better year by year. 

## But AI is not a replacement for skill 

Working with AI feeels like pairing with an enthusiastic but inexperienced junior developer: fast, helpful and creative, but not someone you can trust with a full project on their own. If you can already build things, AI accelerates the process. If you can't build things yet, AI gives you an illusion that you're closer than you actually are.

## Where are the games? 

I might actually try to improve and alter those before putting those available anywhere, because copyrights. At this time this was just and experiment plus I wanted to create another quick blog page to see how to work with GitHub pages. 

