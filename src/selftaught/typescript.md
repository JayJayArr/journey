# Teaching myself TS

When writing JS you eventually come into a realm where your project gets so big/complex that you will be happy for a type system.
JS has the beautiful feature of not warning you when things will crash at runtime, and that's not what you want.
When developing you will want to be warned about things that maybe don't exist, that maybe are undefined, etc.

The TS documentation describes it pretty well when considering this example:

```JS
// Accessing the property 'toLowerCase'
// on 'message' and then calling it
message.toLowerCase();
// Calling 'message'
message();

```

> But assuming we don’t know the value of message - and that’s pretty common - we can’t reliably say what results we’ll get from trying to run any of this code. The behavior of each operation depends entirely on what value we had in the first place.
>
> - Is message callable?
> - Does it have a property called toLowerCase on it?
> - If it does, is toLowerCase even callable?
> - If both of these values are callable, what do they return?
>
>   The answers to these questions are usually things we keep in our heads when we write JavaScript, and we have to hope we got all the details right.
>
>   -- <cite>Typescript Documentation</cite>

You want your IDE to warn you about those kinds of issues, so you can prevent them from crashing at runtime.
Can you put that Object into this function? What comes back out?
What properties does this Object have?
What functions can you call on this Object?
Can this be undefined or null?

If you already use a type system, appreciate it, it has already saved you at least once.
If you don't use a type system yet: Might the errors you have experienced so far been caught by a type system?
