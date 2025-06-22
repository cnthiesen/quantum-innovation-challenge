---
title: About the Quantum Innovation Challenge
menu_title: About
menu_icon: globe2
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

{% if event_status != "over" %}
The Quantum Innovation Challenge is a virtual competition and organised by the [Bio Innovation Institute (BII)](https://), [Molecular Quantum Solutions (MQS)](https://mqs.dk), [QAI Ventures](https://).
The competition is open to researchers and industrial participants at all levels who are interested in applying quantum computing and quantum-inspired algorithms to pharmaceutical development.
{% else %}
The Quantum Innovation Challenge was a hosted on {{ site.event_date }}, organised by the [Bio Innovation Institute (BII)](https://), [Molecular Quantum Solutions (MQS)](https://mqs.dk), [QAI Ventures](https://).
The event included researchers and industrial participants at all levels who are interested in applying quantum computing and quantum-inspired algorithms to pharmaceutical development.
{% endif %}

### The organizing team

<!-- {:.lead}
To contact us about the quantum challenge, please contact us via mail. -->

<table class="team-list">
    <tr>
        <td>
            <img alt="Mark Nicholas Jones" src="https://avatars.githubusercontent.com/u/61972059?v=4">
        </td>
        <td>
            <strong>Mark Nicholas Jones</strong>
            <span class="profile-links">
                <a title="Profile &amp; contact" href=""><i class="bi bi-person-lines-fill"></i></a>
                <a title="Website" href="https://mqs.dk/"><i class="bi bi-globe2"></i></a> 
                <a title="GitHub" href="https://github.com/sgbaird"><i class="bi bi-github"></i></a>
                <a title="LinkedIn" href=""><i class="bi bi-linkedin"></i></a>
            </span>
            <br>Molecular Quantum Solutions (MQS)
            <br>CEO/CTO
        </td>
    </tr>
    <tr>
        <td>
            <img alt="Francesco Russo" src="...">
        </td>
        <td>
            <strong>Francesco Russo</strong>
             <span class="profile-links">
                <a title="Website" href="..."><i class="bi bi-globe2"></i></a>
                <a title="GitHub" href="..."><i class="bi bi-github"></i></a>
                <a title="LinkedIn" href="..."><i class="bi bi-twitter"></i></a>
            </span>
            <br>Novo Nordisk Foundation
            <br>Scientific Manager
        </td>
    </tr>
    <tr>
        <td>
            <img alt="Cathal Mahon" src="...">
        </td>
        <td>
            <strong>Cathal Mahon</strong>
            <span class="profile-links">
                <a title="Website" href="..."><i class="bi bi-globe2"></i></a>
                <a title="GitHub" href="..."><i class="bi bi-github"></i></a>
                <a title="LinkedIn" href="..."><i class="bi bi-twitter"></i></a>
            </span>
            <br>Bio Innovation Institute
            <br>Chief Business Officer
        </td>
    </tr>
    <!--
    <tr>
        <td>
            <img alt="KJ Schmidt" src="../assets/kj.jpeg">
        </td>
        <td>
            <strong>KJ Schmidt</strong>
            <span class="profile-links">
                <a title="Website" href="http://kjschmidt.us/"><i class="bi bi-globe2"></i></a>
                <a title="GitHub" href="https://github.com/kjschmidt913"><i class="bi bi-github"></i></a>
                <a title="Twitter" href="https://twitter.com/kj_schmidt"><i class="bi bi-twitter"></i></a>
            </span>
            <br>University of Chicago/Argonne National Lab
            <br>Research Scientist
        </td>
    </tr>
        <tr>
        <td>
            <img alt="Ari Scourtas" src="../assets/ari.JPG">
        </td>
        <td>
            <strong>Aristana Scourtas</strong>
            <span class="profile-links">
                <a title="GitHub" href="https://github.com/ascourtas"><i class="bi bi-github"></i></a>
                <a title="Twitter" href="https://twitter.com/aristana_s"><i class="bi bi-twitter"></i></a>
            </span>
            <br>University of Chicago/Argonne National Lab
            <br>Research Scientist
        </td>
    </tr> -->
</table>

### Acknowledgements

We thank Sterling G. Baird, and the rest of the organizing team for the [Bayesian Optimization Hackathon for Chemistry and Materials](https://github.com/AC-BO-Hackathon/ac-bo-hackathon.github.io) which has built on top of the [LLMs in Materials and Chemistry '23 Hackathon](https://materials-data-facility.github.io/llm-hackathon/).
