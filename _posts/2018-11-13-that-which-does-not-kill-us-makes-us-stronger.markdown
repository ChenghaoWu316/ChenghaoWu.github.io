---
layout: post
title:  How to desgin a data poster for color blindness?
date:   2019-11-13 15:01:35 +0300
image:  '/images/02.jpg'
tags:   [design, data_visualiztion]
---
The data-viz rule: “Don’t use red & green together.” The issue: "Ten percent of men are colorblind and mostly red/green issues." Reaction: "Don't use red and green together." Studies have shown that around 8% of men and 0.5% of women have color vision deficiency (CVD). This is more commonly referred to as colorblindness, although colorblindness is not the most accurate term. Having CVD does not mean that a person can’t see color unless you are the very rare person (one in 33,000 people) with achromatopsia. For the more common person with CVD, the key problem is that colors most people see as different will look the same. The two most common types of CVD are deuteranomaly and deuteranopia, which together count for about 6% of men, and protanomaly and protanopia, which account for another 2% (more information available at color-blindness.com). These conditions are also commonly referred to as “red weak” and “green weak” or “red-green colorblindness.” (Note: I will not discuss blue/yellow CVD because it is far less common.) Here are some tips for designing vizzes that are colorblind-friendly.


> 1. Red and green together can be problematic, but they can sometimes be used together

<div class="gallery-box">
  <div class="gallery">
    <img src="/images/project-5.jpg" alt="Project">
  </div>
</div>

So indeed, using red and green together is a common problem. People with strong CVD (strong meaning a more severe condition of CVD) would see both red and green as brown. People with weak CVD can see strong red and green colors as red and green. However, this can still be problematic when the colors are weak or blended together. Keep in mind that being able to tell these colors apart is only an issue if color is the only encoding method used to make a distinct comparison—for example, a good number vs. a bad number in a table, or one line vs. another line in the same line chart. For example, in the chart below, color is needed to tell a good square from a bad square. Using deuteranope simulation, we can see how difficult this would be.

> 2. Be aware that it’s not just red and green
Many data visualization tools have a “stoplight” palette built into them, and there are many companies (and clients and bosses) that still insist on using the stoplight palette. With all the talk of stoplight colors and the nicknames for the CVD conditions, it’s no wonder that the data visualization rule has simply become “don’t use red and green.” Below is a simulation of Tableau’s stoplight colors using protanope simulation.

<div class="gallery-box">
  <div class="gallery">
    <img src="/images/project-5.jpg" alt="Project">
  </div>
</div>

Notice that the problem here is much more complex than just simply red vs. green. Since red, green, and orange all appear to be brown for someone with strong CVD, it would be more accurate to say, “Don't use red/green/brown/orange together.” However, it doesn’t end there. When colors are mixed, they can also be problematic. One color combination that is frequently overlooked is using blue and purple together. In an RGB color model, purple is achieved by using blue and red together. If someone has issues with red, then the person may also have issues with purple, which would appear to look like blue. Also, pink and gray together and gray and brown together can be problematic. Below is the Tableau 10 color palette using a deuteranope simulation. Not only are red, green, and brown problematic but so are blue and purple, pink and gray, and gray and brown.

<div class="gallery-box">
  <div class="gallery">
    <img src="/images/project-5.jpg" alt="Project">
  </div>
</div>

My brother-in-law has CVD, so he is frequently the guinea pig for my color experiments. Off all of the things I’ve tested on him, the combination of colors on the image below (left) was the hardest for him to distinguish. He seems to suffer from protanopia, which is simulated below on the right.

<div class="gallery-box">
  <div class="gallery">
    <img src="/images/project-5.jpg" alt="Project">
  </div>
</div>

So now that we know there are many more combinations of color that can be problematic, what should we do?


<p><iframe src="https://www.youtube/embed/J7LCT7Qe4Ws" frameborder="0" allowfullscreen></iframe></p>


Qua ex cognitione facilior facta est investigatio rerum occultissimarum. Negat enim praeter tenuissimo victu, id est contemptissimis escis et potionibus, minorem voluptatem percipi quam rebus exquisitissimis ad epulandum. Non enim iam stirpis bonum quaeret, sed ista animalis. Qui autem esse poteris, nisi te amor ipse ceperit? Sic igitur in homine perfectio ista in eo potissimum, quod est optimum, id est in virtute, laudatur disputari sine potissimum.

Sin tantum modo ad indicia veteris memoriae cognoscenda, curiosorum. Haec et tu ita posuisti, et verba vestra sunt. Idemne potest esse dies saepius, qui semel fuit. Ampulla enim sit necne sit, quis non iure optimo irrideatur, si laboret? Ego vero volo in virtute vim esse quam maximam; Serpere anguiculos, nare anaticulas, evolare merulas, cornibus uti videmus boves, nepas aculeis. Archytam? Qua ex cognitione facilior facta est investiga.