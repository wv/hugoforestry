---
date: "2020-07-09T20:30:00Z"
title: The journey to modern manufacturing with AWS
twittercard: How Manufactering is moving towards pure data-driven decision making
twitterimage: /images/sitewisebanner.png
twitterlargeimage: "true"
useexcerpt: "true"
---

<img src="/images/sitewisebanner.png" width="650">

One of the most rewarding parts of my job is getting to watch different
industries implement new technologies that improve and transform
business operations. Manufacturing, in particular, has always captivated
my attention in this respect. When I think about how Amazon's globally
connected distribution network has changed in the last decade alone,
it's incredible. From the Internet of Things (IoT) to Artificial
Intelligence (AI) and task automation to predictive maintenance
technology, the advancements in this space are creating a world of new
opportunity.

But this is complicated by that fact that many manufacturers have been
around for decades or longer. Some of their equipment was designed
before the internet even existed. If replacing this equipment isn't an
option, how do these manufacturers begin their journey to modern
manufacturing? The choice of what to embrace and where to start can be
daunting.

Ultimately, the reason for adopting any new technology in manufacturing
is usually to achieve one or more of the following objectives: produce
more, increase safety, or increase quality---and all at a lower cost.
The good news is that the most important thing a manufacturer needs to
accomplish with any of these objectives is something they already have.
It's something they've had since the moment they opened their doors,
whether that was yesterday or 100 years ago: data.

<!--more-->

**Data-driven technology**

In some ways, data is to factories what oxygen is to humans. Oxygen is
all around us, but it doesn't do us any good until we breathe it in.
Then we can use it to create energy. The more energy we have, the more
we can do. Manufacturers all over the world are sitting on mounds of
data that they aren't "breathing in."

Truly, the journey to modern manufacturing begins with unlocking this
data. The ability to tap into that data is the difference between
factories that are "smart" and benefiting from new technology, like
automation, machine learning (ML), and AI, and those that are being held
back by outdated tools and systems.

Where is this trapped data? That's where the problem lies for many
manufacturers. A lot of this valuable data is sitting in places where
it's hard to collect, compare, and take action on, like in old
machinery, isolated systems, spreadsheets, and even paper clipboards.

