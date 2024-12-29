# Building this app

## Sunday 29th December

After a week off for Christmas, it's time to start working on a passion project before the tumult of School of Code recommences. They say the hard part is knowing what to build. But I have a dream of an app I've wished existed for a long time. It sounds so simple, yet I know it's going to be hard, and perhaps impossible (legally rather than technically, although with my rookie knowledge it will be technically hard too). 

I want to be able to send someone the equivalent of a mixtape. That is, I curate songs (probably 2 x 45 minute sessions, as per a 90 minute cassette) and they get to listen to it _without any track listing_. They just listen without prejudice. It is very, very easy to make a great playlist on Spotify for a friend, but as far as I know it is currently impossible to share / send it "blind". That's the point of my web app, Blind Mixtape.

It might look a bit like
[this.](dev_images/blind_mixtape_napkin_concept.png)

This morning I kicked off by having a good look through the Spotify API. Having learnt a little about APIs, I could just about make sense of the basics, although there's clearly a lot going on I don't understand at all. To optimize for morale, I put it aside and got cracking with the basic files for a webpage, where I embedded a Spotify player widget for one of my own playlists. It was tempting simply to hide this with a bit of javascript and build my functionality on top, but (a) I'm going to need to use the API to make this work for anyone's playlist's but my own, and (b) Using the Spotify widgets subjects you to some restrictions according to the Developer Agreement:

> a. You shall display the Spotify Widgets in the form made available by Spotify, without alteration, and in accordance with the requirements set out on our developer website.
b. You shall not obfuscate the Spotify Widgets in any way, whether by banner advertisements or by any other means, or alter the form or format of the Spotify Widgets from that made available by Spotify. 

So widgets are out. Next I looked through the Developer Agreement and [Brand Guidelines](https://developer.spotify.com/documentation/design) to see if what I want to do is prohibited. I can't find anything to say it is. There is mention of having to follow certain rules "if you're using artwork and/or metadata provided by Spotify" and "when you're showing any playing views in your app". But I'd be doing neither of these things! I would still provide a path back to Spotify proper, at the point of reveal (_after_ listening). So I think what I want to do is permitted. Yay! Now I just have to work out how to do it, and deal with the possibility that it won't work for free accounts, which I believe are condemned to interminably shuffle mode. Never mind. Most people interested enough in music to want to make a blind mixtape probably have a premium Spotify account anyway.