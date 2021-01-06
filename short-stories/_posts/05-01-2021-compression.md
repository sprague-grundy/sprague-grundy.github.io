---
layout: post
title: Compression is Abstraction
---

My brain does this weird thing sometimes.  I'll be minding my own
business, and then I'll see something perfectly normal.  That's not
the weird part.  The weird part is I'll see some ordinary everyday
thing, and it'll leap out at me and burn itself into my memory.  Like
that condition where soldiers can see bombs dropping when they close
their eyes, except it'll be some stupid everyday shit, like a mom and
kid sitting on a park bench staring at their phones instead of each
other.

So I'll just tell you now that the rest of this story is perfectly
fucking normal.  But it stuck with me.

---

I have a friend, Reginald.  Not Reggie or Reg, he likes all the
syllables.  He was really into speedrunning when we were in college.
Still is, I guess, but he has a kid now and that hobby is a bottomless
time-pit.  Anyway, the story starts when I was over at his place for a
barbecue.  It was mostly Angie's friends -- Angie's his wife -- so
Reginald had shown up for a few minutes at the start to shake hands,
then disappeared.

I found him in his home "office", which was really just a private room
with a computer and a door that closed, which also mean it was his
gaming setup these days.  He was playing one of the new neural-net
open world games.  AI Dungeon 3D Returns: Founder's Edition or some
shit.

Have you tried these things?  They're really impressive.  It's amazing
how many advances in technology have come from someone just looking at
a rickety system of hacks, taking the newest one, and saying "what if
it was all this *one* rickety hack?".

NVIDIA has been shipping neural-net based graphics upsampling for
years now, so games could render at low resolutions on consumer
laptops and have the world look amazing on 8K TVs.  Developers have
been using neural nets for dialogue generation, enemy AI, and
sometimes even procedural world generation if the map is big enough.

If you're using a neural net to generate a map, rendering that map to
a shitty 3D model, doing an even shittier rasterizing step, and then
trusting another neural network to pretty the thing up and make the
shadows look nice -- why not just cut out the middle man?

Games aren't one big neural net.  Yet.  The mechanics, the gameplay
and magic system and whatnot, are still written by hand.  Easier to
iterate that way, and games have to actually be fun.  But the NPCs,
the graphics, the audio, and even some of the more complicated stuff
like physics interactions are all just deep stacks of matrices
multiplying their hearts out.

But anyway.  Reginald was playing this game, but he wasn't really
*playing* it.  He had the game open on one screen, and a paused video
open on the other.  He was leaning forward, brow furrowed, running
into a rock at a very precise angle over and over again.  After a few
tries, he'd back off, look at the spreadsheet again, adjust the
camera, and run back at the rock.  There was a little girl NPC that
kept following him around while he did it, some kind of escort mission
or something.

I'd seen him do this a hundred times before in college.  He was trying
to get a finicky glitch to work.

He was dialed in enough that I don't think he even noticed I was
there.  Eventually, he got it: he clipped at the right angle or had
the camera looking at the right texture or whatever.  I guess this
game didn't have textures, but he booped whatever widget it had into
the right configuration.  The game freaked out for a second, the
little girl behind him warping into an elaborate fleshy sword.  Some
games look creepier than others when you make them glitch, but this
one was something special.  The girl-sword fell to the ground, streams
of lumpy flesh rolling off of it like vapor.  I made a noise,
involuntarily, and Reginald looked up.

We'd known each other long enough he didn't even say hello.  "Come
look at this shit!" he said instead, popping one of his earbuds out.
I walked over, putting my hands on the back of his chair and watching
the screen.

"You can use this rock to munge two object vectors," he said.  His
character walked over an picked up the girl-sword.  The flesh-vapor
continued to roll off of it.  Reginald winced at a sound in his
earbuds that I couldn't hear, turning down his volume.  "It screams,"
he said.  "Dope."

"Why the hell did they put that in the game?" I asked.

"They didnt."

"Is it a mod?"

"No, man.  It's like--"  He held up his hand, rotating them slowly as
he tried to figure out how to explain it.  "Imagine in, like, doom, if
you managed to mash two models together.  Like, a health pack and the
shotgun.  What'd you get?"

I shrugged.  "I dunno, depends how you mash them together.  Maybe a
box with a gun sticking out of it.  Maybe a new model with all the
points at weird coordinates.  Maybe the game couldn't load it."

"Right, right.  Exactly.  Because the representation of the objects is
super simple, it's just some polygons.  But that's not how this game
works."

Reginald swung the sword, in-game, and when it struck the ground, the
grass began to bleed.  "In this game, objects are just a big vector.
Like the bottleneck layer in a GAN."

"The what?"

"Like, um.  You know how JPEG compression is way better for natural
scenes than vector art?  Because wavelets do a better job of modeling
that type of data?  It's kinda like that.  The huge neural net that
renders the world and handles the physics is basically the mother of
all fantasy-world compression algorithms.  It can take a vector of
numbers and decompress it into an NPC, or a sword, or a rock, or the
sun, or whatever you want."

The grass didn't seem to want to stop bleeding.  Reginald walked away
from it, the game rendering bloody footprints behind him.

"I see," I said.  I didn't really see.  "So you mashed two of these
vectors together with a glitch, and the game just happily decompresses
it into...this?"

"Yeah, yeah, exactly.  You can generate all kinds of stuff.  We're
still testing combinations.  I wonder what this thing does to doors?
We might get a sequence break."

"How do you get the game to mash stuff together?  Like, why can it
even do that?"

"I dunno, man.  This guy Nascento37 figured it out.  Some shit with
NaNs causing an operation to abort and leave memory uninitialized.  It
doesn't really matter."

Reginald tabbed out to a text doc and started to write down what he'd
done.  He was clearly busy, so I clapped him on the shoulder and
wandered out to get more pulled pork.

---

That's the story.  Yup, that's all of it.  Perfectly normal, right?
I'm not sure why it sticks with me.

Maybe it's just me.  You see, when I was a little kid I thought magic
might be real.  Not in a "woo" sense, in a "these people on the
Internet say that putting corn in a mason jar and doing a bunch of
really specific shit can give someone you don't like a headache"
sense.  I was young, I didn't really have a good model of the world,
so it sounded pretty plausible, you know?

It never worked of course.  Not even once.  Even confimation bias
couldn't overcome the sheer magnitude of how much it didn't fucking
work.  And as I got older, I learned enough about physics to see why
it was mechanistically impossible.

But the thing that I keep thinking about is just how much that glitch
looked like magic.  The importance of the arbitrary location in the
world, the super specific set of actions that seemed disconnected from
the goal, all of it.  There was even a human sacrifice.

I'd always had the thought, kicking around in the back of my head,
that speedruns which used code manipulation look a lot like magic.  If
you have ten minutes, go watch the exit code injection speedrun for
Super Mario World.  It looks like fucking witchcraft.

But the result of those sorts of code manipulation speedruns always
look like video game glitches.  You warp to a different screen or
something.  In these new games, it looks like magic.  *Real* magic.

Which shouldn't matter at all.  But I can't stop thinking about i.
