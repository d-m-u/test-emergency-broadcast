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


svg {
  margin: 2em 0;
  font: 10px sans-serif;
}

.foreground {
  fill: #2D6A99;
}

.background {
  fill: #eee;
}

<script src="http://d3js.org/d3.v3.min.js" charset="utf-8"></script>

var n = 10, // how many bars?
    random = function() { return Math.floor(Math.random() * 100); }, // randomize some numbers for data
    data = d3.range(n).map(random); // an array of randomized datapoints

var barChart = {
  init: function() {
    this.height = 100;
    this.width = 220;
    this.padding = 12;
    this.el = "article header"; // where we'll put our svg 

    // calculate the bar width from the total chart width
    barWidth = Math.floor((this.width - (this.padding * (data.length - 1))) / data.length);
    barHeight = this.height - 20;


    this.svg = d3.select(this.el).insert('svg', ':first-child')
      .attr('width', this.width)
      .attr("height", this.height);

  }
}

var barChart = {

  init: function() { /***/ },

  // draw our svg container
  draw: function() {
    this.meters = this.svg
      .append("g")
        .attr("class", "meter")
        .selectAll("rect")
          .data(data)
          .enter()
          .append('g')
            .attr("class", "bar");

    this.drawBar().attr("class", "background").attr("y", 0).attr("height", barHeight);
    this.drawBar().attr("class", "foreground").attr("y", barHeight).attr("height", 0);
  },

  // this actually draws a bar
  drawBar: function () {
    var self = this;

    return this.meters.append("rect")
      .attr("x", function (d, i) {
        return i * (barWidth + self.padding);
      })
      .attr("width", barWidth);
  }
}

// initialize the bar chart!
barChart.init();
