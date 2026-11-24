---
layout: page
permalink: /activities/
title: Activities
class: activities
---

{:.hidden}
# Talks

# Talks and Presentations
{% assign talktitles = site.data.talks | group_by:"title" %}
{% for title in talktitles %}
{:.talk-title}
### {{ title.name }}
{% assign sorted_talks = title.items | sort: 'date' | reverse %}
{% for talk in sorted_talks  %}
  {% include talk.html talk=talk %}
{% endfor %}
{% endfor %}

# Services and Outreach

Participant in *Promoting Postdoc Progress (P3)* hosted by CITRAL. UCSB. (Spring 2026)\\
Organizer of *AMS 2026 Spring Eastern Sectional Meeting*. Boston, MA. (March 2026)\\
Participant in *ESCALA's Culturally Responsive Practices for STEM Faculty Teaching Latinx Students*. Online. (August, 2025)\\
Participant in *The Mathematics of Opportunity: Beyond Limits* hosted by Just Equations. Online. (Apr, 2025)\
Organizer of *Applied Math, PDE & Data Science Seminar*. UCSB. (Sep 2023 - Spring 2025)\\
Section Chair of *Southern California Applied Mathematics Symposium (SOCAMS)*. UCSD. (April 2024)\\
Organizer of *Applied & Computational Mathematics Seminar*. Dartmouth. (Sep 2020 - June 2021, Sep 2022 - June 2023)\\
Participant in *Research Mentor Training*. CIMER and Dartmouth. (May, 2023)\\
Section Chair of *SIAM Conference on Uncertainty Quantification*. Atlanta, GA. (April, 2022)\\
Selection Committee of *AWM Essay Contest on ``Biographies of Contemporary Women in Mathematics"*. Dartmouth. (Feb, 2022)\\
Hearing board of *Academic Honor and Conduct*. Dartmouth. (Winter 2021)



