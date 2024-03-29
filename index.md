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
Initially, non-linearities were thought to explain the lack of robustness to adversarial 
inputs. However, Goodfellow et al. show that linear perturbations of non-linear models are 
sufficient to generate misclassification. Consider an image $\textbf{x}$ represented by integer
pixel value between 0 and 255. Any perturbation within 1/255 precision should not 
lead to different model output. Consider a perturbation $\eta$ within 1/255 precision and the
resuling perturbed input $\overline{x}$.
The linear combination of the perturbed image with a weight vector and $\overline{x}$, 
$$w^{T}\overline{x} = w^{T}x + w^{T}\eta$$ is optimized by choosing $\eta=\epsilon sign(w)$. 
Therefore, a $\epsilon$ perturbation on each pixel of the image $x$ lead to
a total perturbation of magnitude $\epsilon m n$ after the linear combination, where 
$m$ is the average value of the weight $w$ across all dimensions and $n$ is the dimension
of $w$. 

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