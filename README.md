# Neural Networks from Scratch — An Interactive Course

A hands-on, browser-based course that builds a neural network from first principles,
grounded in a robotics-club story: predicting the **probability that a robot's shot
goes in** from three features you could read off a photo of the shot — its arc,
its distance to the goal, and how visible the goal is.

Each lesson is a single, self-contained HTML file — no build step, no install.
Just open it in a browser (or visit the published site).

## Lessons

1. **Features** (`lesson1_features.html`) — Reality is a function of inputs.
   Explore in 3D how a shot's make-probability changes with its arc, distance to
   the goal, and goal visibility.
2. **Hinges** (`lesson2_hinges.html`) — A line fails; a bendable ReLU "hinge"
   works. Stack hinges to approximate reality, then see the exact same model
   redrawn as a textbook neural network.
3. **Ramps** (`lesson3_ramps.html`) — Add a second input and the hinge becomes a
   tilted ramp. Combine ramps to fit a 2D landscape, then view it as a
   two-input neural network.
4. **How the Computer Learns** (`lesson4_learning.html`)
   — Error, derivatives, gradient descent, computational graphs, and
   backpropagation — one operation at a time.
5. **Learned Features** (`lesson5_learned_features.html`) — Instead of
   hand-measuring features, feed the network a raw photo of the shot and
   train it live; watch it invent its own feature detectors.
6. **Transformers** (`lesson6_transformer.html`) — Connect the whole
   course to a Transformer: the feed-forward layers are the ReLU machine
   from earlier lessons, and attention lets the pieces of the input
   (patches or words) share information.

## The unifying idea

Every lesson models the same "reality" function, so students carry one mental
model all the way from *features* to *backpropagation*. It turns three shot
features (x1 = arc, x2 = distance to goal, x3 = goal visibility) into a make-probability
between 0 and 100%:

```
make % = 100 · exp((x1 − 40 − 0.3·x2)^2 / −3000) · ln((110 − x2) / 10) / ln(11) · (x3 / 100)
```

## Running locally

Open any `.html` file directly in a browser. The lessons use
[Plotly](https://plotly.com/javascript/) via CDN for 3D plots, so an internet
connection is needed the first time a plot loads.

## Audience

Built for a high-school robotics club. The goal is intuition first — students
manipulate sliders and watch the model respond before any heavy math.
