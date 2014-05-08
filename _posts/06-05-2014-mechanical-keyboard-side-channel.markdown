---
layout: post
title: Acoustic Side-Channel on Mechanical Keyboards
tags:
- keyboard
- side-channel
- todo
---


All mechanical devices leave traces when used. Keyboards are no exception.
I recently started reading Pete Wright's *Spy Catcher* in which he describes
(among other things) the various methods he used against foreign
(ie. non-British) intelligence agencies.

It occured to me that it should be possible, provided a decent sound recording,
to figure out which keys have been pressed in a typing session. Below you'll
find my recording of typing this very text, with back-spaces, arrow-key usage,
and all the things we do when we type.

<iframe width="100%" height="166" scrolling="no" frameborder="no"
src="https://w.soundcloud.com/player/?url=https%3A//api.soundcloud.com/tracks/148228406&amp;color=ff0707&amp;auto_play=false&amp;hide_related=false&amp;show_artwork=false">
</iframe>

It should be possible to attack this recording and reconstruct this text. The
parameters one should keep in mind are

* The keyboard's profile
* The typist's hand


The profile is the unique sound made by a certain key on a certain keyboard.
The hand is the user's typing profile, including things like quick two-key
presses, changes in key sound due to key depression force and stuff like that.

End recording.

---

A few hints: My emacs inserts a space after every comma automatically and I'm not
really used to it yet, so after every *comma* there's a *space* and a
*backspace* sound.

I grew up in the digital era where signals are high and low. Working with sound
always terrified me because the signal is analog. I guess it's time to change
that.

It turns out my phone was more than capable of recording all the small details
that make the attack possible. I exported it to `.WAV` from its native `.3ga`
which is probably overkill; I should be able to work with an `.mp3` as well.
After all Wright had much less sensitive microphones and managed to figure out
the starting positions of cipher machines, among other things. I haven't
finished the book but I wonder why he didn't try to run this attack on recordings
of typewriters.

This is what the first 18 seconds look like in Audacity:

![18 seconds of typing]({{ site.url }}/assets/keyb_18.png)

Minute imperfections during keyswitch construction shouldn't make much difference
on the sound produced by each key. Wear sustained during normal use should though
and the effect should be amplified in older keyboards.