# ece473-homework-6--multi-agent-pac-man-solved
**TO GET THIS SOLUTION VISIT:** [ECE473 Homework 6- Multi-agent Pac-man Solved](https://www.ankitcodinghub.com/product/ece473-homework-6-multi-agent-pac-man-solved/)


---

📩 **If you need this solution or have special requests:** **Email:** ankitcoding@gmail.com  
📱 **WhatsApp:** +1 419 877 7882  
📄 **Get a quote instantly using this form:** [Ask Homework Questions](https://www.ankitcodinghub.com/services/ask-homework-questions/)

*We deliver fast, professional, and affordable academic help.*

---

<h2>Description</h2>



<div class="kk-star-ratings kksr-auto kksr-align-center kksr-valign-top" data-payload="{&quot;align&quot;:&quot;center&quot;,&quot;id&quot;:&quot;94488&quot;,&quot;slug&quot;:&quot;default&quot;,&quot;valign&quot;:&quot;top&quot;,&quot;ignore&quot;:&quot;&quot;,&quot;reference&quot;:&quot;auto&quot;,&quot;class&quot;:&quot;&quot;,&quot;count&quot;:&quot;0&quot;,&quot;legendonly&quot;:&quot;&quot;,&quot;readonly&quot;:&quot;&quot;,&quot;score&quot;:&quot;0&quot;,&quot;starsonly&quot;:&quot;&quot;,&quot;best&quot;:&quot;5&quot;,&quot;gap&quot;:&quot;4&quot;,&quot;greet&quot;:&quot;Rate this product&quot;,&quot;legend&quot;:&quot;0\/5 - (0 votes)&quot;,&quot;size&quot;:&quot;24&quot;,&quot;title&quot;:&quot;ECE473 Homework 6- Multi-agent Pac-man Solved&quot;,&quot;width&quot;:&quot;0&quot;,&quot;_legend&quot;:&quot;{score}\/{best} - ({count} {votes})&quot;,&quot;font_factor&quot;:&quot;1.25&quot;}">

<div class="kksr-stars">

<div class="kksr-stars-inactive">
            <div class="kksr-star" data-star="1" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="2" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="3" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="4" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="5" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
    </div>

<div class="kksr-stars-active" style="width: 0px;">
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
    </div>
</div>


<div class="kksr-legend" style="font-size: 19.2px;">
            <span class="kksr-muted">Rate this product</span>
    </div>
    </div>
<div class="page" title="Page 1">
<div class="layoutArea">
<div class="column">
Assignment: Multi-agent Pac-man

Introduction

For those of you not familiar with Pac-Man, it’s a game where Pac-Man (the yellow circle with a mouth in the above figure) moves around in a maze and tries to eat as many food pellets (the small white dots) as possible, while avoiding the ghosts (the other two agents with eyes in the above figure). If Pac-Man eats all the food in a maze, it wins. The big white dots at the top-left and bottom-right corner are capsules, which give Pac-Man power to eat ghosts in a limited time window, but you won’t be worrying about them for the required part of the assignment. You can get familiar with the setting by playing a few games of classic Pac-Man, which we come to just after this introduction.

In this assignment, you will design agents for the classic version of Pac-Man, including ghosts. Along the way, you will implement both minimax and expectimax search.

The base code for this assignment contains a lot of files, which are listed towards the end of this page; you, however, do not need to go through these files to complete the assignment. These are present only to guide the more adventurous amongst you to the heart of Pac-Man. As in previous assignments, you will only be modifying hw6 submission.py.

A basic hw6 grader.py has been included in the .zip file, but it only checks for timing issues, not functionality. You can check that Pac-Man behaves as described in the problems, and run hw6 grader.py without timeout to test your implementation.

</div>
</div>
</div>
<div class="page" title="Page 2">
<div class="layoutArea">
<div class="column">
Warmup

First, play a game of classic Pac-Man to get a feel for the assignment:

python pacman.py

You can always add –frameTime 1 to the command line to run in ”demo mode” where the game pauses

after every frame. Now, run the provided ReflexAgent in hw6 submission.py: python pacman.py -p ReflexAgent

Note that it plays quite poorly even on simple layouts:

python pacman.py -p ReflexAgent -l testClassic

You can also try out the reflex agent on the default mediumClassic layout with one ghost or two. python pacman.py -p ReflexAgent -k 1

python pacman.py -p ReflexAgent -k 2

Note: You can never have more ghosts than the layout permits.

Options: Default ghosts are random; you can also play for fun with slightly smarter directional ghosts using -g DirectionalGhost. You can also play multiple games in a row with -n. Turn off graphics with -q to run lots of games quickly.

Now that you are familiar enough with the interface, inspect the ReflexAgent code carefully (in hw6 submission.py) and make sure you understand what it’s doing. The reflex agent code provides some helpful examples of methods that query the GameState: A GameState object specifies the full game state, including the food, capsules, agent configurations, and score changes: see hw6 submission.py for further information and helper methods, which you will be using in the actual coding part. We are giving an exhaustive and very detailed description below, for the sake of completeness and to save you from digging deeper into the starter code.

Note: If you wish to run the game in the terminal using a text-based interface, check out the terminal directory.

</div>
</div>
<div class="layoutArea">
<div class="column"></div>
</div>
</div>
<div class="page" title="Page 3">
<div class="layoutArea">
<div class="column">
Problem 1: Minimax

a. Before you code up Pac-Man as a minimax agent, notice that instead of just one adversary, Pac- Man could have multiple ghosts as adversaries. So we will extend the minimax algorithm from class, which had only one min stage for a single adversary, to the more general case of multiple adversaries. In particular, your minimax tree will have multiple min layers (one for each ghost) for every max layer.

Formally, consider the limited depth tree minimax search with evaluation functions taught in class. Suppose there are n + 1 agents on the board, a0, . . . , an where a0 is Pac-Man and the rest are ghosts. Pac-Man acts as a max agent, and the ghosts act as min agents. A single depth consists of all n + 1 agents making a move, so depth 2 search will involve Pac-Man and each ghost moving two times. In other words, a depth of 2 corresponds to a height of 2(n + 1) in the minimax game tree.

Write the recurrence for Vminmax (s, d) in math as a piecewise function. You should express your answer in terms of the following functions:

<ul>
<li>IsEnd(s), which tells you if s is an end state.</li>
<li>Utility(s), the utility of state s.</li>
<li>Eval(s), an evaluation function for the state s.</li>
<li>Player(s), which returns the player whose turn it is in state s.</li>
<li>Actions(s), which returns the possible actions that can be taken from state s.</li>
<li>Succ(s, a), which returns the successor state resulting from taking an action a at a certain state s.
No need to submit your answer. This is to brainstorm how to write your code for Problem 1b.
</li>
</ul>
</div>
</div>
<div class="section">
<div class="layoutArea">
<div class="column">
 Example text Example Condition

Vminmax(s, d) = Example text Example Condition (1)

 etc.

</div>
</div>
</div>
</div>
<div class="page" title="Page 4">
<div class="layoutArea">
<div class="column">
b. Now fill out the MinimaxAgent class in hw6 submission.py using the above recurrence. Remember that your minimax agent should work with any number of ghosts, and your minimax tree should have multiple min layers (one for each ghost) for every max layer.

Your code should also expand the game tree to an arbitrary depth. Score the leaves of your mini- max tree with the supplied self.evaluationFunction, which defaults to scoreEvaluationFunction. The class MinimaxAgent extends MultiAgentSearchAgent, which gives access to self.depth and self.evaluationFunction. Make sure your minimax code makes reference to these two variables where appropriate, as these variables are populated from the command line options.

Implementation Hints

◦ Read the comments in hw6 submission.py thoroughly before starting to code!

◦ Pac-Man is always agent 0, and the agents move in order of increasing agent index. Use self.index in your minimax implementation to refer to the Pac-Man’s index. Notice that only Pac-Man will actually be running your MinimaxAgent.

◦ All states in minimax should be GameStates, either passed in to getAction or generated via GameState.generateSuccessor. In this assignment, you will not be abstracting to simplified states.

<ul>
<li>You might find the functions described in the comments to the ReflexAgent and MinimaxAgent useful.</li>
<li>The evaluation function for this part is already written (self.evaluationFunction), and you should call this function without changing it. Use self.evaluationFunction in your definition of Vminmax wherever you used Eval(s) in part 1a. Recognize that now we’re evaluating states rather than actions. Look-ahead agents evaluate future states whereas reflex agents evaluate actions from the current state.</li>
<li>If there is a tie between multiple actions for the best move, you may break the tie however you see fit.</li>
<li>The minimax values of the initial state in the minimaxClassic layout are 9, 8, 7, -492 for depths 1, 2, 3 and 4 respectively. You can use these numbers to verify whether your implemen- tation is correct. Note that your minimax agent will often win, despite the dire prediction of depth 4 minimax search, whose command is shown below. Our agent wins just under 50% of the time: Be sure to test on a large number of games using the -n and -q flags.
<pre>       python pacman.py -p MinimaxAgent -l minimaxClassic -a depth=4
</pre>
Further Observations These questions and observations are here for you to ponder upon; no need to submit the answer to the following questions.
</li>
<li>On larger boards such as openClassic and mediumClassic (the default), you’ll find Pac-Man to be good at not dying, but quite bad at winning. He’ll often thrash around without making progress. He might even thrash around right next to a dot without eating it. Don’t worry if you see this behavior. Why does Pac-Man thrash around right next to a dot?</li>
<li>Consider the following run:

python pacman.py -p MinimaxAgent -l trappedClassic -a depth=3

Why do you think Pac-Man rushes the closest ghost in minimax search on trappedClassic?</li>
</ul>
</div>
</div>
<div class="layoutArea">
<div class="column"></div>
</div>
</div>
<div class="page" title="Page 5">
<div class="layoutArea"></div>
<div class="layoutArea">
<div class="column">
Problem 2: Alpha-beta pruning

a. Make a new agent that uses alpha-beta pruning to more efficiently explore the minimax tree in AlphaBetaAgent. Again, your algorithm will be slightly more general than the pseudo-code in the slides, so part of the challenge is to extend the alpha-beta pruning logic appropriately to multiple minimizer agents.

You should see a speed-up: Perhaps depth 3 alpha-beta will run as fast as depth 2 minimax. Ideally, depth 3 on mediumClassic should run in just a few seconds per move or faster.

<pre>     python pacman.py -p AlphaBetaAgent -a depth=3
</pre>
The AlphaBetaAgent minimax values should be identical to the MinimaxAgent minimax values, al- though the actions it selects can vary because of different tie-breaking behavior. Again, the minimax values of the initial state in the minimaxClassic layout are 9, 8, 7, and -492 for depths 1, 2, 3, and 4, respectively. Running the command given above this paragraph, which uses the default mediumClassic layout, the minimax values of the initial state should be 9, 18, 27, and 36 for depths 1, 2, 3, and 4, respectively.

</div>
</div>
</div>
<div class="page" title="Page 6">
<div class="layoutArea">
<div class="column">
Problem 3: Expectimax

<ol>
<li>Random ghosts are of course not optimal minimax agents, so modeling them with minimax search is not optimal. Instead, think about the recurrence for Vexptmax(s,d), which is the maximum expected utility against ghosts that each follow the random policy, which chooses a legal move uniformly at random. Your recurrence should resemble that of problem 1a, which means that you should write it in terms of the same functions that were specified in problem 1a.
Similar to Problem 1a, no need to submit your answer. This is to brainstorm how to write your code for Problem 3b.
</li>
<li>Fill in ExpectimaxAgent, where your agent will no longer take the min over all ghost actions, but the expectation according to your agent’s model of how the ghosts act. Assume Pac-Man is playing against multiple RandomGhost, which each chooses getLegalActions uniformly at random.
You should now observe a more cavalier approach to close quarters with ghosts. In particular, if Pac- Man perceives that he could be trapped but might escape to grab a few more pieces of food, he’ll at least try.

<pre>     python pacman.py -p ExpectimaxAgent -l trappedClassic -a depth=3
</pre>
You may have to run this scenario a few times to see Pac-Man’s gamble pay off. Pac-Man would win half the time on average, and for this particular command, the final score would be -502 if Pac-Man loses and 532 or 531 (depending on your tiebreaking method and the particular trial) if it wins. You can use these numbers to validate your implementation.

Why does Pac-Man’s behavior as an expectimax agent differ from his behavior as a minimax agent (i.e., why doesn’t he head directly for the ghosts)? Again, just think about it; no need to submit the answer.
</li>
</ol>
</div>
</div>
<div class="section">
<div class="layoutArea">
<div class="column">
 Example text Example Condition

Vexptmax(s, d) = Example text Example Condition (2)

 etc.

</div>
</div>
</div>
</div>
<div class="page" title="Page 7">
<div class="layoutArea">
<div class="column">
Problem 4: Evaluation Function

<ol>
<li>Write a better evaluation function for Pac-Man in the provided function betterEvaluationFunction. The evaluation function should evaluate states rather than actions. You may use any tools at your disposal for evaluation, including any util.py code from the previous assignments. With depth 2 search, your evaluation function should clear the smallClassic layout with two random ghosts more than half the time for full credit and still run at a reasonable rate.
<pre>     python pacman.py -l smallClassic -p ExpectimaxAgent -a evalFn=better -q -n 20
</pre>
We will run your Pac-Man agent 20 times, and calculate the average score you obtained in the winning games. Starting from 1300, you obtain 1 point per 100 point increase in your average winning score. In hw6 grader.py, you can see the how credit is awarded. For example, you get 2 points if your average winning score is between 1400 and 1500.

Hints and Observations

<ul>
<li>Having gone through the rest of the assignment, you should play Pac-Man again yourself and think about what kinds of features you want to add to the evaluation function. How can you add multiple features to your evaluation function?</li>
<li>You may want to use the reciprocal of important values rather than the values themselves for your features.</li>
<li>The betterEvaluationFunction should run in the same time limit as the other problems.</li>
</ul>
</li>
<li>Clearly describe your evaluation function. What is the high-level motivation? Also talk about what else
you tried, what worked, and what didn’t. Elaborate in code comments below betterEvaluationFunction.
</li>
</ol>
</div>
</div>
<div class="layoutArea">
<div class="column"></div>
</div>
</div>
<div class="page" title="Page 8">
<div class="layoutArea"></div>
<div class="layoutArea">
<div class="column">
File Description

hw6 submission.py

pacman.py

game.py

util.py

<pre>      graphicsDisplay.py
</pre>
<pre>      graphicsUtils.py
</pre>
<pre>      textDisplay.py
</pre>
<pre>      ghostAgents.py
</pre>
<pre>      keyboardAgents.py
</pre>
layout.py

search.py, searchAgents.py, multiAgentsSolution.py

Acknowledgement

</div>
<div class="column">
Where all of your multi-agent search agents will reside, and the only file that you need to concern yourself with for this assignment.

The main file that runs Pac-Man games. This file also describes a Pac-Man GameState type, which you will use extensively in this assignment.

The logic behind how the Pac-Man world works. This file describes several supporting types like AgentState, Agent, Direction, and Grid.

Useful data structures for implementing search algorithms. Graphics for Pac-Man.

Support for Pac-Man graphics.

ASCII graphics for Pac-Man.

Agents to control ghosts.

Keyboard interfaces to control Pac-Man.

Code for reading layout files and storing their contents.

These files are not relevant to this assignment and you do not need to modify them.

</div>
</div>
<div class="layoutArea">
<div class="column">
Stanford CS221: Artificial Intelligence: Principles and Techniques

</div>
</div>
</div>
