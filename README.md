# Reverse a LinkedList Snake Game Project using Pure React and Vanilla Javascript :

# Goal of the Project:
1)Basically in the snake Game you're a snake on a 2D Board and usually you see a kind of outlines of the Squares int the board .you control the sanke and you've to eat the food that kind of randomly appears on the screen .There is a little like gear icon/flower icon and Whenever you eat the food your sanke gets bigger .Suppose if you hit the wall or your own tail for example your body you'll lose just to know to get a high score as possible  
2)second of all looped and ate my own body and So I died yeah thats what i am try to build 

# COMPONENTS:
Vanilla JS ,Pure React
I used create React App and npm package 

# Workflow:
Basically I have an App component here there comes our main app file and there it renders the board and there will be an Empty component where all of our code is going to go and I got the board CSS file and it serves as the Background the color of the Background so if I put in my board something like foo bar then you go to the foo bar and precreated an util File Where copy and pasted the function to generate a random Number from an interval in js which got from stackoverflow whene to trying to figure out the fn pops up on the board and close out these app.js and index.js files that rernders the app all we gonna be working on with the board file 

1) Let's jump into it and create a board with the 2D grid .Basically I created a board variable in react so its going to be a state variable you know need to access it very easily update it or Something it basically craetes a new 2d  Array I got a constant for the size of an array so right now we are creating 10 * 10 board Guess it will be 100 cells then I iterate over the board mapping every row to an element then for Every row I map every cell to an element and So i got three classes board row and cell then in cells only I have most of my styles so now they are over 50 pixels this might be little big but we'll see and got an outline and putting an outline on the board .beacuse otherwise like have an outline on the board if I didn't pick up the outer outline innner cells will gets overlap and already had an created an internal representation and kinda looks like green colour I added a snake cell,food cell and background class name of the element determining whether its a snake cell/ food cell if its red i put a false here then It will back to normal .

2) For snake respresentation I go over with singly Linked list Every cell or body part of the snake its going to be a Linked list node that points to the next part in the snake when the snake moves like it body has to know where to go next the head is pretty easy of reference of where the head is wht the next cell the head has to go through based on the direction that the snake is going but everty other node needs to know where having a linked list is very easy every node equals to its next pointer but we need to have athe access to the tail I think the tail we want to do the reversal the tail have to become the head so i think we want to have the access to the tail .so i'll keep a reference for now and created a classesa for the linked list Clearly Singly linked list classes that holds the reference to the tail and head.when you created a linked list need to pass the value it creates the first node in the linked list got a value and dot next pointer to how do we actually know whats cell is a snake.Lets say the snake is at the middle of an array .we need to have some sort of hash table that ponts to whether or not the sanke is at a particular point .every snake cell should know where currently it is .So for movement of left just take left and update a number going to need the directions so probab aly Typescript directions like left,right up, down not gonna be controlling just seeing how the snake is moving .The original sanke cell trying to figure it out I got a react bug kind of challenging .Right now going to move forward and try to do like kind of the game for little bit just I have a manual button to press to move the snake because this works right .I got the movement with the manual and trying to go back automatic and there will be a curr row /col snake head which is stored in my linked list node and the value is  like a cell class I computed my n/r of cells when I created the board I started one and the maximum cell possible cell value which is the actual board size multiplied by board size and it came pretty naively I have a while lopp and It keep geenerating the random numbers until I found one .So keep ressting the game at every movement .If i Go out of bounds and resets the score may be it will be little bit more polished  so that you can see the score atb the very end and see how big your snake is . At some point I deafulted my snake to have a sizeof Three or four just to play around .Basically we update the tail of the ll we create a new node we set the list as that new node update its pointer to the prev. tail 

3)so another function node I pass the tail in the direction I got the new direction of the next node of the tail so that way I know if the tail here pass in the key and I have a hashtable like direction which is looking like a typescript enum 
I had  to handle the  out of bounds bug on the browser console 
basically I got the next head coordinates of the next head of the snake so where we would be moving 
i have got the gross snake function defined right and I got the growth node coordiantes .So the growth node I yet to add 
Got to see growth of the snake without doing the manual .Basically I create  new head as  I'm moving the snake right this is all the new head logic 
Was trying to debug the whole like bug that I had a movement that wasn't working automatically turns out It has to do with the set interval method and making it declarative  to work with react hooks So I found this .If now if the food reverses the direction then wer'e going to call a method named reverse snake and its literlly going to reverse

4) the method which reverses a linked lists I put it in utils and exported the same function reverse a linked lists 



# PRODUCTION DEMO LIVE : https://csb-0vihv5.netlify.app/

