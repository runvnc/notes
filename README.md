# notes

LOL https://spion.github.io/posts/es7-async-await-step-in-the-wrong-direction.html

> Generators are JavaScript's programmable semicolons. Lets not take away that power by taking away the programmability. Lets drop async/await and write our own interpreters.

First of all, are we sure we want a semicolon to be programmable? Semicolons mean "do the next thing". Generators can like you say do pretty much anything, but I think we are lucky they are more visible than semicolons. It would be pretty hard to figure out what the heck the program was doing if every semicolon had its own behavior.
Secondly, no one is saying to drop generators. You can still use them to embed interpreters for transactions, or regular iterators, or whatever you want.
But if I just need to say "do this thing, wait until its done, do the next thing, wait until that's done" then I should not have to "write an interpreter". There absolutely needs to be a simple way to do that. And actually we are better off having that separate from generators, that way we can tell the difference between when it is just waiting for something to finish and when it is running some interpreter or whatever interesting thing you put in your generator.
