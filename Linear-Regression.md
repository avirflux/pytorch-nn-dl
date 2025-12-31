Linear Regression is the simplest form of ML. Imagine we have data points showing how much something changes with another thing like temp and ice cream sales. The model learns a line that best firts those points so it can predict the new outcomes.

In 1D Linear Regression we predict a single output (y) from a single input (x). The math behind the model is simple

- y = w\*x + b
  w: the weight aka slope of the line
  b: the bias
- x is the input neuron. w and b are the learnable params, and y is the output

1. 1D LR Prediction: 1 Parameter : Computers can learn to draw a straight line through messy dots aka Linear Regression. The computer does not know the line at first but we can teach it by showing its mistakes ad heping it get better. Imagine we have a bunch of red dots on a graph. The dots are measurments: when x is small, y is bigg, and when x gets bigger, y gets smaller. The secret line has a slop of -3 meaning for every step right it goes down 3. But dont forget I added some noise so the dots arent perfect.

a. The number we are teaching is "w"

- the computer only has to learn one magic number "w" aka the slope
- if "w" is to big, the line is super steep the wrong way
- if "w" is just right, it first the dots nicely
- we can start with a silly guess like w=-10, bc the cimputer has no idea yet

b. Guessing the line

- the computer guesses the line with prediction=w\*x
- It draw the guess in blue over the red dots and at first it looks terrible

c. How wrong are we

- we can measure how wrong the guesses are using Mean Squared Error (MSE)
- Think of MSE like the "oops" score:
  for every dot, loot at how far away the blue line is
  square that distance (so big mistakes count extra)
  Add them all up and divide by how may dots -> that the "oops" score
  High score = very wrong
  Low score = good job

d. The cost mountain

- Imagine the "oops" score make a giant hill or bowl
- the bottom of the bowl is the perfect w(-3)
- Wherever our current w is, were somwhere on the side of the bowl.
- The higher up, the worse it gets

e. Gradient Descent - Sliding Down the Hill

- The cumputer feels which way is down hill aka "graident", like how steep the slide is. It take a tiny step downhill by changiing "w" a litter bit.
- We control the step size with the "learning rate"
- Then it guesses again, measure "oops" again, and slides again
- We do this 12 times and each time we awatch the red dot ("w") slide down to the best spot.

2. 1D LR Prediction 2 Paramater: Now we are teach two numbers. The slope "w" adn the starting height "b" aka bias. The full guuess is now: prediction = w\*x+b

a. Computer will learn two magic numbers

- w: how steep and which direction the line goes
- b: where the line crossses when x=0. like lifting or lowering the whole line
- with two numbers, there are endles wrong comboincation. this is like a hughe landscape of good and bad guess.

b. The cost bowl

- Its now in 3D. Instead of a simple hill like with 1 parameter, the "opps" score (MSE-how wrong the line is) makes a giant 3D bowl
- The bottom of the bowl is the perfect w and b
- Ever possible pair (w,b) has a height = how big the mistakes are
- We drew the bowl in colors. Yellow high up = very wrong. Dark low = good.
- There is also counter map, think of this like the birds eye view with circles like a treasure map showing rings around the best spots

c. Guesing the full line

- The computer guesses: blue line = w\*x+b. At firs with bad w and b. the line is owhere near the read dots

e. Measuring the "Opps" (MSE)

- How far is the blue lune from each red dot?. Square the distances (big oops count more), average them → "oops" score.

f. Sliding Down the Big Bowl (Gradient Descent with Two Directions)

- The computer feels the slope of the bowl in both w and b directions (that's the gradient—like which way is downhill for tilt and for height).
- It takes a small step downhill in both directions at once (learning rate 0.1—like careful baby steps).
- Then guesses again, measures oops again, and slides again.

g. Watching the Adventure Like a Movie

- Every few steps, we saw two pictures side by side:
  Left: Red dots and the blue line getting closer and closer to fitting them.
  Right: The contour treasure map with red X's showing where our (w, b) guesses are—watching them march toward the center of the circles!
