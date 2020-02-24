---
layout: post
title:      "Solving a Booleans Lab!"
date:       2020-02-24 19:54:18 +0000
permalink:  solving_a_booleans_lab
---

So you've come for advice in a booleans lab. I get it, I had a tough time of it myself. In solving a booleans lab, first we understand what a boolean is.  A boolean is a true or false data type. In Ruby, it's represented as simply "true" and "false". Booleans are most commonly used to implement control flow, so here's an example: IF the user types in a correct password (true) then allow him access to his account. IF the user types in an incorrect password (false) then prompt him to retry! So the first boolean lab i came across was in regards to "if" statements, which are at their very core one of the purest representations of booleans at work in Ruby. We'll go over the "Speaking Grandma" lab in this blog post!

This lab asks us to :
```
# Write a speak_to_grandma method.

# Whatever you say to grandma, she should respond with
# HUH?! SPEAK UP, SONNY!
# unless you shout it (type in all capitals).

# If you shout, she can hear you (or at least she thinks so) 
# and yells back

# NO, NOT SINCE 1938!

# However if you say 'I LOVE YOU GRANDMA!', she should respond with
# 'I LOVE YOU TOO PUMPKIN!'
```

So right away, we define our #speak_to_grandma method, taking in an argument of a phrase (this argument being the input we use to speak to our grandma):

```
def speak_to_grandma(phrase)
end
```

So, I started with the simplest part of this. If you say, "I LOVE YOU GRANDMA!" (if this input is 'true') she will respond with, "I LOVE YOU TOO PUMPKIN!"

```
> def speak_to_grandma(phrase)
>        if phrase == "I LOVE YOU GRANDMA!" #this says, if our phrase is equal to (==) "I LOVE YOU GRANDMA!" then:
>                 "I LOVE YOU TOO PUMPKIN!"         #our first boolean! If our "if" statement proves "true", then this line executes
>        end
>   end
```

Then we move on to our other conditions (IF this statement is true, THEN)! Let's take on this part:
If what we say is NOT upper case (shouted) then she responds with, "HUH!? SPEAK UP SONNY!"

```
def speak_to_grandma(phrase)
       if phrase == "I LOVE YOU GRANDMA!"
			           "I LOVE YOU TOO PUMPKIN!"
				elsif phrase != phrase.upcase #here we use our shebang operator ("!") and the #upcase method!
				         "HUH!? SPEAK UP SONNY!"
				end
end
```

So above, we use our shebang operator ("!") which Ruby reads as "not"! So it is comparing both sides of our elsif statement! if our arguement of "phrase" IS NOT EQUAL to "phrase.upcase" (the #upcase method is literally what it says! Upper case!) then the statement is true! If the statement proves true, she responds, "HUH!? SPEAK UP SONNY!".

Great! So let's move on to the last part of our solution! if our phrase arguement IS upper case, grandma thinks she hears us and responds with, "NO, NOT SINCE 1938!"

Knowing what we know about our #upcase method and our equal-to (==) operator, we can do this easily!

```
def speak_to_grandma(phrase)
         if phrase == "I LOVE YOU GRANDMA!"
				        "I LOVE YOU TOO PUMPKIN"
				 elsif phrase != phrase.upcase
				        "HUH!? SPEAK UP SONNY!"
				 else phrase == phrase.upcase #if our argument of phrase is EQUAL TO phrase.upcase (uppercase) then its true!
				        "NO, NOT SINCE 1938!"      #so grandma responds....
				end
end 
```

Congratulations! We've solved our first booleans lab using "if", "elsif" and "else" with some boolean operators ("!")!
				

