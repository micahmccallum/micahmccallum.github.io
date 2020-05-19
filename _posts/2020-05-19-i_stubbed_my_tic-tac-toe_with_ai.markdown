---
layout: post
title:      "I Stubbed My Tic-Tac-Toe with AI"
date:       2020-05-19 18:18:04 +0000
permalink:  i_stubbed_my_tic-tac-toe_with_ai
---

When I started the *Tic-Tac-Toe with AI* project I had a pretty good idea of what I wanted to do since this is the third iteration of T-T-T in the Flatiron course up until now.  I knew that I needed to display the board, count the turns, check for a winner using win combinations, etc.  I got started and felt like I was just flying along, happily coding, until I stubbed my proverbial toe with the AI element of the project.  I had a real hard time with this.  However, looking back at my process, I can say that my biggest error was trying to make it too hard.

I know, the README said the following: 

> You can hardcode your logic, things like "On turn 1 always try to go in the middle if you can" and if not "try to go in a corner" or any logic tree you can think of - there is an algorithm called Min/Max, but it's going to be hard to implement given our current implementation of a Game, so we recommend building something that's a more colloquial or condition-based algorithm.
> 

I read that a few times and I took it as a challenge, I wanted to try something that wasn't hardcoded.  I researched the idea of a min/max algorithm, and even thought that it might work, but,  in the end, what the README says is true, in order for the min/max to work I, at least, need to implement a game object.  If I understand min/max correctly, as the algorithm performs it's magic it needs to create many instances of a game object in order to "foretell" what move will produce a win, block or fork.  I just didn't want to rework the whole thing so I decided to hardcode the first moves like this:
```
if @board.turn_count == 0
        int = [Board::CORNERS.sample, Board::CENTER].sample
      elsif @board.turn_count == 1
        @board.taken?("5") ? int = Board::CORNERS.sample : int = Board::CENTER
```
After that I wrote methods that checked the board for tokens and based on the board state would play a token to get two in a row if the third space were empty, block if the opponent had two in a row or play a third token in a row for the win.  It seems to work well enough but I still want to try the min/max someday.  I just hope I don't stub my other *Tic-Tac-Toe* on **that** AI.

