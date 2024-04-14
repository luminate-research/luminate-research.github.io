---
layout: default
---

<!-- Thanks to their generative capabilities, large language models (LLMs) have become an invaluable tool for creative processes. These models have the capacity to produce hundreds and thousands of visual and textual outputs, offering abundant inspiration for creative endeavors. But are we harnessing their full potential? We argue that current interaction paradigms fall short, guiding users towards rapid convergence on a limited set of ideas, rather than empowering them to explore the vast latent design space in generative models. To address this limitation, we propose a framework that facilitates the structured generation of design space in which users can seamlessly explore, evaluate, and synthesize a multitude of responses. We demonstrate the feasibility and usefulness of this framework through the design and development of an interactive system, Luminate, and a user study with 14 professional writers. Our work advances how we interact with LLMs for creative tasks, introducing a way to harness the creative potential of LLMs. -->

<!-- <br/> -->

<p style="text-align: center; font-size: 1.2rem">
  <displayquote>
    "<i>if you want to have good ideas, you must <strong>have lots of ideas</strong> <br>and
    learn to <strong>throw away the bad ones</strong></i>"
    <br>
    - Linus Pauling -
  </displayquote>
</p>

<div class="gif-container">
  <img src="assets/gif/fixation.gif">
</div>

<p>
  <span class="highlight">Creative processes</span> typically begin with generating and exploring multiple ideas rather than refining a single one. Without first exploring diverse ideas, one can hastily converge on a suboptimal idea and spend time iterating it without considering other options. This is known as <span class="highlight">fixation</span>, a phenomenon that hinders creative processes.
</p>

<div class="gif-container">
  <img src="assets/gif/design-space-thinking.gif">
</div>

<p>
  Another key to success in creative processes is being able to think about the space of possible ideas — referred to as <span class="highlight">design space thinking</span>. 
</p>

<div class="gif-container">
  <img src="assets/gif/llm-for-creativity.gif">
</div>

<p>
  Today, <span class="highlight">large language models (LLMs) offer an unprecedented opportunity to support these needs</span>. Specifically, the capacity to instantly produce tens to hundreds of outputs empowers them to address fixation by offering users a set of ideas different from the current set of ideas. Moreover, they can generate diverse ideas to reveal the design space to users. <span class="highlight">However, current user interaction paradigms for LLMs do not fully harness this potential</span>.
</p>

<hr>

<p style="text-align: center">
  <span class="highlight"><i>Prompting for Design Space</i></span><br>(Structured Multi-Output Approach)
</p>

<div class="img-container">
  <img src="assets/img/framework-comparison.png">
</div>

<p>
  The current interaction paradigm with LLMs — prompt engineering — constrains us to generating a <i>single</i> output and then iterating on it. This is illustrated in the figure below as the (A) <span class="highlight">Unstructured Single-Output</span> approach. Another approach found in recent work that generates <i>multiple</i> outputs from a single prompt is referred to as the (B) <span class="highlight">Unstructured Multi-Output</span> approach.
</p>

<p>
  We propose the (C) <span class="highlight">Structured Multi-Output</span> approach, where <i>structured</i> denotes the presence of <strong>dimensions</strong> relevant to the task/domain to guide the response generation and <i>unstructured</i> their absence.
</p>

<p style="text-align: center">
  <i>What do we mean by <strong>dimensions</strong> and why do we need <strong>them</strong>?</i>
</p>

The figure below provides an example that shows the benefits of exposing <span class="highlight">design space</span> to users and how <strong>dimensions</strong> can assist this. 

<div class="img-container">
  <img src="assets/img/framework-example.png">
</div>


<p>
  By generating relevant <span class="highlight">dimensions</span> for a task or topic, we can inform users about many dimensions and [values] they can consider — e.g., plot complexity: [linear, twisting, ...], genre: [fantasy, adventure, ...]. If all the possible dimensions and values are used to generate responses, the responses will cover many sub-spaces within the overall <span class="highlight">design space</span> and reveal to users a space of possible responses they can generate with LLMs.
</p>

We introduce <img src="assets/favicon/luminate-icon.png"/><span class="sys-name">Luminate</span>, an interactive system that uses our <i>Prompting for Design Space</i> framework to enable structured generation and exploration of design space with LLMs.

## Video Demo

<!-- See <img src="assets/favicon/luminate-icon.png"/><span class="sys-name">Luminate</span> in action in this Video Demo. -->

{% if site.video %}
<div class="video-wrapper">
  <iframe src="{{site.preview}}&color=white&rel=0&modestlogo=1" id="yt-video" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
</div>
{% endif %}

<!-- {% if site.video %}
<div class="video-wrapper">
  <iframe src="{{site.video}}&color=white&rel=0&modestlogo=1" id="yt-video" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
</div>
{% endif %} -->

------

## Bibtex
<pre>
 @inproceedings{suh2024luminate,
   title = {Luminate: Structured Generation and Exploration of Design Space with Large Language Models for Human-AI Co-Creation},
   author = {Suh, Sangho and Chen, Meng and Min, Bryan and Li, Toby Jia-Jun and Xia, Haijun},
   booktitle = {Proceedings of the 2024 CHI Conference on Human Factors in Computing Systems},
   pages = {1--26},
   year = {2024},
   url = {https://doi.org/10.1145/3613904.3642400},
   doi = {10.1145/3613904.3642400}
 }
</pre>
