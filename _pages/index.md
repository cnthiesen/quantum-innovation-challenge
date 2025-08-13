---
layout: page
title: Home
menu_title: Home
menu_icon: house-door
permalink: /
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

<!--
<div style="display: flex; align-items: left; justify-content: left;">
    <img src="./assets/Cover_Image.png" alt="Cover Image" style="widt:300px;">
</div> -->

<section class="py-24 lg:pt-32 pb-24 flex max-w-screen-lg mx-auto text-center items-center justify-center px-5">
  <div class="flex-1 gap-4 flex flex-col">
    <h1 class="font-space-mono text-4xl font-bold">Quantum Innovation Challenge 2025</h1>
    <p class="tracking-[1px] font-space-mono text-xl">The Quantum Innovation Challenge 2025 invites researchers, start-ups, and students from around the world to explore how quantum computing and quantum-inspired algorithms can advance (bio)pharmaceutical innovation – offering selected teams exclusive access to the Gefion AI Supercomputer.</p>
  </div>
</section>

<section class="flex flex-col mx-auto text-center items-center justify-center mb-12 border-electron/25 py-10">
  <p class="text-white/50 text-sm uppercase tracking-[1px] text-lg font-space-mono px-5 ">
    A joint innovation challenge partnership between
  </p>
  
  <!-- Partner Grid -->
  <div class="w-full px-5 border-electron/25">
  <div class="grid grid-cols-2 sm:grid-cols-3 md:grid-6 lg:grid-cols-5 xl:grid-cols-9 gap-8 md:gap-10 lg:gap-12 xl:gap-8 py-4 place-items-center w-full max-w-7xl mx-auto items-center justify-center ">
    <div class="flex justify-center items-center h-16 w-full">
      <img src="{{ "/assets/partners/nnf.svg" | relative_url}}" alt="Novo Nordisk Foundation" class="svg h-12 w-auto max-w-full object-contain brightness-0 invert transition-all ">
    </div>
    <div class="flex justify-center items-center h-16 w-full">
      <img src="{{ "/assets/partners/bii.svg" | relative_url}}" alt="BII" class="svg h-12 w-auto max-w-full object-contain brightness-0 invert transition-all ">
    </div>
    <div class="flex justify-center items-center h-16 w-full">
      <img src="{{ "/assets/partners/nh.svg" | relative_url}}" alt="NH" class="svg h-12 w-auto max-w-full object-contain brightness-0 invert transition-all ">
    </div>
    <div class="flex justify-center items-center h-16 w-full">
      <img src="{{ "/assets/partners/mqs.svg" | relative_url}}" alt="MQS" class="svg h-12 w-auto max-w-full object-contain brightness-0 invert transition-all ">
    </div>
    <div class="flex justify-center items-center h-16 w-full">
      <img src="{{ "/assets/partners/dcai.svg" | relative_url}}" alt="DCAI" class="svg h-12 w-auto max-w-full object-contain brightness-0 invert transition-all ">
    </div>
    <div class="flex justify-center items-center h-16 w-full">
      <img src="{{ "/assets/partners/qai.svg" | relative_url}}" alt="QAI" class="svg h-12 w-auto max-w-full object-contain brightness-0 invert transition-all ">
    </div>
    <div class="flex justify-center items-center h-16 w-full">
      <img src="{{ "/assets/partners/dba.svg" | relative_url}}" alt="DBA" class="svg h-12 w-auto max-w-full object-contain brightness-0 invert transition-all ">
    </div>
    <div class="flex justify-center items-center h-16 w-full">
      <img src="{{ "/assets/partners/erhvervsstyrelsen.svg" | relative_url}}" alt="Erhvervsstyrelsen" class="svg h-12 w-auto max-w-full object-contain brightness-0 invert transition-all ">
    </div>
    <div class="flex justify-center items-center h-16 w-full">
      <img src="{{ "/assets/partners/icd.svg" | relative_url}}" alt="ICD" class="svg h-12 w-auto max-w-full object-contain brightness-0 invert transition-all ">
    </div>
  </div>
  </div>
</section>



