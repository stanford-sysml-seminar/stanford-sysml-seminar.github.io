---
layout: default
meta-description: "Seminar series on the frontier of machine learning and systems."
---

# Stanford MLSys Seminar

**News**:
* In late 2023, we're partnering with [CS 229s](https://cs229s.stanford.edu/fall2023/), Systems for Machine Learning, and CS 528 to offer a special **systems for machine learning limited series**! We'll have talks on Mondays, 10:30-11:30 am PT. Stanford students can sign up for either class!
* In early 2023, we partnered with [CS 324](https://stanford-cs324.github.io/winter2023/), Advances in Foundation Models, to offer a special **foundation models limited series**! We had talks on certain Mondays and Wednesdays, 3:30-4:20 PM PT (see schedule below).
* Join our [email list](https://groups.google.com/forum/#!forum/stanford-mlsys-seminars/join) to get notified of the speaker and livestream link every week!.

## Systems for Machine Learning Limited Series
{% for category in site.data.talks_229s %}
### {{ category.type }}
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

## About the MLSys Seminar

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

## Foundation Models Limited Series

In early 2023 (Stanford winter quarter), we're excited to partner with CS 324 to offer a special foundation model limited series!
We have an exciting slate of speakers from OpenAI, Google, Anthropic, Meta and more -- the experts who are developing and deploying foundation models in practice.
Tune in and be sure not to miss it!

{% for category in site.data.talks_fm %}
### {{ category.type }}
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

{% for category in site.data.talks %}
## {{ category.type }}
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

**Seminar Hosts:** Simran Arora, Dan Fu.

**Guest Hosts (2023 Foundation Models Limited Series)**: Avanika Narayan, Michael Zhang, Percy Liang, Tatsu Hashimoto.

**Executive Producer:** Chris Ré.

**Alumni:**
* Karan Goel (co-host, 2020-2023)
* Fiodar Kazhamakia (co-host, 2020-2022)
* Piero Molino (co-host, 2020-2022)
* Matei Zaharia (executive producer, 2020-2022)

From Fall 2021-Spring 2022, we ran the MLSys seminar alongside [CS 528](/cs528).

You can reach us at sysmlstanfordseminar [at] gmail.

If you'd like to clone this website for your own talk series, source code can be found [here](https://github.com/stanford-sysml-seminar/stanford-sysml-seminar.github.io).

<!-- Please uncomment this part if you clone our source code! -->
<!--
Website template from the [Stanford MLSys Seminar Series](https://mlsys.stanford.edu).
-->
