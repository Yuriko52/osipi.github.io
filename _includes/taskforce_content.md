{% assign taskforce = site.data.tf[page.tf] %}

### Task force aims

{{ taskforce.aims }}

---

### Task force description

{{ taskforce.description }}

<!-- SUBGROUPS -->
{% if taskforce.subgroups %}
---
{% include taskforce/subgroups.md subgroups=taskforce.subgroups %}
{% endif %}

<!-- LEADS -->
{% if taskforce.leads %}
---
### Task force leads

{% include taskforce/leads.md leads=taskforce.leads %}
{% endif %}

<!-- MEMBERS -->
{% if taskforce.members %}
---
### Task force members 

{% include taskforce/members.md members=taskforce.members %}
{% endif %}

<!-- Status -->
{% if taskforce.status %}
---
### Task force status  

<ul>
{% for status in taskforce.status %}
    <li> {{ status }} </li> 
{% endfor %}
</ul>
{% endif %}

<!-- Links -->
{% if taskforce.links %}
---

### Task force members links

{% include taskforce/links.md links=taskforce.links %}
{% endif %}

<!-- Resources -->
{% if taskforce.resources %}
---

### Public resources

{% include taskforce/links.md links=taskforce.resources %}
{% endif %}