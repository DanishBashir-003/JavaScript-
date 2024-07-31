All right, guys.

So I want to spend a little bit of time on data types.

So when you're dealing with code, any any type of code, any language, and you're dealing with data,

that data is associated with some kind of data type, okay?

And it doesn't matter which language you're using, they all have some kind of data types and they can

be different language by language.

Now in JavaScript, you essentially have two types of types.

You have primitive data types and you have reference types or objects, and I'll talk about those in

a second.

But I want to start off with primitive data types.

Now I feel like a lot of JavaScript courses kind of skip over some important fundamentals.

And what I want to do is I'll talk more about this in the next video, but I want you to understand

how these data types are stored and how primitive data types are different or are accessed differently

than reference types.

But again, I'll talk more about that in the next video.

Right now I just want you to know what these types are.

So the first is a string, which we've dealt with.

So a string is essentially a sequence of characters, and a string must be enclosed in either double

quotes or single quotes or backticks.

Next we have a number which are integers which could be positive or negative numbers as well as floating

point numbers or decimals.

Now, in some languages you actually have either a decimal and or a float type.

In JavaScript, we don't if it's an integer or if it's a decimal or a floating point number, it's they're

all the same.

They're all going to be the type of number.

Okay, So keep that in mind.

Next we have a Boolean which represents a logical entity.

It can be either true or false.

Next we have NULL, which is the intentional absence of any object value and a lot of people get null

confused with undefined, which I'll talk about next.

But just know that null is it's always it's intentional.

It's supposed to be there but it's supposed to be null.

It's supposed to be empty.

You can essentially think of it as empty.

Now the next one undefined is a variable that hasn't been defined or assigned.

Okay, so null is purposeful.

Undefined usually isn't.

All right.

Next, we have a symbol which I'm not going to talk too much about right now because it's kind of advanced

and it was actually added in 2015 or ES6.

So a symbol is essentially a built in object whose constructor returns a symbol, a unique symbol or

a symbol that is unique.

All right.

And we'll get into that later.

It's not something you use very often, at least I don't.

And then the last one is a new data type that was just recently added called big INT.

Okay.

And it just represents really, really big integers, really large numbers that the number type can't

handle.

All right.

And we will jump into some code in this video and just kind of show you how to how to store each of

these in a variable.

So the next type of type is reference or objects.

Now reference or objects that are non primitive.

And when we assign a reference type to a variable, the variable is given a reference to that value.

And again, I'm going to talk more about how reference types and primitive types are stored and accessed

in the next video.

But object literals arrays functions.

These are all examples of reference types.

Now in programming, you have something called static typing or statically typed and you have dynamically

typed.

JavaScript is a dynamically typed language.

And what this means is that we don't explicitly define the types for our variables.

So if I say like const name equals Brad, I don't have to put const name, string equals Brad, It just

knows it's dynamic.

With many languages you actually have to, you have to add the types yourself.

Those are statically typed languages like C, C plus plus Java.

And I'm sure that some of you have worked with some of those languages in JavaScript.

You don't explicitly set your types.

However, there is something called TypeScript, which is very, very popular and it's a superset of

JavaScript, meaning that it's everything that JavaScript is.

It essentially is JavaScript, but it also has some additional features, including static typing.

Okay, so there are reasons to use static typing.

It is more code that you have to type, but it can make your code more verbose and it can make it less

prone to errors.

And a lot of people really love TypeScript, so that might be something you want to look into once you

really learn the fundamentals of JavaScript.

Okay.

So I just want to jump into VS code and go over these types in the text editor and also show you how

we can get the types of a specific variable.

So let's start off with strings, which are very simple, just they're just sequences of, of characters.

So I'll create a variable and I'm using const.

Like I said in the last video, I use const for everything unless I know I'm going to reassign it.

So we'll say first name and we'll set that to Sarah.

All right, now I want to console log out the value so we'll say first name, but I also want to show

you how we can get the actual type from this first name variable.

So as a second argument, I'm going to pass in the type of operator.

Okay.

So just type of and then a space and then whatever you want to get the type of so first name and now

you'll see it's logging out.

Sarah and String.

All right.

Now there's going to be a few variables that I want to show the value and the type, and I don't want

to type it twice.

So I'm going to create another variable here.

We'll just call it output.

And for now, I'll set it to first name and then let's come down here and put output.

