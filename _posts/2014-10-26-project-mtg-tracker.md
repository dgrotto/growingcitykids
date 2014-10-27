---
layout: post
author: David
title: "Project: MTG Tracker"
tags: projects
---
## The idea
Yesterday we started on a new project - MTG Tracker. My son is a *huge* fan of [Magic the Gathering][mtg]. What I love about MTG is that he has to be engaged in meatspace to play it. Too many of the games he is interested in right now are video-only.

What I dislike about MTG is the investment in learning and memorizing every detail of every card available. Don't get me wrong - this aspect of the game is extremely appealing to an 11 year old. I think that my brain is old and leaky enough now that rote memorization is not an interesting prospect.

I saw this as an opportunity to introduce my son to ways that technology can be used to solve these types of problems. I started the conversation by asking him if it would be interesting to build something that he and friends could use to manage their cards and decks. To him, of course, the natural next step was "Hey! We could build a Magic video game!"

## The requirements
After steering away from this and ensuring him that hanging out with his friends would be more interesting, he quickly developed a pretty robust list of requirements for this tool:

* Users can create their own profile
* Users can enter the cards that they owned
* Users can track what cards they wanted to acquire
* Cards can be placed in decks
* Your database of cards is searchable by asking questions like "Show me all green instants that I own" and "Tell me what red Planswalkers I need to get"

He definitely wants to track a lot of details of the cards that probably already exist on the web in various sources, so I'll help him create some kind of backend tool to scrape this info for use in the tracker.

## The technology
There's lots to do, teach, and learn here. I've tried to interest both of my older kids in simple programming before by goofing around with Python game libraries, but the realtime nature of something like a Flappy Bird clone becomes complex very fast. My son has also drawn storyboards of games he wants to create that are way beyond my abilities at the moment.

The web and its [stateless nature][stateless] seem *much* more my speed. I've also developed similar database-backed web tools at work in the past, so I knew that this was something that I could accomplish. One day we will get to games and realtime...for now, I'm going to stick with what I know.

That being said, I've begun the project with the following:

* [Python][python] is my hacking language of choice
* I love [Flask][flask] for its simplicity and (when implemented this way) its ability to isolate the models, views, and controllers.
* We'll start off with a [SQLite][sqlite] backend, but we'll develop migration scripts and use the ORM [SQLAlchemy][sqlalchemy] to ensure a more robust backend can be used later
* I'm not a designer, so [Boostrap][bootstrap] will make things look OK
* Naturally, we'll being using git for version control

Finally, I'm drawing a lot of inspiration from [Miguel Grinberg][miguel]'s fantastic [Flask Mega-Tutorial][mega-tut]. If you're interested in writing web projects in Flask, this is the only link you need to create some great stuff.

<p style="text-align: center">: : :</p>

As I said at the top of the post, I started this proejct already; I immediately learned several things about teaching my kids about technology. I'll follow up on this in the next post. Thanks for reading.

[mtg]: http://magic.wizards.com/
[stateless]: http://en.wikipedia.org/wiki/Stateless_protocol
[python]: https://www.python.org/
[sqlite]: http://www.sqlite.org/
[sqlalchemy]: http://www.sqlalchemy.org/
[bootstrap]: http://getbootstrap.com/
[flask]: http://flask.pocoo.org/
[miguel]: http://blog.miguelgrinberg.com/
[mega-tut]: http://blog.miguelgrinberg.com/post/the-flask-mega-tutorial-part-i-hello-world
