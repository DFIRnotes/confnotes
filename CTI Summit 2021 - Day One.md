# CTI Summit 2021

## intros
* Rob M Lee (SANS, Dragos)
* Rebekah Brown (author with Scott of IDIR)
* Rick Holland
* Katie Nickels
* #ctlsummit , evals, Slack

**Day 1 talks**

## Hack Your Stakeholder: Eliciting Intelligence Requirements with Design Thinking - Brian Kime, @BrianPKime
* YOLOSec vs FOMOSec
* limits of brainstorming: many only invite 'friendly' minds, exclude actual stakeholders
* Intel Prep of Cyber Environment (IPCE) - phases of process : not good against hordes of weakly defined threats
  * sometimes reduced to two: most likely and most damaging
  * acknowleges that it didn't work at $lastjob
  * saw a vendor try to use it for onboarding, 30 Days
    * at a high level, from outside
* bad requirements examplea
  * the dark web
  * domain names, Ip ranges, Tor nodes
  * executive contact data
* good requirements examples (long term stakeholder questions)
  * What infrastructure is being used for social engineer vs $ORGNAME contacts ?
  * What exploits are likely to be used to compromise $ORG hw and hw ?
  * Infra of known threat group, likely to be used in campaign against $ORGNAME ? (disagree)
  * TTPs likely to be wielded by $ACTORS against $ORG $crown_jewels ?
* how elicit requirements?
* Design thinking
  * "iterative process of building products with stakeholder at center"
    * cycles, prototypes, testing
  1. Motivation
     1. Threat Landscape
     2. Big incident theirs or someone elses
     3. brand protection
  2. Empathise
     * Stakeholder Analysis worksheet (slide): 
       * by role , rankings, their issues and possible strategies for influence 
     * Empathy Map (??) : models how to have actual conversations
  3. thing
  4. thing
* Feedback / metrics
  * s/n
  * FP rate (??)
  * talk to stakeholder and keep having conversations on their concerns
* requirements are only part of planning and direction
  * collection plan
    * sources linked to SIRs
    * new sources needed
  * RFIs in planning and direction
  * intel architecture / data processing
    * to make way for human analysis
* an action plan
  * pick a couple stakeholders, and ask them for others
    * iterate and make incremental improvements
  * for BPK: more research 
    * hoping to opensource some tools / templates
* Q & A
  * try to learn about the org, don't ask for requirements outright up front
  * how often review requirements ? continually , whatever that means for your iterations
  * how many IRs / maturity: 4-5 is a good number for one org, vendors says 20-25 per client
  * needs analysis remote? design thinking vs Zoom: challenges over video
    * some distraction / non-verbal cues on video
    * inflections in voice channel
  * Empathy as a Service (infosec sherpa talk)

## spectrum of state affiliation - Joshua Miller @chicagocyber
* ...
* stipulations
  * attribution: activity clusters
  * Attribution: namign and shaming : harder
  * Trust but Verify : public on the record statements by govts (orgs really) are political (and commerical) acts
  * CTI: 
    * informs risk decision makers
    * research adversaries to enhance defense, 
* Sources of attribution
  * Gov: indictments and sanctions (DoJ, DoT)
    * other gov statements
  * OpSec fails by actors (various examples)
  * Leaks ...
* via the academic Atlantic Council paper maybe a good link /QR code
  * red (prohibited) to purple (integrated)
* Red: State-Prohibited: UK national extradited in TDO case
  * but inadequate: BEC from African countries with unrestricted targeting (same country)  
* State Ignored
  * eg Iran residents, Samsam actors indictment
* Yellow: State Encouraged
  * website defacements / hackivism by Iranian citizen
* State Shaped and State Coordinated (green)
  * Companies working on behalf of the government (IRGC)
  * State provided operation details (MSS)
* State-Ordered (bright blue)
  * proxies for state action: logo comparision for APT39 vs Iranian intel corp Rana
  * two source corraberation
* State Rogue
  * "moonlighting" with / as criminals
  * not Lazarus Group(s), says the presenter
* State Executed (dark blue)
  * APT1 2014 Indictment
  * Equifax indictment, PLA "in uniform"
  * SandCat email/domain opsec fail reported by Kaspersky Labs
* State Integrated (purple)
* rainbow of 10 terms and colours, nuance
* Hypotheticals
  1. Vendor: DIB trackign seeing credit union targeting?
    * State ordered or possibly state rogue
  2. internal corp CTI: embarass Iran, new threat group types target you?
    * Sands casino example: high end
    * defacements and graffiti: state encouraged 
* Actions for audiences:
  * Gov: use this or another framework for clearer more useful reporting
  * Vendor: use approproate language in assessments
  * internal: help you stakeholders understand the differences
    * state-prohibited crimeware may present more risk (or more actions) than state integrated APT
* Q&A
  * ... colours ...
  * Distinguish state supported financial vs other financial ?
    * Don't assume financially motivated cannot be state shaped, sponsored or even integrated.
      * Samsam vs "Lazarus Group"
      * targetting analysis and thinking about objectives of adversary
  * ... transitive attribution via loss / impact measures ?
  * big A vs little a attribution, how do you use the spectrum with C-levels vs CTI teams?
    * [discussion]

## Cyber-Espionage: Out of the Shadows, Into The Digital Crosshairs - John Grim 
* Verizon Cyber espionage report Nov 2020 from DBIR data
  * 1 incident class pattern from 10 in the DBIR
  * 7 years, 7 verticals, 1K+ breach reports
  * not indicators, but assets targeted and data sought
  * callouts: prevent mitigate detect and respond
    * eg CIS CC
* defined
  * espionage motive 
  * confirmed data breach, 
  * external threat actor, 
  * unauthorised access
  * often state affiliated, often non-regulated data
* actor tendencies
  * usually move slowly and carefully
  * avoid detection through entire life cycle (incl exfil)
  * often long dwell time
* frameworks and guides
  * NIST 1.1 five functional areas and controls
  * VERIS
  * VIPER readiness and preaperedness
* Nine patterns and a catch-all : 16K reported data breaches
* Actors (from A4 in VERIS)
* into the dataset
* State affiliation
* Motives over time
* industries
* breached data types, money, and CSC controls
  * timelines, and controls, Cyber espionage vs all breaches in DBIR dataset
* attacker time to compromise: much slower than other breaches
* attacker time to exfil: much slower than other breaches
* defender time to discovery: months to years (peak in years) vs days to months (peak in months)
* defender time to containment: days to months vs hours to months for all
* discovery methods: technical sources (AV, NSM) distinct from non-technical for all breach data
  * longer to discover, if you have packet capture and analysis (or EDR ) and skillset, processes
* Threat model (A4) -> Assets impacted
  * endpoints actually targeted vs all breaches (servers and databases)
* Actions
  * same three actions, different priority
* Social Action varieties
  * more phishing for cyberespionage (90% vs 80%)
* "Hacking" Action varieties
  * backdoors lead stolen creds for cyberespionage
* "Malware" action varieties
  * cyberespionage broadly have backdoor and C2
  * less emphasis on keyloggers and data theft malware
* Attributes (CIA)
  * Confidentialy and Integrity breach percentages
    * vs Availability
  * software integrity types (91%) clearly more prevalent in cyberespionage vs DBIR 43%
* ... dropped speaker connection ... briefly
  * Hosts: good material for threat modelling and questions queing up
* Parting thoughts: advanced tools for advanced threat
  * malware tracking ineffective vs LoL and actor use of admin tools
  * handouts / links
* Q&A -> Slack
* Lunch!

* _missed more talks_

