---
layout: page
title: People
permalink: /people/
comments: true
---

{% include 2018-elections.html %}

### 2018 Election
#### Primary Candidates
{% assign person = site.data.2018.primary.candidates | sort:'last_name' %}
<table>
<thead>
  <th>First Name</th>
  <th>Last Name</th>
  <th>Candidate for</th>
  <th>City</th>
  <th>County</th>
</thead>
<tbody>
{% for member in person  %}
  <tr>
    <td><a href="{{member.id}}">{{member.first_name}}</a></td>
    <td><a href="{{member.id}}">{{member.last_name}}</a></td>
    <!-- <td><a href="{{member.id}}">{{member.first_name}}&nbsp;{{member.last_name}}</a></td> -->
    <td>{{ member.office }}</td>
    <td><a href="../places/{{ member.county | downcase | replace: ' ','-' }}/{{ member.city | downcase | replace: ' ','-' }}">{{ member.city }}</a></td>
    <td><a href="../places/{{ member.county | downcase | replace: ' ','-' }}">{{ member.county }}</a></td>
  </tr>
{% endfor %}
</tbody>
</table>

<br><br>
### 2017 Municipal Election
#### Primary Candidates
{% assign person = site.data.2017.primary.candidates | sort:'name' %}
<table>
<thead>
  <th>Name</th>
  <th>Candidate for</th>
  <th>City</th>
  <th>County</th>
</thead>
<tbody>
{% for member in person  %}
  <tr>
    <td><a href="{{member.id}}">{{member.name}}</a></td>
    <td>{{ member.body }}</td>
    <td><a href="../places/{{ member.county | downcase | replace: ' ','-' }}/{{ member.city | downcase | replace: ' ','-' }}">{{ member.city }}</a></td>
    <td><a href="../places/{{ member.county | downcase | replace: ' ','-' }}">{{ member.county }}</a></td>
  </tr>
{% endfor %}
</tbody>
</table>
