---
layout: base.njk
title: PLACEHOLDER Graphical Exploration of Limits
description: Discover the concept of limits through graphical analysis and exploration
date: 2024-06-21
---

# Lab: PLACEHOLDER Graphical Exploration of Limits

## Objective
Develop an intuitive understanding of limits by exploring function behavior near specific points using graphical analysis.

## Materials Needed
- Graphing calculator or computer with graphing software
- Graph paper
- Ruler
- Magnifying glass (optional, for detailed graph analysis)

## Part 1: The Mystery of the "Hole"
**Time: 15 minutes**

Consider the function: $$f(x) = \frac{x^2 - 4}{x - 2}$$

### Investigation A: What happens at x = 2?

1. **Try to evaluate** $f(2)$ directly. What happens?

2. **Create a table** of values approaching $x = 2$:

| x | 1.9 | 1.99 | 1.999 | ? | 2.001 | 2.01 | 2.1 |
|---|-----|------|-------|---|-------|------|-----|
| f(x) |  |  |  | undefined |  |  |  |

3. **Graph the function** on your calculator. What do you observe at $x = 2$?

4. **Zoom in** around $x = 2$. What does the graph suggest about the "missing" point?

### Discovery Questions:
- What value does $f(x)$ seem to approach as $x$ gets close to 2?
- Does it matter whether $x$ approaches 2 from the left or right?
- How would you "fill in the hole" in the graph?

## Part 2: One-Sided Limits
**Time: 15 minutes**

### Investigation B: The Step Function

Consider the piecewise function:
$$g(x) = \begin{cases} 
x + 1 & \text{if } x < 1 \\
3 & \text{if } x = 1 \\
2x & \text{if } x > 1
\end{cases}$$

1. **Graph this function** carefully. Pay special attention to what happens at $x = 1$.

2. **Trace along the curve** approaching $x = 1$ from the left. What y-value do you approach?

3. **Trace along the curve** approaching $x = 1$ from the right. What y-value do you approach?

4. **What is the actual value** of $g(1)$?

### Analysis Table:

| Approach Direction | Limiting Value | Actual Function Value |
|---|---|---|
| From the left ($x \to 1^-$) |  |  |
| From the right ($x \to 1^+$) |  |  |
| At the point ($x = 1$) |  |  |

### Discovery Questions:
- Do the left and right approaches give the same result?
- Does the limit exist at $x = 1$? Why or why not?

## Part 3: Infinite Behavior
**Time: 10 minutes**

### Investigation C: Vertical Asymptotes

Explore the function: $$h(x) = \frac{1}{x - 3}$$

1. **What happens** when you try to evaluate $h(3)$?

2. **Create approach tables**:

**From the left of x = 3:**
| x | 2.9 | 2.99 | 2.999 | 2.9999 |
|---|-----|------|-------|--------|
| h(x) |  |  |  |  |

**From the right of x = 3:**
| x | 3.1 | 3.01 | 3.001 | 3.0001 |
|---|-----|------|-------|--------|
| h(x) |  |  |  |  |

3. **Graph the function** and observe the behavior near $x = 3$.

### Discovery Questions:
- What happens to the y-values as x approaches 3 from each side?
- How would you describe this behavior mathematically?
- What does "limit equals infinity" mean?

## Part 4: Oscillating Functions
**Time: 10 minutes**

### Investigation D: When Limits Don't Exist

Examine the function: $$k(x) = \sin\left(\frac{1}{x}\right)$$ near $x = 0$.

1. **Graph this function** using a viewing window like $[-0.5, 0.5]$ by $[-2, 2]$.

2. **Zoom in** progressively closer to $x = 0$. What do you observe?

3. **Try to trace** the function as it approaches $x = 0$. What happens?

### Discovery Questions:
- Does the function settle on a single value as $x$ approaches 0?
- How would you describe the function's behavior near $x = 0$?
- Why might this limit not exist?

## Part 5: Synthesis Activity
**Time: 10 minutes**

### Your Turn: Function Detective

For each graph below, determine if the limit exists at the indicated point. If it does, estimate the limit value.

**Function A:** (Draw or describe a function with a removable discontinuity)
- $\lim_{x \to 2} A(x) = $ _______

**Function B:** (Draw or describe a function with a jump discontinuity)
- $\lim_{x \to -1} B(x) = $ _______

**Function C:** (Draw or describe a function with a vertical asymptote)
- $\lim_{x \to 0} C(x) = $ _______

## Part 6: Real-World Connection
**Time: 5 minutes**

Consider the cost function for a shipping company:
$$C(w) = \begin{cases} 
5.00 & \text{if } 0 < w \leq 1 \\
8.00 & \text{if } 1 < w \leq 2 \\
11.00 & \text{if } 2 < w \leq 3
\end{cases}$$

where $w$ is weight in pounds.

1. **What is** $\lim_{w \to 1^-} C(w)$?
2. **What is** $\lim_{w \to 1^+} C(w)$?
3. **Does** $\lim_{w \to 1} C(w)$ exist?
4. **What does this mean** in practical terms for shipping costs?

## Reflection and Conclusions

### Key Discoveries

Write a brief explanation of each concept:

1. **Removable Discontinuity**: _________________________________

2. **Jump Discontinuity**: _____________________________________

3. **Infinite Limits**: _______________________________________

4. **Oscillating Behavior**: __________________________________

### The Big Picture

**In your own words**, explain what a limit represents and why it's useful in mathematics.

### Questions for Further Exploration

1. How might limits help us understand rates of change?
2. What happens to limits when we have functions like $\frac{\sin x}{x}$ as $x \to 0$?
3. How do limits relate to the idea of continuity?

## Lab Report

Create a visual summary showing:
- One example each of the four types of limit behavior you explored
- A written explanation of when limits exist vs. when they don't
- One real-world situation where understanding limits would be important

## Extension Challenge

Design your own piecewise function that has:
- A removable discontinuity at $x = 1$
- A jump discontinuity at $x = 2$
- A vertical asymptote at $x = 3$

Graph your function and verify that it has these properties.