---
layout: default
meta-description: "Seminar series on the frontier of machine learning and systems. Livestreamed every Thursday, 1:30-2:30 pm PT."
---

# Stanford MLSys Seminar Series

**News**:
* We are now available in podcast form on [Apple Podcasts](https://podcasts.apple.com/us/podcast/stanford-mlsys-seminar/id1603927994), [Spotify](https://open.spotify.com/show/3NazVHl6ujGuHCjGlN0SCf), and [Google](https://podcasts.google.com/feed/aHR0cHM6Ly9hbmNob3IuZm0vcy83YmRkMzMxNC9wb2RjYXN0L3Jzcw)!
* Stanford students, check out [CS 528](/cs528), a new course at Stanford running this fall!
* Our talks this semester are Thursdays 1:30 PM PT!
* Join our [email list](https://groups.google.com/forum/#!forum/stanford-mlsys-seminars/join) to get notified of the speaker and livestream link every week! 

Machine learning is driving exciting changes and progress in computing.
What does the ubiquity of machine learning mean for how people build and deploy
systems and applications?
What challenges does industry face when deploying machine learning systems in
the real world, and how can academia rise to meet those challenges?

In this seminar series, we want to take a look at the frontier of machine
learning systems, and how machine learning changes the modern programming
stack.
Our goal is to help curate a curriculum of awesome work in ML systems to help
drive research focus to interesting questions.

We started livestreaming each talk in this seminar series every week on [YouTube](https://www.youtube.com/channel/UCzz6ructab1U44QPI3HpZEQ)
in Fall 2020, and we've been going strong ever since!
Every week we take questions from the live chat, and keep videos of the talks
available on YouTube afterwards as well.
Give our channel a follow, and tune in every week for an exciting discussion!

Read about our [motivation for starting this seminar](https://hazyresearch.stanford.edu/blog/2020-10-13-mlsys).

Check out our introductory video:
<iframe width="560" height="315" src="https://www.youtube.com/embed/OEiNnfdxBRE" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

<!-- Read our blog post on our [why we're running this seminar]({{ site.baseurl }}/about). -->

{% for category in site.data.talks %}
# {{ category.type }}
<div class="talk-list">
  {% for talk in category.members %}
  <div class="talk list-group-item">
  <div class="talk-date">{{ talk.date }}</div>
  <div class="talk-presenter">{{ talk.speaker }}</div>
  {% if talk.title %}
  <div>
    {% if talk.recording %}
      <span><a class="talk-title-link" href="{{ talk.recording }}">{{ talk.title }} <i class="bi bi-box-arrow-up-right"></i></a></span>
    {% elsif talk.livestream %}
      <span><a class="talk-title-link" href="{{ talk.livestream }}">{{ talk.title }} <i class="bi bi-box-arrow-up-right"></i></a></span>
    {% else %}
      <span>{{ talk.title }}</span>
    {% endif %}
  </div>
  {% endif %}
  {% if talk.abstract %}
    <details>
    <summary>Abstract</summary>
    {{ talk.abstract }}
    
    {% if talk.bio %}
    <br><br>
    <strong>Bio: </strong> {{ talk.bio }}
    {% endif %}

    {% if talk.recording %}
      <br><br>
      <strong><a href="{{ talk.recording }}">Video Link</a></strong>
    {% elsif talk.livestream %}
      <br><br>
      <strong><a href="{{ talk.livestream }}">Livestream Link</a></strong>
    {% endif %}
    </details>
  {% endif %}
  </div>
  {% endfor %}
</div>
{% endfor %}

# About The Seminar

**Seminar Hosts:** Dan Fu, Karan Goel, Fiodar Kazhamakia, Piero Molino.

**Executive Producers:** Matei Zaharia, Chris Ré.

You can reach us at sysmlstanfordseminar [at] gmail.

Source code for this website can be found [here](https://github.com/stanford-sysml-seminar/stanford-sysml-seminar.github.io).

<!-- Please uncomment this part if you clone our source code! -->
<!--
Website template from the [Stanford MLSys Seminar Series](https://mlsys.stanford.edu).
-->
