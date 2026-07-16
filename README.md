# Neural Networks from Scratch — An Interactive Course

A hands-on, browser-based course that builds a neural network from first principles,
grounded in a robotics-club story: predicting a robot's **score** from features like
driving speed, driving practice, and shooting reliability.

Each lesson is a single, self-contained HTML file — no build step, no install.
Just open it in a browser (or visit the published site).

## Lessons

1. **Features** (`lesson1_features.html`) — Reality is a function of inputs.
   Explore in 3D how a robot's score changes with driving speed, practice, and
   shooting reliability.
2. **Hinges** (`lesson2_hinges.html`) — A line fails; a bendable ReLU "hinge"
   works. Stack hinges to approximate reality, then see the exact same model
   redrawn as a textbook neural network.
3. **Ramps** (`lesson3_ramps.html`) — Add a second input and the hinge becomes a
   tilted ramp. Combine ramps to fit a 2D landscape, then view it as a
   two-input neural network.
4. **How the Computer Learns** (`lesson4_computational_graph_v11_learning_rates.html`)
   — Error, derivatives, gradient descent, computational graphs, and
   backpropagation — one operation at a time.

## The unifying idea

Every lesson models the same "reality" function, so students carry one mental
model all the way from *features* to *backpropagation*:

```
score = 0.5 · exp((x1 − 50 − 0.3·x2)^2 / −3000) · ln((x2 + 10) / 10) · x3
```

## Running locally

Open any `.html` file directly in a browser. The lessons use
[Plotly](https://plotly.com/javascript/) via CDN for 3D plots, so an internet
connection is needed the first time a plot loads.

## Audience

Built for a high-school robotics club. The goal is intuition first — students
manipulate sliders and watch the model respond before any heavy math.
