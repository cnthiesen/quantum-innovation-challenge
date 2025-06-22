---
layout: page
title: Quantum Innovation Challenge
menu_title: Home
menu_icon: house-door
---
{% assign current_date = 'now' | date: "%Y-%m-%d" %}
{% assign event_start_date = site.event_start_date | date: "%Y-%m-%d" %}
{% assign event_close_date = site.event_close_date | date: "%Y-%m-%d" %}
{% assign registration_opens_date = site.registration_opens_date | date: "%Y-%m-%d" %}
{% assign registration_closes_date = site.registration_closes_date | date: "%Y-%m-%d" %}

{% if current_date < registration_opens_date %}
    {% assign registration_status = 'soon' %}
{% elsif current_date >= registration_opens_date and current_date <= registration_closes_date %}
    {% assign registration_status = 'open' %}
{% else %}
    {% assign registration_status = 'closed' %}
{% endif %}

{% if current_date < event_start_date %}
    {% assign event_status = 'soon' %}
{% elsif current_date >= event_start_date and current_date <= event_close_date %}
    {% assign event_status = 'now' %}
{% else %}
    {% assign event_status = 'over' %}
{% endif %}

{:.secondary}
# sponsored by the Novo Nordisk Foundation, Danish Business Authority and Danish Centre for AI Innovation - Gefion

<div class="aside">
    <h2><i class="bi bi-calendar3"></i> Event timeline</h2>
    <dl>
        {% if registration_status == "soon" or registration_status == "open" or registration_status == "demo" %}
            <dt>{{ site.registration_opens_date }}</dt>
            <dd>
                Applications open for participants<br>
                {% if registration_status == 'open' %}
                    <a href="{{ site.baseurl }}{% link registration.md %}" class="btn">Register now</a>
                {% elsif registration_status == 'closed' %}
                    <a class="btn disabled">Registration has closed</a>
                {% elsif registration_status == 'soon' %}
                    <a class="btn disabled">Registration opens soon</a>
                {% endif %}
            </dd>
        {% endif %}

        <dt>{{ site.registration_closes_date }}</dt>
        <dd>Applications close</dd>

        <dt>{{ site.event_date }}</dt>
        <dd>Quantum Innovation Challenge Final Projects Presentation</dd>
    </dl>
</div>

{% if event_status != "over" %}

With the emergence of near term intermediate quantum computers and quantum-inspired algorithms powered by GPUs, it is important to understand their strengths and weaknesses, reduce the barrier to use, and adapt them for pharmaceutical development apart from drug discovery (e.g. docking and binding analysis).
The Bio Innovation Institute (BII), Molecular Quantum Solutions (MQS), Novo Nordisk, QAI Ventures and Roche are hosting the virtual quantum challenge for researchers all over the world to work collaboratively in teams on projects. 

Researchers can propose projects with respect to this year's [challenge topic](_/../projects.md) applying quantum computing and quantum-inspired algorithms to existing benchmarks, developing new benchmarks involving quantum computing methods, creating sub-aglorithms based on quantum computing methods, proposing quantum computing based sampling and optimization methods, and more.
After the challenge, results will be collated and secured under open-source and free license agreements (Apache/MIT) in the dedicated Quantum-Challenge-2025 repository.

[This opportunity](_/../registration.md) is open to researchers at all levels who are interested in quantum computing for better informed pharmaceutical development in the low data regime.
Prior programming experience is required and basic familiarity with git and GitHub.
Training and orientation resources are available on the [resources page](_/../resources.md).

## Logistics

([Element](https://) for ongoing comms, especially for the participants to find other team members.

Questions via email can be sent to quantum_challenge@mqs.dk during the two weeks Q&A phase and will be collectively answered via the Q&A page.

## Outputs

By the end of the event, we hope you will have formed new connections, learned new skills, and been inspired with new ideas!

{% else %}

With the completion of the BII Quantum Challenge 2025, we thank participants for exploring, collaborating, innovating, and contributing to the advancement of quantum computing and quantum-inspired methods for pharmaceutical development.

During the hackathon, researchers had the opportunity to develop with a use-case example provided by Novo Nordisk.

Although the event has concluded, the outputs from the quantum challenge, including applied and developed algorithms, benchmarks, etc. will continue to serve as valuable resources for the research community. Outputs from teams that have participated  are available at [https://github.com/BII-Quantum/Quantum-Challenge-2025](https://github.com/BII-Quantum/Quantum-Challenge-2025).

We want to express our gratitude to all the participants for their contributions, and we look forward to future collaborations.
{% endif %}

## Prizes

{% if event_status != "over" %}

Gefion access has been given to the five highest-ranked projects [agenda](_/../agenda.md).


{% else %}
Five teams will be selected for their outstanding contributions during the phase 1 of the challenge and will receive access to Gefion during phase 2! The top-ranked projects from the showcase and judging session will be highlighted here:

| Rank | Project #                                            | Team Name | Project Name |
| ---  | ---------------------------------------------------- | --------- | ------------ |
| 1st  | [Project xx](https://bii-quantum.github.io/projects) |           |              |
| 2nd  | [Project xx](https://bii-quantum.github.io/projects) |           |              |
| 3rd  | [Project xx](https://bii-quantum.github.io/projects) |           |              |
| 4th  | [Project xx](https://bii-quantum.github.io/projects) |           |              |
| 5th  | [Project xx](https://bii-quantum.github.io/projects) |           |              |

For a full list of the challenge projects, we encourage you to check out the [projects page](_/../projects.md).

{% endif %}

## Sponsors

- [Novo Nordisk Foundation](https://novonordiskfonden.dk/)
- [Danish Business Authority](https://danishbusinessauthority.dk/)
- [Danish Centre for AI Innovation - Gefion](https://dcai.dk/)

## Hosts

<div style="display: flex; align-items: center; justify-content: center;">
    <a href="https://bii.dk/">
        <img src="https://mva.org/wp-content/uploads/2019/03/BII_Logo_Petroleum_RGB.png" alt="BioInnovation Institute" style="width:400px; margin-right: 20px;">
    </a>
    <a href="https://mqs.dk">
        <img src="https://mqs.dk/Images/Logo/MQS_Logo_Text_black.png" alt="Molecular Quantum Solutions (MQS)" style="width:500px; margin-left: 20px;">
    </a>
</div>

## Prize Sponsor

<div style="display: flex; align-items: center; justify-content: center;">
    <a href="https://danishbusinessauthority.dk/">
        <img src="https://stateofgreen.com/en/wp-content/uploads/2018/05/profile_logo_6283_460x160-4-240x83.png" alt="Danish Business Authority" style="width:200px;">
    </a>
</div>

[faq]: {{ site.baseurl }}{% link faq.md %}
