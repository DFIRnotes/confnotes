# TIL Purple Team Summit 2021

_These are not my full notes taken, as those are colorful and mass 500g._

_work in progress_

All the talks were informative and most were over-filled with actionable recommendations and pitfalls to avoid based on the experience of the presenters. Thanks to all the presenters, hosts, and especially the event staff!

# Day 1 Talk Highlights

## Purple Vitamins - Didier Stevens
**Purple Vitamins to Grow Your Skills** - Didier Stevens @DidierStevens (Day 1 Keynote)
* An immensely accomplished hacker whose tools we all use explains some of the "secrets" that power his work
  * starting with: things you learn through your own discovery and experimentation stick with you forever (story in talk)
* gives tips on Experimentation and documentation for skills improvements
  * as Vitamins: P V X B D & M
  * but not in Production / without permission!
* Code, document, blog, give talks on things others already have or know
  * to learn, to understand problems, and to help others learn
  * start simple (use templates) and work on your problems
  * don't worry about "reinventing wheels" so much
* Document and share failures too, failure is essential to learning and improving
  * First Attempt In Learning
* vital skills in infosec: programming, reading code, writing documentation
* Purple? Red + Blue is only the beginning of cross-collaboration
  * Red and Blue, 'sploit and detect, but
  * Ask an Exchange admin for help on those vulns/PoCs/detections!
* The live example detection he walks through, though explainable in the talk, is pretty useful vs Metasploit Framework and Cobalt Strike traffic.
* I :heart: the virtual machine snapshot tree screenshots he shared.

## Purple Team Maturity Model
**Purple Team Maturity Model** Timothy Schulz
* Advocates taking Purple Team approach beyond exercises to an organisational design 
  * go beyond Red, Blue, and CTI as teams model limitations
  * to achieve greater effectiveness from collaboration and break down silos
* Distinguishes "red" from "blue" as threat understanding and detection understanding
* Three levels, applicable to many technologies/processes beyond Purple Teaming    
  * Level 1: Deployment: can you use tools someone else wrote ?
  * Level 2: Integration: can you share data with other systems and processes effectively ?
  * Level 3: Creation: can you create new content, new integrations ?
* charts TU , DU and the Levels against each other in a 3x3 matrix
* nice three party scenario with Red, Blue, and CTI  working together
  * shifting roles along the PTMM for a better process, better results (with some testing & SDLC)
  * maybe fewer detections that work much better, rather than so many less useful detections and alerts

## Purple Wars Episode II 
**Purple Wars Episode II: Attack of the Emulators** - Jonas Baueters
* outlines the Offensive Security Maturity Model
  * distinguishes Vuln Scan, Vuln assessment, Pen Test from
  * Red Team, Purple Team, Adversary Emulation
* explains the different activities and their goals and value
  * Objective based tests and scenario based tests  
  * use of stealth tactics
  * simulation vs emulation  
* Purple team Exercises and Adversary Simulation for detection improvements
  * starts with no stealth, add stealth to continuosly improve detections
* Recommends continuous Purple Team activity with periodic Red Team assessments
  * get more value out of expensive,detailed Red Team / Adv Emu exercises
  * replay TTPs from Red Team activity for Purple Team exercises, possibly automated
  * Scythe.io, MITRE Caldera, RedCanary Atomic Red Team
* Report on exercises and show improvements over time
  * Vectr.io, DeTT&CT
* Observations and Lessons Learned:
  * Lots of Blue Team time/resources needed for success: 
    * work all together rather than trying to synchronise with short meetings
  * Align exercices to maturity and use them to correct expectations of response
* Purple Team exercises as as the course, Red Team exercise as the Exam : formative vs summative evaluation!

## Don't Fear the Zero: Test Driven Approach to Analytic Development
**Don't Fear the Zero: Test Driven Approach to Analytic Development** - Fred Frey & Tim Nary (BAH Dark Labs)
* a detailed and thorough introduction to analytic design by testing, what some now call "detection engineering"
* walk through a simple looking detection ```net.exe localgroup adminsitrators``` describing how complex it can be to get right
  * and another ```wmic process call create script.vbs```
