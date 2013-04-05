A Unified Theory

Disclaimer: This may very well turn out to be little but empty words. Having played with the idea in my mind for a while now I'm putting out there in the case that it isn't.  So humour me for a bit why don't you?

I would say that today, one can make a computer do practically anything.  The current languages that we use today are amazingly good at allowing us to create cool shit.  Problem is though, that these things often end up at the upper end of the complexity spectrum.  And that is by definition a bad thing.

This complexity always arises due to the same underlying issue.  Rarely, if ever, are we asking our computers to do one thing alone, expressable as one nicely dressed function.  It is always more than that, several functions interacting and depending on each other.  And thus we have complexity.

Now, we can build really nice functions, especially if we limit these to do a singular thing.  And to be fair, there are also languages which allows us to combine some of these functions quite nicely without making them *too* complex.  But there is always a limit, beyond which complexity lies.

**To battle this complexity, here is what I propose:**

Let's use these singular functions as atomic building blocks and model the interactions between them with a new language.  To define this language we first have to examine the nature of these interactions.

First we need to consider that the functions actually need to expose two distinct parts, the execution entry and exit.  Since this new language only will deal with function interactions, and not the execution itself, we can consider the entry essentially decoupled from the exit.

Along with this we have function chaining, the output of one function is the input of another.

Now, function interaction is simply when their exits trigger other entries and transfer the appropriate output to input.  Lets allow these exits to trigger several entries at ones.  Meaning that functions can both be chained sequentially and in parallel.

That is essentially it, but to make life easier I will also include three additions to this.  The pure approach would properly be to only allow a function exit once and only once, but I suggest we allow them to exit zero or more times.  This can be considered as if function output is "streamed".

Since the entry is decoupled from the exit, they will also be decoupled in time.  So let's say that a function may take zero or more time to exit.

Finally I want to flesh out the input and the output.  I'm sure you guessed it, zero or more inputs along with zero or more outputs.

Now we have covered the interactions between two functions fairly well, but let us also consider the case of longer chains than that.  From the rules we already have there isn't really a limit to the chain length, and I am not about to introduce one either.  Instead I will introduce a scope.  So that outputs are effectively pass along if they are used further down the chain.

Now, what have we ended up with?  With these rules we can define a wide range of function interactions.
