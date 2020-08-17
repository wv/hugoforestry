---
date: "2020-04-14T09:00:00Z"
title: When scaling your workload is a matter of saving lives
twittercard: Scaling the JHSPH model to save lives.
twitterimage: /images/covid1.png
twitterlargeimage: "true"
useexcerpt: "true"
---

<img src="/images/covid1.png" width="650">

On March 16, 2020, at 9:26 PM, I received an urgent email from my friend
DJ Patil, former White House Chief Data Scientist, Head of Technology
for Devoted Health, a Senior Fellow at the Belfer Center at the Harvard
Kennedy School, and Advisor to Venrock Partners. You don't get that many
titles after your name unless you're pretty good at something. For DJ,
that "something" is math and computer science.

DJ was writing to me from the California crisis command center. He
explained that he was working with governors from across the country to
model the potential impact of COVID-19 for scenario planning. He wanted
to help them answer critical questions, like "How many hospital beds
will we need?" and "Can we reduce the spread if we temporarily close
places where people gather?" and "Should we issue a shelter-in-place
order and for how long?" While nobody can predict the future, modeling
the virus with all the factors they *did know* was their best shot at
helping leaders make informed decisions, which would impact hundreds of
thousands of lives.

<!--more-->

DJ assembled a team of volunteers that consisted of some of the
brightest minds from across Silicon Valley and the country. As though
following a call to arms, these professionals came together, in a
personal capacity, to fight COVID-19 the best way they knew how: with
data.

The good news is that they had a model. And not just any model. DJ and
his team have been working with one that had been primarily developed by
the world renowned [Johns Hopkins Bloomberg School of Public
Health](https://www.jhsph.edu/) (JHSPH). This model, which is an
[open-source
project](https://github.com/HopkinsIDD/COVIDScenarioPipeline), uses
state or county population numbers along with transportation data to
model the number of people who potentially would be exposed, infected,
and/or hospitalized. The model also considers virus spread based on a
variety of non-pharmaceutical interventions, including shutting down
schools and parks and issuing quarantine orders.

However, the model was running on the JHSPH on-premises infrastructure
and the model pipeline couldn't scale to run a large number of scenarios
simultaneously or to meet the needs of the country (and potentially the
world). It was too slow. To get the required scale and speed, DJ and his
team needed to run the model in the cloud---so they moved their
on-premises code to AWS. This led to another challenge: The code hadn't
been written initially with the cloud in mind, so it couldn't fully take
advantage of the scale and optimizations possible with AWS. As a result,
DJ's team spent one week porting and running a single scenario for
California, which still wasn't fast enough.

Imagine how long it would take to scale the pipeline for 49 more states.
It would require at least months of work. Adding multiple scenarios with
different variables would delay it even more. DJ's team didn't have that
kind of time. In the words of Dr. Anthony Fauci, the director of the
National Institute of Allergy and Infectious Diseases, "You don\'t make
the timeline. The virus makes the timeline."

DJ's team needed to be able to onboard the model pipeline and run a full
report in hours rather than weeks or months. That's why DJ reached out
to me. He wanted our help optimizing the model pipeline for the cloud.
Presented with an opportunity to help my friend and support a project
that could save lives, I immediately said "yes."

When I sounded the alarm internally, something amazing happened. People
from across the company volunteered to help because they knew that they
had the expertise that the project needed. Nobody asked, "Who is
responsible for this customer?" or "Who has the bandwidth to work on
this project?" Everyone sprang into action immediately.

We wanted to get that model pipeline running like it had a jet engine.
The first thing we had to do was create an architecture that would fuel
the model every step of the way. We began by profiling the code and
re-compiling key numerical libraries.

Next, we had to help optimize the model pipeline. That's when our
specialist team, including the high performance computing (HPC) group,
stepped in. These professionals help organizations solve some of the
biggest data-related problems and tame the largest workloads, like in
genomics, computational chemistry, machine learning, and autonomous
vehicle simulation. They worked with members of DJ's team, JHSPH, and
some state employees non-stop through two weekends to optimize the model
pipeline through re-architecture and deployment on AWS.

We contributed to the open-source JHSPH model to enable a Continuous
Integration & Deployment (CI/CD) pipeline for container deployments on
Amazon Elastic Container Registry. Also, we orchestrated scalable
deployment strategies on AWS Elastic Container Service through AWS Batch
and integrated several other services, including Amazon S3 and Amazon
EC2 Auto Scaling. A high level of coordination with AWS was critical to
bringing all these technologies together.

<img src="/images/covid2.png" width="650">

<center>Figure 1: Architecture for the Scalable COVID Scenario Pipeline using
AWS Batch</center>
<br/>
**What was the end result?**

DJ's team has reduced the time to on-board the model pipeline and
generate a full report from one week for one scenario to under 12 hours
for multiple scenarios. Now, the new model created by JHSPH is being
rolled out on AWS to all 50 states and internationally to help with
making decisions that directly impact the global spread of COVID-19.

But this isn't where the story ends---it's where it begins. While the
spread of the virus is now global, we have yet to grasp its full impact
on human society. As we learn more about the spreading conditions of the
virus, iterating over existing models will be crucial. There will be
many more sleepless nights for everyone working on this initiative as
they continue to scale the model to more states and countries as well as
analyze the effect of mitigation strategies.

If you have relevant skills in technology, communications, and/or
operations, please consider joining the U.S. Digital Response team. It's
a volunteer-run, non-partisan effort to help federal, state, and local
government with technology, data, design, operations, communications,
project management, and other needs during the COVID-19 crisis.
<https://www.usdigitalresponse.org/>