* Starting from "zero hits can mean a lot of things" ( the difference between zero results and null results ), they describe in detail a continuous process starting from threat intelligence to design, test, improve, and maintain effective detections
* "Production ready real world analytics"
  1. from TI reporting
  1. Isolate Techniques -> Threat Library
  1. Create Detections -> Detection (Analytic) Library
  1. Test and improve to reduce FPs (with Red Team)
  1. Continually improve robustness and validate detection logic working with Red Team
* So many great things in this talk:
  * treating detections as code, applying an SDLC to detections
  * track your detections outside the target tool to run a robust process
  * you might build up undetected attack logs in your Threat Library faster than untested detection rules in your Analytic Library
  * expecting variances in the environment to change the results of deployed analytics ...
  * Sigma Project has free rules covering many use cases
  * Great dev/test resources, by category
    * Mordor Project, RedCanary ART, DetectionLab, Sigma
  * Distinguish IoC matches, behavioural detections, and investigative leads (haystack)
    * high confidence but brittle <- "just right" -> useful for correlation
* "Process is key" and sharing a collaboration platform is very helpful

## Red vs. Blue: Getting Blue Team Value from Red Team Testing
**Red vs. Blue: Getting Blue Team Value from Red Team Testing** - Tony Drake
* This is a great talk full of guidance and lessons developed from years of Red Team exercises
  * (disclaimer: I worked through some of it with Tony, so I could be biased ...)
* Aligning organisational goals of Red Team exercises with improving Blue Team just makes sense
  * Clarity from leadership about the purpose of exercises is essential!
* Tony describes and labels common SOC ailments and provides solutions:
  * Leadership and clear communication of exercise purpose
  * Capture more data during tests
  * Vary the methodology to get more learning
  * Eventually, gamification

## Red Team Engagements: Training Blue Team to Hunt Adversaries
_need to look over the slides / watch this one again to get more of it_
* Four Phases:
  1. Detection Chart (ala Navigator)
  1. Purple Team Exercise
  1. Adv Detection Pipeline
  1. Adv Services Lifecycle
* Execution and AAR phases
  * Don't disable monitoring, increase noise!
  * Provide IoCs to Blue Team if needed, "white card"
* Remediation
* Reporting and leadership engagement
  * RoI via improved MTTD, MTTR


I also found the lunchtime session with SANS Technical Institute team (sans.edu) helpful and informative.

# Day 2

## Understanding the Effectiveness of Exploit Mitigations
**Understanding the Effectiveness of Exploit Mitigations for Purple Team** - Stephen Sims, curriculum lead for Offensive Operations, author SEC660, SEC760
* pulled material for this talk from SEC599, SEC660, and SEC760
  * feels like he explained all of EMET and Defender in one talk!

## Purple Team Feedback Loop
**Purple Team Feedback Loop** - Michael Rogers
* Describes turning existing processes purple to close gaps 
  * in seven (7) (?!) areas
  * also uses threat hunting and tabletops in a Progressive Purple Feedback Loop (!)
* describes a robust detection development and testing process involving all roles, in four phases
  1. Research and Development (R & D)
  1. Creation
  1. Testing
  1. Deployment and Lessons Learned
* measurement and reporting suggestions throughout, to motivate teams, priortise issues, and report up
  * new detections, new techniques, new hunts, improved rule fidelity
* demostrates across a few test scenarios: use Agile processes to plan, track, and execute work
  * uses Level of Effort (LoE) points to allocate Red, blue, CTI, etc resources to a board track -> common goal
* A different Purple Team Maturity Model, four levels:
  1. Basic: broken controls, "hygiene" concerns, and a pen test report with findings
  2. Average
  3. Exceeding
  4. Defining Standards
* Specific guidance on "buy-in" and communicating RoI to different stakeholders
  * define and track output
  * work to common goals
* Project manager/coordinator: dedicated role essential, requires highly skilled person

## Supply Chain Purple
**Supply Chain Purple** Mike Gualtieri @mlgualtieri
* Hands on technical talk that describes a technique, explains how it works, demonstrates how to simulate a sophisticated intrusion using it
  * also how to detect it using Sysmon
  * how to combine host (sysmon) data with network data (Wireshark) to refine the detection
* many helpful tips on succesfully using malicious code in scenario or technique based exercises
  * and on steadily increasing obfuscation / evasion to better improve detection and response
* Details, source code, slides, blog post shared on his [GitHub](https://github.com/mlgualtieri/PurpleTeamSummit/tree/main/Summit-May2021)