In an environment with varying legacy protocols and data formats from
the last 30+ years, how can one compare important metrics, like
productivity, equipment availability, and output quality, from different
lines within a factory or different factory sites? The data is stuck in
silos. I know this because, at AWS, we've helped hundreds of
manufacturing companies, like
[Georgia-Pacific](https://aws.amazon.com/solutions/case-studies/georgia-pacific/),
[Volkswagen](https://get.awscloud.com/iot-volkswagen-video-highlight),
and
[INVISTA](https://aws.amazon.com/solutions/case-studies/invista-case-study/),
solve the challenge of liberating industrial data to extract insights
from it.

**Using the right tools**

Manufacturers that are struggling to modernize their factories or feel
overwhelmed about all the different investments they could make in new
technology should focus on getting to the data. Collect data from
on-premises equipment, historian databases, and IoT sensors and move it
to the cloud. Then it can be organized, analyzed, visualized, and,
eventually, used to do more advanced things, like train an ML model that
can help predict when machinery will need to be serviced, thereby
avoiding unplanned downtime for operations. While that might sound
easier said than done, there are a variety of solutions that can help.

Let's take a look at the journey to modern manufacturing and some of the
tools at AWS that can help along the way.

**Data ingestion**

One solution that's become very important at AWS in simplifying the
ingestion of data into the cloud is [AWS IoT
SiteWise](https://aws.amazon.com/iot-sitewise/), a managed service that
makes it easy to collect, store, organize, and monitor data from
industrial equipment at scale.

<img src="/images/sitewise1.png" width="650">
<p align="center">Figure 1: AWS IoT SiteWise process flow</p>

AWS IoT SiteWise includes edge gateway software that automates the
process of securely connecting to on-premises equipment, collecting and
organizing industrial equipment data, and sending the data to the cloud.
Manufacturers run this gateway software on popular third-party
industrial gateways to read data using OPC Unified Architecture
(OPC-UA). This is an open interoperability standard for secure and
reliable exchange of data within industrial automation developed by the
[OPC Foundation](https://opcfoundation.org/).

By using standards like OPC-UA, industrial customers have a consistent
method for interfacing with many types of industrial equipment, like
SCADA systems, PLCs, and historians on the factory floor. With this
information, manufacturers can compare machine 1 to machine 2 (which may
have been bought 15 years apart), production line 1 to production line
2, and even factory 1 to factory 2.

AWS IoT SiteWise gateway software is provided as a pre-packaged
connector that runs on [AWS IoT
Greengrass](https://aws.amazon.com/greengrass/), which extends AWS to
edge devices so that they can act locally on the data they generate
while still using the cloud for management, analytics, and durable
storage. There are millions of connected devices in the manufacturing
world collecting important data every minute, like the environmental,
process, and vibration data from a particular machine.

AWS IoT SiteWise also provides interfaces for collecting data from
modern industrial applications through MQ Telemetry Transport (MQTT)
messages or Application Programming Interface (APIs).

**Data Management**

To make the data useful, you have to give it context. With AWS IoT
SiteWise, customers model their industrial equipment, processes, and
facilities by adding context (like equipment type and facility location)
to the collected data and creating hierarchies to represent
relationships. Then they define common industrial performance metrics,
like Overall Equipment Effectiveness (OEE) and uptime, on top of the
data using the AWS IoT SiteWise built-in library of mathematical
functions.

As data is ingested into the cloud, AWS IoT SiteWise automatically
computes the metrics at the interval defined by the customer (like
"report uptime every hour"). All uploaded data and computed metrics are
stored in a fully managed time series database, which automatically
scales with the customer's data usage and storage. This type of data
store is uniquely designed to store and retrieve time-stamped data with
low latency, making it significantly easier for customers to analyze
equipment performance over time.

For example, [Bayer Crop
Science](https://aws.amazon.com/iot-sitewise/#Customers), one of the
largest agricultural companies in the world, is constantly striving to
optimize yield in their crop fields and reduce waste in their production
plants. A major challenge they have faced in doing this is making all
the data they collected useful because it was stuck in siloes. Now,
using AWS IoT SiteWise across multiple corn production plants, they can
combine and analyze this data in a meaningful way, like to measure the
OEE of their machinery in near real time to identify production
inefficiencies.

**Data Visualization**

Having the right tools to collect, organize, and create metrics on
incoming data without writing any code creates huge savings in time and
effort for any developer. But the data and insights gathered also need
to be easily shared and visualized by industrial end users, such as
process engineers and operators, who will use the information to
identify and apply corrective actions and process improvements.

From within the AWS IoT SiteWise console, customers can create no-code,
fully managed web applications in minutes. There, they can display
equipment data and computed metrics in near real time and compare and
analyze historical performance across equipment or facilities. End users
can access the web applications from a browser on any web-enabled
desktop, tablet, or phone and sign-in with their corporate credentials
through a single sign-on (SSO) experience. Customers can create one or
more web applications to easily share access to industrial data with any
team in their organization to spot anomalies. This helps manufacturers
reduce waste, make faster decisions, and optimize their plant
performance.

<img src="/images/sitewise2.png" width="650">
<p align="center">Figure 2: AWS IoT SiteWise end user web application</p>

**Machine learning and more**

The next step in the journey to modern manufacturing is to start using
ML for predictive maintenance. Many manufacturers rely on people to
perform routine diagnostic duties and preventative maintenance on fixed
schedules. ML can provide a more reliable approach to preventive
maintenance. ML models can help predict the likelihood of asset failure
using sensor data and optimize schedules for maintenance procedures.
This predictive maintenance can help lower maintenance costs and reduce
unscheduled downtime.

For example, Georgia-Pacific is using ML to optimize paper towel
manufacturing. The Georgia-Pacific ML model can predict---based on the
quality of a parent paper towel roll---precisely how fast converting
lines should run to avoid tearing and to maximize production while still
maintaining the best quality. By reducing paper tears, Georgia-Pacific
has increased profits by millions of dollars for just one production
line. And there are at least 150 more lines that could benefit from
these optimized processes.

Predictive maintenance requires ML models that are trained on large
amounts of data. This is why data ingestion and data management are
critical first steps to take before expanding into ML. It's also why
many companies choose to create a [data
lake](https://aws.amazon.com/big-data/datalakes-and-analytics/what-is-a-data-lake/),
a centralized repository where organizations can store all their
structured and unstructured data at any scale. A data lake is a powerful
foundation for ML and AI (artificial intelligence) because ML and AI
thrive on large, diverse datasets.

An important tool many of our manufacturing customers use for ML,
including Georgia-Pacific, is [Amazon
SageMaker](https://aws.amazon.com/sagemaker/), a fully managed service
that removes the heavy lifting from each step of the machine learning
process to develop high quality models.

**Summary**

The history of manufacturing is a timeline of technology innovation.
Since the industrial revolution, manufacturers have been developing new
approaches to increasing quality, speed, safety, and efficiency while
lowering costs and waste. Now, as manufacturing innovation has moved to
the cloud, it\'s exciting to see the possibilities available to
manufacturing customers of all sizes and in every industry.

At AWS, we believe no manufacturer should be left behind. We provide a
path that can help manufacturers take advantage of new technology and
business opportunities, no matter where they are in their journey. I
look forward to seeing what our manufacturing customers will develop
next.

You can learn more about [modern
manufacturing](https://aws.amazon.com/manufacturing/) and [AWS IoT
SiteWise](https://aws.amazon.com/iot-sitewise/) on our website.