Now I just want to mention some little, little tips and tricks as we go along.

I already went over some shortcuts, but just to kind of remind you, we can go to the end of this first

name, hold shift and then highlight it, and then we can do a command or control D to select the next

instance of first name and then replace it with output and then save.

Okay.

And we should get the same result.

So I'll just mention little tips and tricks like that as we go along.

So the next type I want to look at is number.

So let's do const.

We'll say age equals 30.

So that's an example of a number.

If I change that to age, we get 30 and it shows number from our type of operator.

Now I also want to mention that decimals, so if I do temp and set that to, let's say 98.9 and then

we look at the type for that, that's also going to be a number.

There's no specific float or decimal or anything like that.

Everything is a number in JavaScript.

So the next type is boolean, which is really simple.

It's just a true false value.

So maybe we want to say like has kids since we're talking about a person and we'll set that to true

and then we'll come down here, we'll change the output to has kids and we get true and it says Boolean.

So the next one is null, which is basically like an intentional empty value.

So maybe we have like an apartment number, but let's say this person lives in a house, so we set that

to null.

There's no apartment number, there's no need for one.

And this one is a little weird because if we set this to apartment number and we look at the value,

which is null, and then we look at the result of this type of we get object.

Okay, now this is a little confusing because NULL is not an object, it's not a reference type.

It's a primitive.

But there's a reason for this.

It's kind of in summary, it's kind of a mistake.

In fact, I'm going to paste in.

The the link right here if you're interested.

And we can check it out real quick.

So let's go to that link.

And it just kind of explains why this happens.

And it has to do with the first implementation of JavaScript values will represented as a type tag and

value.

The type tag for object was zero NULL was represented as the null pointer, which was 0X00.

Consequently NULL had zero as a type tag, hence the type of return of object.

So in case you're wondering why it says object and not null, that's why.

But it's not.

It's not that important honestly.

Now the next is undefined and you're probably not going to purposely set variables to undefined very

much.

But just to show you if we were to do remember in the last video I showed you we can we can use let

to just create a variable but not actually define it to something.

So I'll just say let score and then we'll pass that in here to output so we can see the value in the

type.

And both are undefined, the value and the type.

Okay.

So if you just set a variable and you don't define it, it's going to be undefined.

Now you can also explicitly set it to undefined.

You don't do this very much, but I could say const score, let's just comment this out and I could

just say set it to undefined and we get the same thing.

All right.

Now a symbol is a primitive type, but it's not something that you're probably going to use very much,

especially in your early career.

But just to show you we can create, let's say, ID and let's set that to symbol.

So we're going to say symbol with parentheses and then pass in a unique identifier of ID, and then

we'll change this to ID and save and you'll see we get symbol as our type.

And then the last one is the I should say the last primitive type is big int, which is just a really

big number that is too big for the number type.

So I'll say const N and I'm actually going to just copy or paste in this number here.

So it's basically this long string of numbers.

And then N And if we were to put N right here and save, we get the type of big INT.

Now as far as reference types, let's come down here and in the next video I'm going to talk about the

difference in how these, how primitive and reference types are stored and accessed.

But as far as what reference types are arrays, object literals functions.

So just to give you an example, we'll create a simple array, I'll call it numbers.

Okay.

And then if I were to.

Actually, we want to put.

Let's grab this and let's put this up here.

We want this above the output.

And then let's change this to numbers.

Okay, if I save that, it's going to show the array as the value and object as the type.

Okay.

Any reference type is an object.

So an object literal of course, is also an object is also a reference type.

So if I say person and we're going to learn all about objects and arrays and get much more advanced,

but just to show you.

We'll say, Brad and then if we change this here to person, you'll see we also get object.

Now a function is also a reference type.

So I'm just going to create a very simple function called Say hello and just have it do a console log

of hello.

And then down here, let's swap this out for say hello.

So you'll see for the value for the console log of the value.

It's just the function itself.

I didn't call it with parentheses.

And notice that instead of object it says function.

Now it's still an object.

It's just defined as a function object.

And I'm going to put the documentation link here if you want to read more about that.

And in the final version of the Sandbox, I'll label what these links are and stuff.

So I'll make things a little neater.

But yeah, that's it.

As far as what the types are, the primitive types and reference types are objects.

In the next video, I just want to quickly go over how those are stored in memory.

0:00
