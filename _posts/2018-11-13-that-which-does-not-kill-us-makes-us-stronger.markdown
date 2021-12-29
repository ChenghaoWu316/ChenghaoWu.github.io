---
layout: post
title:  How to desgin a data poster for color blindness?
date:   2019-11-13 15:01:35 +0300
image:  '/images/02.jpg'
tags:   [design, data_visualiztion]
---
Below is a video from my youtube channel, please like and subscribe :)
<p><iframe src="https://www.youtube.com/embed/J7LCT7Qe4Ws" frameborder="0" allowfullscreen></iframe></p>

Credit to Jeffrey Shaffer

The data-viz rule: “Don’t use red & green together.” The issue: "Ten percent of men are colorblind and mostly red/green issues." Reaction: "Don't use red and green together." Studies have shown that around 8% of men and 0.5% of women have color vision deficiency (CVD). This is more commonly referred to as colorblindness, although colorblindness is not the most accurate term. Having CVD does not mean that a person can’t see color unless you are the very rare person (one in 33,000 people) with achromatopsia. For the more common person with CVD, the key problem is that colors most people see as different will look the same. The two most common types of CVD are deuteranomaly and deuteranopia, which together count for about 6% of men, and protanomaly and protanopia, which account for another 2% (more information available at color-blindness.com). These conditions are also commonly referred to as “red weak” and “green weak” or “red-green colorblindness.” (Note: I will not discuss blue/yellow CVD because it is far less common.) Here are some tips for designing vizzes that are colorblind-friendly.


> Red and green together can be problematic, but they can sometimes be used together

<div class="gallery-box">
  <div class="gallery">
    <img src="/images/project-5.jpg" alt="Project">
  </div>
</div>

So indeed, using red and green together is a common problem. People with strong CVD (strong meaning a more severe condition of CVD) would see both red and green as brown. People with weak CVD can see strong red and green colors as red and green. However, this can still be problematic when the colors are weak or blended together. Keep in mind that being able to tell these colors apart is only an issue if color is the only encoding method used to make a distinct comparison—for example, a good number vs. a bad number in a table, or one line vs. another line in the same line chart. For example, in the chart below, color is needed to tell a good square from a bad square. Using deuteranope simulation, we can see how difficult this would be.

> Be aware that it’s not just red and green

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

> Use a colorblind-friendly palette when appropriate

One color used together in combination with another color is generally fine when one of them is not usually associated with CVD. For example, blue/orange is a common colorblind-friendly palette. Blue/red or blue/brown would also work. For the most common conditions of CVD, all of these work well, since blue would generally look blue to someone with CVD. Tableau has a built-in colorblind-friendly palette designed by Maureen Stone. This palette works very well for the common cases of CVD. Below is the Tableau colorblind-friendly palette under both deuteranope and protanope simulation. Notice how well this color palette works for the various comparisons of color.

<div class="gallery-box">
  <div class="gallery">
    <img src="/images/project-5.jpg" alt="Project">
  </div>
</div>

<div class="gallery-box">
  <div class="gallery">
    <img src="/images/project-5.jpg" alt="Project">
  </div>
</div>

Maybe it’s the boss, the client, or even the company colors or style guide that requires you to use red and green. So now what can we do?


> If you must use red and green together, leverage light vs. dark

For someone with CVD, the problem is primarily with color hue (e.g. red vs. green) and not with the color value (light vs. dark). Almost anyone can tell the difference between a very light color and a very dark color, so another option when using red and green together is to use a really light green, a medium yellow, and a very dark red. This would appear to be more of a sequential color scheme to someone who has strong CVD, but the person would at least be able to distinguish red from green based on light vs. dark.


> If you must use red and green together, offer alternate methods of distinguishing data

Along those same lines, if using red and green, you can also add icons, directional arrows, labels, annotations, or other indicators that would allow a person with CVD to see that something is bad (red) vs. good (green). Another option might be a checkbox for a user to switch the color palette for the entire viz to a colorblind-friendly palette. This allows for the red/green pairing for the majority of the audience while offering a way for someone with CVD to change the palette entirely. Unfortunately, there isn’t an easy way to do this in Tableau. However, it can certainly be done. Below are two examples, one using a parameter to change the color palette (using both a sequential and categorical color scheme with transparency) and the other using a dashboard action, similar to what Tableau Zen Master Robert Rouse used in his hidden-menu technique.


<div class='tableauPlaceholder' id='viz1640768668519' style='position: relative'>
<object class='tableauViz'  style='display:none;'>
<param name='host_url' value='https%3A%2F%2Fpublic.tableau.com%2F' />
<param name='embed_code_version' value='3' /> 
<param name='path' value='views&#47;ColorblindMapSwapper&#47;ColorSwapParameter?:embed=y&amp;:toolbar=yes&amp;:loadOrderID=0&amp;:display_count=yes&amp;:showTabs=y&amp;:tabs=yes' /> 
<param name='toolbar' value='yes' />
<param name='animate_transition' value='yes' />
<param name='display_static_image' value='yes' />
<param name='display_spinner' value='yes' />
<param name='display_overlay' value='yes' />
<param name='display_count' value='yes' /><param name='tabs' value='yes' />
<param name='showTabs' value='y' />
</object></div>               
<script type='text/javascript'>
var divElement = document.getElementById('viz1640768668519'); 
var vizElement = divElement.getElementsByTagName('object')[0];
vizElement.style.width='440px';vizElement.style.height='550px'; 
var scriptElement = document.createElement('script');   
scriptElement.src = 'https://public.tableau.com/javascripts/api/viz_v1.js';
vizElement.parentNode.insertBefore(scriptElement, vizElement); 
</script>


