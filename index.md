---
layout: post
title:  "Adversarial Deep Learning"
---

# Adversarial Deep Learning
Adversarial learning generates applies small perturbations to 
the inputs of a deep learning architecture so that the neural network
outputs a wrong answer with high confidence. 


**Why does it matter?**
The lack of robustness to small perturbation is seen as a sign that 
neural networks do not learn the true data manifold. Moreover, adversarial
attacker could use that weakness to generate visually undetectable 
input perturbations that lead to a misclassified outputs. Such attacks 
could have dramatic consequences when applied to system with safety or security 
concerns. Think of how problematic it would be if an attacker can paint stop signs so that 
deep learning algorithms deployed in autonomous vehicles would recognize them as
an other sign. 

**What causes this vulnerability?**

$$mean = \frac{\displaystyle\sum_{i=1}^{n} x_{i}}{n}$$


the possibility
to 

Adversarial examples are input to trick the neural network. 
Changes are imperceptible to human perception. 
Here attacks are white box attacks with access to model parameters.

<ul>
  {% for post in site.posts %}
    <li>
      <a href="_drafts/advesarial.md">Adversarial Deep Learning</a>
      {{ post.excerpt }}
    </li>
  {% endfor %}
</ul>