<section class="border-t-1 border-electron/25 ">
<div class="flex items-start max-w-screen-xl mx-auto gap-10"> 
<div class="flex-1 py-16 w-full lg:w-auto px-5" id="left-content">
<div class="max-w-screen-lg! mx-auto prose-wrapped prose">

<h2> Accelerating Quantum Applications in the Life Sciences</h2>

<p>The Quantum Innovation Challenge 2025 invites researchers, start-ups, and students from around the world to explore how quantum computing and quantum-inspired algorithms can advance (bio)pharmaceutical innovation – offering selected teams exclusive access to the Gefion AI Supercomputer.</p>

<p>With the emergence of near-term quantum computers and powerful GPU-based methods, there is a growing need to understand their strengths and limitations, reduce barriers to adoption, and apply them to real-world problems in drug development. This virtual challenge is designed to foster collaborative, open research that contributes to this mission.</p>

<h2> Your Role </h2>

<p>Academic/industrial researchers, start-ups and students can propose projects with respect to this year's <a href="https://quantum-innovation-challenge.github.io/projects/">challenge topic</a> applying quantum computing and quantum-inspired algorithms to:</p>

<ul>
<li>existing benchmarks or new benchmarks as further defined by the <a href="https://quantum-innovation-challenge.github.io/projects/">Quantum Challenge 2025 topic</a></li>
<li>creating sub-algorithms based on quantum computing methods</li>
<li>designing quantum-enhanced sampling and optimization techniques</li>
</ul>

<p>Following the challenge, results will be collated and secured under open-source and free license agreements (Apache/MIT) in the dedicated Quantum-Challenge-2025 repository.</p>

<h2> Who can participate? </h2>

<p>The challenge encourages cross-disciplinary and international collaboration. It is open to teams of academic and industrial researchers, start-ups, and students who are interested in using quantum computing and quantum-inspired methods to advance pharmaceutical development.</p>

<p>To be eligible for submission:</p>

<ul>
<li>Each team must include at least one clearly documented academic participant in a main role</li>
<li>Teams should have prior programming experience and basic familiarity with git and GitHub</li>
<li>Full eligibility details are available on the <a href="https://quantum-innovation-challenge.github.io/eligibility/">Eligibility page</a></li>
</ul>



<div class="block lg:hidden mx-auto">
 {% include timeline.html %}
</div>

<h2> Support and participation resources: </h2>

