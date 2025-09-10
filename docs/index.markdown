---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: default
items:
  - title: CompanionManager
    desc: Radial menu for summoning companions.
  - title: GuildAlts
    desc: Manage guild alts and shows main character for alts in chat.
  - title: GuildRecipes
    desc: Share and view tradeskill recipes with your guild.
  - title: KillTrack
    desc: Tracks all your kills.
  - title: TitleRotator
    desc: Rotates your titles every few seconds.
  - title: TurtleCalendar
    desc: In-game calendar showing you raid & instances lockout, battleground and Darkmoon faire timers.
  - title: TurtleMail
    dl: https://github.com/sica42/TurtleMail/archive/refs/heads/master.zip
    desc: Automatically opens mail, mail multiple items, autocomplete recipient names, shows collected gold.
  - title: RaidCalendar
    desc: In-game raid calendar where you can signup and register SR items in-game.
  - title: RollFor
    repo: roll-for-vanilla
    dl: https://github.com/sica42/roll-for-vanilla/releases/download/latest/RollFor.zip
    desc: An addon that automates rolling for items for vanilla WoW.
  - title: Speedometer
    desc: Shows your current running speed.
---


<h1>{{ site.title | default: site.github.repository_name }}</h1>
<p>{{ site.description | default: site.github.project_tagline }}</p>

## Addons

{% for item in page.items %}
| <a class="download" title="Download" href="{% if item.dl %}{{ item.dl }}{% else %}https://github.com/sica42/{{ item.title }}/archive/refs/heads/main.zip{% endif %}"></a><a class="github" title="Github page" href="https://github.com/sica42/{{ item.repo | default: item.title }}"><a href="./{{ item.title }}">{{ item.title }}</a> | {{ item.desc }}|{% endfor %}
