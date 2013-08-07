---
layout: page
title:
tagline: vijay's quantumchemistry blog
---
{% include JB/setup %}

--------------------------------------------------------------------------------
> Si, abbiamo un anima. Ma e fatta di tanti piccoli robot.
>
> Yes, we have a soul. But it's made of lots of tiny robots. —Giulio Giorelli
--------------------------------------------------------------------------------

A PhD student at the [LCPQ/IRSAMC](http://www.lcpq.ups-tlse.fr) working on
the problems of Quantum Chemistry.

I have a few demonstrations on some simple physical/quantum mechanical ideas,
Fork me on [github](http://github.com/vijaygopalchilkuri)

I have another blog on my Raspberry Pi at home :
[Pi](http:109.21.246.125)

See my [About](./About.html) page for details.

{% for category in site.categories %}
  <h2 id="{{ category[0] }}-ref">{{ category[0] | join: "/" }}</h2>
  <ul>
    {% assign pages_list = category[1] %}
    {% include JB/pages_list %}
  </ul>
{% endfor %}