<ul>
<li>Participants are welcome to connect and form teams using our dedicated <a target="_blank" href='https://matrix.to/#/#mqs-community-space:mozilla.org'>Element Space</a> (see also <a target="_blank" href="https://element.io">https://element.io</a>)</li>
<li>Orientation materials and technical guidance are available on the <a href="https://quantum-innovation-challenge.github.io/resources/">Resources page</a></li>
<li>Pre-registrations and questions can be sent to <a href="mailto:quantum_challenge@mqs.dk">quantum_challenge@mqs.dk</a>. All inquiries will be addressed collectively on the <a href="https://quantum-innovation-challenge.github.io/faq/">FAQ page</a></li>
</ul>

<h2> Why participate? </h2>

<div class="grid grid-cols-1 md:grid-cols-2 gap-6 py-4">
<div class="flex flex-col items-center justify-start p-5 border-1 border-electron/25 bg-electron/5">
<img src="{{ "/assets/icons/supercomputer.svg" | relative_url }}" class="svg w-12 h-12 text-electron">
<p class="font-bold text-center">Access to the Gefion AI supercomputer </p>
</div>
<div class="flex flex-col items-center justify-start p-5 border-1 border-electron/25 bg-electron/5">
<img src="{{ "/assets/icons/globe.svg" | relative_url }}" class="svg w-12 h-12 text-electron">
<p class="font-bold text-center">Join QAI venture and Novo Holdings ecosystem (1:1 mentoring) </p>
</div>
<div class="flex flex-col items-center justify-start p-5 border-1 border-electron/25 bg-electron/5">
<img src="{{ "/assets/icons/collaborate.svg" | relative_url }}" class="svg w-12 h-12 text-electron">
<p class="font-bold text-center">Sparring with life science, quantum computing and AI experts</p>
</div>
<div class="flex flex-col items-center justify-start p-5 border-1 border-electron/25 bg-electron/5">
<img src="{{ "/assets/icons/exposure.svg" | relative_url }}" class="svg w-12 h-12 text-electron">
<p class="font-bold text-center">Exposure at high impact conferences</p>
</div>
<div class="flex flex-col items-center justify-start p-5 border-1 border-electron/25 bg-electron/5">
<img src="{{ "/assets/icons/open-source.svg" | relative_url }}" class="svg w-12 h-12 text-electron">
<p class="font-bold text-center">Community driven open-source and free license efforts</p>
</div>

<div class="flex flex-col items-center justify-start p-5 border-1 border-electron/25 bg-electron/5">
<img src="{{ "/assets/icons/network.svg" | relative_url }}" class="svg w-12 h-12 text-electron">
<p class="font-bold text-center">Supported and extended networking opportunities</p>
</div>
</div>

<ul>
<li>Five teams will be selected to present their work at the <a href="https://eqtc2025.ku.dk/">European Quantum Technologies Conference 2025 (EQTC)</a> in Copenhagen.</li>
<li>After the announcement of the finalists at EQTC in November, the 5 finalists gain access to the GEFION Supercomputer to continue the development of their models. Submission deadline for the second phase is expected to be end of January 2026 with announcement of the final winner in Q1 2026.</li>
<li>The winning solution will be announced in Spring 2026 during another leading European quantum event and a prize is offered for the final winning team in the form of extended free access to the Gefion AI supercomputer, sponsored by DCAI.</li>
<li>Networking and access to a global community of experts from the academic and industrial life science community.</li>
<li>Working on a relevant life science use case with feedback and mentoring from leading industry partners, investors, and experts.</li>
<li>Direct access and support from Gefion, one of the fastest supercomputers globally, to run your challenge code (5 finalists).</li>
<li>Global marketing and branding with free tickets to EQTC 2025, presentation opportunities and further fostering of relationships (5 finalists).</li>
<li>Novo Holdings and QAI Ventures will help to facilitate access to their global investor network.</li>
<li>Onboarding to the global QAI Ventures ecosystem with 1 year of exclusive 1:1 mentoring from investment and technology experts and a ticket to the QAI Ventures speed dating session to join upcoming venture building or accelerator programs (top 3 teams).</li>
</ul>

<p>Do not miss this opportunity to engage in quantum innovation at the frontier of life sciences.</p>

<p>📅 Visit the <a href="https://quantum-innovation-challenge.github.io/agenda/">Timeline page</a> to view the full agenda.</p>

<h2> Submitted Projects </h2>

<p>The top-ranked projects will be highlighted here:</p>

<div class="overflow-x-auto">
  <table class="w-full mx-auto border-collapse border border-electron/25">
    <thead>
      <tr class="bg-electron/5">
        <th class="border border-electron/25 px-4 py-3 text-left font-space-mono text-sm font-semibold">Rank</th>
        <th class="border border-electron/25 px-4 py-3 text-left font-space-mono text-sm font-semibold">Project #</th>
        <th class="border border-electron/25 px-4 py-3 text-left font-space-mono text-sm font-semibold">Team Name</th>
        <th class="border border-electron/25 px-4 py-3 text-left font-space-mono text-sm font-semibold">Project Name</th>
      </tr>
    </thead>
    <tbody>
      <tr class="hover:bg-electron/5 transition-colors">
        <td class="border border-electron/25 px-4 py-3 font-space-mono text-sm">1st</td>
        <td class="border border-electron/25 px-4 py-3 font-space-mono text-sm"><a href="" class="text-blue-600 hover:underline"></a></td>
        <td class="border border-electron/25 px-4 py-3 font-space-mono text-sm"></td>
        <td class="border border-electron/25 px-4 py-3 font-space-mono text-sm"></td>
      </tr>
      <tr class="hover:bg-electron/5 transition-colors">
        <td class="border border-electron/25 px-4 py-3 font-space-mono text-sm">2nd</td>
        <td class="border border-electron/25 px-4 py-3 font-space-mono text-sm"><a href="" class="text-blue-600 hover:underline"></a></td>
        <td class="border border-electron/25 px-4 py-3 font-space-mono text-sm"></td>
        <td class="border border-electron/25 px-4 py-3 font-space-mono text-sm"></td>
      </tr>
      <tr class="hover:bg-electron/5 transition-colors">
        <td class="border border-electron/25 px-4 py-3 font-space-mono text-sm">3rd</td>
        <td class="border border-electron/25 px-4 py-3 font-space-mono text-sm"><a href="" class="text-blue-600 hover:underline"></a></td>
        <td class="border border-electron/25 px-4 py-3 font-space-mono text-sm"></td>
        <td class="border border-electron/25 px-4 py-3 font-space-mono text-sm"></td>
      </tr>
      <tr class="hover:bg-electron/5 transition-colors">
        <td class="border border-electron/25 px-4 py-3 font-space-mono text-sm">4th</td>
        <td class="border border-electron/25 px-4 py-3 font-space-mono text-sm"><a href="" class="text-blue-600 hover:underline"></a></td>
        <td class="border border-electron/25 px-4 py-3 font-space-mono text-sm"></td>
        <td class="border border-electron/25 px-4 py-3 font-space-mono text-sm"></td>
      </tr>
      <tr class="hover:bg-electron/5 transition-colors">
        <td class="border border-electron/25 px-4 py-3 font-space-mono text-sm">5th</td>
        <td class="border border-electron/25 px-4 py-3 font-space-mono text-sm"><a href="" class="text-blue-600 hover:underline"></a></td>
        <td class="border border-electron/25 px-4 py-3 font-space-mono text-sm"></td>
        <td class="border border-electron/25 px-4 py-3 font-space-mono text-sm"></td>
      </tr>
    </tbody>
  </table>
</div>

<p>For a full list of the submitted challenge projects, we encourage you to take a look at the <a href="https://quantum-innovation-challenge.github.io/submission/">Submit a Project page</a>.</p>


<h2> Partners </h2>
<div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-4 not-prose"> 
<div class="flex flex-col items-center justify-center p-5 border-1 border-electron/25 bg-white p-5 h-[150px]  hover:bg-electron cursor-pointer transition-all duration-300 ease-in-out">
<a target="_blank" class="w-full h-full text-[#00185A]!" href="https://novonordiskfonden.dk" style="color: #00185A !important">
<img src="{{ "/assets/partners/nnf.svg" | relative_url }}" alt="Novo Nordisk Foundation" class="svg w-full h-full  object-cover">
</a> 
</div>
<div class="flex flex-col items-center justify-center p-5 border-1 border-electron/25 bg-white p-5 h-[150px] hover:bg-electron cursor-pointer transition-all duration-300 ease-in-out">
<a target="_blank" class="w-full h-full text-[#00464B]!" href="https://bii.dk/">
<img src="{{ "/assets/partners/bii.svg" | relative_url }}" alt="BioInnovation Institute" class="svg w-full h-full  object-cover">
</a>
</div>
<div class="flex flex-col items-center justify-center p-5 border-1 border-electron/25 bg-white p-5 h-[150px] hover:bg-electron cursor-pointer transition-all duration-300 ease-in-out">
<a target="_blank" class="w-full h-full text-[#00185A]!" href="https://novo-holdings.com/">
<img src="{{ "/assets/partners/nh.svg" | relative_url }}" alt="Novo Holdings" class="svg w-full h-full  object-cover">
</a>
</div>
<div class="flex flex-col items-center justify-center p-5 border-1 border-electron/25 bg-white hover:bg-electron p-5 h-[150px]  cursor-pointer transition-all duration-300 ease-in-out">
<a target="_blank" class="w-full h-full text-black!" href="https://mqs.dk/">
<img src="{{ "/assets/partners/mqs.svg" | relative_url }}" alt="Molecular Quantum Solutions (MQS)" class="svg w-full h-full  object-cover">
</a> 
</div>
<div class="flex flex-col items-center justify-center p-5 border-1 border-electron/25 bg-white p-5 h-[150px] hover:bg-electron cursor-pointer transition-all duration-300 ease-in-out">
<a target="_blank" class="w-full h-full" href="https://dcai.dk/">
<img src="{{ "/assets/partners/dcai-full.svg" | relative_url }}" alt="Danish Centre for AI Innovation" class="svg w-full h-full text-black object-cover">
</a>
</div>
<div class="flex flex-col items-center justify-center p-5 border-1 border-electron/25 bg-white p-5 h-[150px] hover:bg-electron cursor-pointer transition-all duration-300 ease-in-out">
<a target="_blank" class="w-full h-full" href="https://qai-ventures.com/">
<img src="{{ "/assets/partners/qai.svg" | relative_url }}" alt="QAI Ventures" class="svg w-full h-full text-black object-cover">
</a>
</div>
<div class="flex flex-col items-center justify-center p-5 border-1 border-electron/25 bg-white p-5 h-[150px] hover:bg-electron cursor-pointer transition-all duration-300 ease-in-out">
<a target="_blank" class="w-full h-full" href="https://investindk.com/">
<img src="{{ "/assets/partners/erhvervsstyrelsen-color.svg" | relative_url }}" alt="Invest in Denmark" class="svg w-full h-full text-black object-cover">
</a>
</div>
<div class="flex flex-col items-center justify-center p-5 border-1 border-electron/25 bg-white p-5 h-[150px] hover:bg-electron cursor-pointer transition-all duration-300 ease-in-out">
<a target="_blank" class="w-full h-full" href="https://danishbusinessauthority.dk/">
<img src="{{ "/assets/partners/dba.svg" | relative_url }}" alt="Danish Business Authority" class="svg w-full h-full text-black object-cover">
</a>
</div>
<div class="flex flex-col items-center justify-center p-5 border-1 border-electron/25 bg-white p-5 h-[150px] hover:bg-electron cursor-pointer transition-all duration-300 ease-in-out">
<a target="_blank" class="w-full h-full" href="https://icdk.dk/">
<img src="{{ "/assets/partners/icd.svg" | relative_url }}" alt="Innovation Centre Denmark" class="svg w-full h-full text-black object-cover">
</a>
</div>
<div class="flex flex-col items-center justify-center  border-1 border-electron/25 bg-white p-2.5 flex justify-center items-center h-[150px] hover:bg-electron cursor-pointer transition-all duration-300 ease-in-out">
<a target="_blank" class="w-full h-full flex justify-center items-center" href="https://eqtc2025.ku.dk/">
<img src="{{ "/assets/partners/eqtc.png" | relative_url }}" alt="European Quantum Technologies Conference 2025" class=" w-full ">
</a>
</div>
</div>
<p class="text-xl">The 2025 challenge is supported by industry experts from Novo Nordisk A/S and Roche Holding AG:</p>
<div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-2 gap-4 not-prose"> 
<div class="flex flex-col items-center justify-center p-5 border-1 border-electron/25 bg-white p-5 h-[200px]  hover:bg-electron cursor-pointer transition-all duration-300 ease-in-out">
<a target="_blank" class="w-full h-full text-[#00185A]!" href="https://novonordisk.com/">
<img src="{{ "/assets/partners/novo-nordisk.svg" | relative_url }}" alt="Novo Nordisk Foundation" class="svg w-full h-full  object-cover">
</a> 
</div>
<div class="flex flex-col items-center justify-center p-5 border-1 border-electron/25 bg-white p-5 h-[200px]  hover:bg-electron cursor-pointer transition-all duration-300 ease-in-out">
<a target="_blank" class="w-full h-full text-[#00185A]!" href="https://roche.com/">
<img src="{{ "/assets/partners/roche.svg" | relative_url }}" alt="Novo Nordisk Foundation" class="svg w-full h-full  object-cover">
</a> 
</div>
</div>


<p>For further information see the list of experts on the <a href="{{ site.baseurl }}/about/">about page</a>.</p>

<h2> Financial Sponsors </h2>
<ul>
<li> <a target="_blank" href="https://novonordiskfonden.dk/">Novo Nordisk Foundation</a> </li>
<li> <a href="https://danishbusinessauthority.dk/">Danish Business Authority</a> </li>
</ul>
</div>

</div>
 <div class="hidden lg:flex flex-col lg:min-w-[360px] lg:w-[360px] lg:max-w-[360px] my-16 py-8 border-1 border-electron/25" id="right-sidebar">
     {% include timeline.html %}
</div>

</div>

</section>

