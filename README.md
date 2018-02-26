# test-emergency-broadcast

##### it's just a stupid place to play with markdown for miq blogs

this [goes here]
foo [stuff here][1] [1a]

[goes here]: other.md
[1]: other.md
[1a]: www.google.com

[here](https://www.youtube.com/embed/O05SBdpl7Gc)

(<iframe width="560" height="315" src="https://www.youtube.com/embed/O05SBdpl7Gc" frameborder="0" allowfullscreen></iframe>)




    <iframe src="/mbostock/raw/4061502/0a200ddf998aa75dfdb1ff32e16b680a15e5cb01/" marginwidth="0" marginheight="0" scrolling="no"></iframe>

http://www.nicksuch.com/2014/03/26/d3-sample/

<script src="https://cdnjs.cloudflare.com/ajax/libs/vis/4.15.0/vis.min.js" type="text/javascript"></script><link rel="https://cdnjs.cloudflare.com/ajax/libs/vis/4.15.0/vis.min.css"></link>


<details>
<summary>How do I dropdown?</summary>
<br>
This is how you dropdown.
<details>


<li class="dropdown">
  <a href="#" class="dropdown-toggle" data-toggle="dropdown" role="button" aria-expanded="false">Posts <span class="caret"></span></a>
  <ul class="dropdown-menu" role="menu">
    {% for p in site.posts %}
      {% include menu_item.html %}
    {% endfor %}
  </ul>
</li>

Hello! I'm a **<mkp-blue>blue</mkp-blue>** word in a regular markdown text!
