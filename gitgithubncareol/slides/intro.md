
## `git@github.com:ncareol`

<img src='img/git-logo.png' height=150 width=150/>
&nbsp;&nbsp;&nbsp;
<img src='img/eollogo_transparent.png' height=150 width=150/>
&nbsp;&nbsp;&nbsp;
<img src='img/octocat-original.png' height=150 width=150/>

#### Erik Johnson, NCAR EOL

#### Boulder Ruby, 2014/08/19

http://erikj.github.io/gitgithubncareol

!NOTE
Erik, Software Engineer w/ NCAR EOL here in Boulder. Here to share our experience
using Git and GitHub to enhance our development and deployment workflows. Also, I
have stickers to give out afterwards.

!SLIDE

### NCAR Earth Observing Laboratory

### (EOL)

<img src='img/eollogo_transparent.png' height=400 width=400 />

!NOTE
NCAR is the US National Science Foundation's National Center for Atmospheric Research.
EOL provides instruments, infrastructure, logistics for atmospheric research
upsondes, dropsondes, radar, Gulfstream V and C-130 research aircraft, instruments aboard NASA Globalhawke UAV

!SLIDE

# NCAR EOL Facilities

<img src='img/gv.jpg' alt='GV' />

!NOTE
NSF/NCAR Gulfstream V

<!-- via https://drive.google.com/a/ucar.edu/folderview?id=0B0Rci5AHHBhHRkRqYUM0QmJ6MFk -->

!SLIDE

# NCAR EOL Facilities

<img src='img/anvil-cloud.jpg' alt='anvil cloud' />

!NOTE
Anvil cloud from G-V

!SLIDE

# NCAR EOL Facilities

<img src='img/c130.jpg' alt='C-130' />

!NOTE
NSF/NCAR Gulfstream C-130


!SLIDE

# NCAR EOL Facilities

<img src='img/radar.jpg' alt='Radar' />

!NOTE
Radar

!SLIDE

# NCAR EOL Facilities

<img src='img/radar-ops.jpg' alt='radar ops' />

!NOTE
Radar Ops

!SLIDE

# NCAR EOL CDS

## <img src='img/cds-logo_3_white_letters-small.png' alt=' Computing, Data and Software (CDS)' />

https://www.eol.ucar.edu/about/our-organization/cds

!NOTE
IT Infrastructure and support facility

!SLIDE

<img src='img/cds-logo_3_white_letters-small.png' alt=' Computing, Data and Software (CDS)' />

- EOL computing & IT infrastructure
- Data-management services
  - real-time & post-facto access
- Field-project support
  - IT
  - collaborative tools

!NOTE
CDS supports everything from EOL networking, printers, workstations and laptops,
to ingest, access and archival of research data from satellites, radar, aircraft,
weather stations, etc.

!SLIDE

# NCAR EOL CDS

## Collaborative Technologies & Metadata (CTM) group

- Databases
- Web applications
- MapServer
- Data ingest
- IRC

!SLIDE

# Field Projects

- Campaigns to conduct atmospheric research
  - Weather
  - Climate
  - Chemistry
  - Pollution

!SLIDE

# Field Projects

- *e.g.*
  - [DC3](https://www.eol.ucar.edu/field_projects/dc3) (Kansas, 2012)
  - [MPEX](https://www.eol.ucar.edu/field_projects/mpex) (US Southwest, 2013)
  - [SAS / NOMADSS / SOAS](https://www.eol.ucar.edu/field_projects/sas) (US Southeast, 2013)
  - [CONTRAST](https://www.eol.ucar.edu/field_projects/contrast) (Guam, 2014)
  - [DEEPWAVE](https://www.eol.ucar.edu/field_projects/deepwave) (New Zealand, 2014)
  - [FRAPPE](https://www.eol.ucar.edu/field_projects/frappe) (Colorado, 2014)

!SLIDE

# Field Catalog

- ingests, serves and archives field-project data:
  - operational
  - research
  - model
  - primarily images, text, HTML, PDF and KML
- used during and after project

!SLIDE

# Field Catalog

Suite of applications:

- *zith9* database schema (MySQL)
- *Catalog Models* Rubygem (Ruby, ActiveRecord)
- *Catalog Ingest* application (Ruby, ActiveRecord, Inotify, EventMachine)
- *Field Catalog* web application (Ruby on Rails, Haml, CoffeeScript, Bootstrap, PDF.js, CKEditor)
- *Catalog Maps* web application (Ruby on Rails, Haml, CoffeeScript, OpenLayers, Bootstrap)
- *Catalog Nagios* monitoring utility (Ruby, ActiveRecord, Nagios)
- *Catalog Stats* command-line application (Ruby, ActiveRecord)
- *IRCBot* Bot-provided IRC utilities (Ruby, Cinch)

!NOTE
Most applications after Catalog Models all depend on it.
We're currently using: Ruby 1.9.3, Rails 3.2 and Bootstrap 2.3

<!-- TODO: screenshots of CatalogUi and CatalogMaps -->

!SLIDE

[catalog.eol.ucar.edu](http://catalog.eol.ucar.edu)

<img src='img/screenshot-projects-list.png' />

!NOTE
root route, `Projects#list`

!SLIDE

[catalog.eol.ucar.edu/frappe](http://catalog.eol.ucar.edu/frappe)


<img src='img/screenshot-frappe-home.png' />

!NOTE
`Projects#show`, FRAPPE project homepage, `/frappe`

!SLIDE

PDF Report

<img src='img/screenshot-frappe-report.png' />

!NOTE
`Pdfs#show`

!SLIDE

Product Navigation

<img src='img/screenshot-frappe-satellite-products.png' />

!NOTE
`Categories#date`

!SLIDE

Satellite Product

<img src='img/screenshot-frappe-goes13-product.png' />

!NOTE
`Files#show`

!SLIDE

# Catalog Maps

<img src='img/screenshot-catalog-maps-deepwave.png' />

[catalog.eol.ucar.edu/maps/deepwave](http://catalog.eol.ucar.edu/maps/deepwave)

!NOTE
Geo interface. Features: geolocated imagery, KMLs of satellite data and aircraft
flight tracks, temporal navigation. Made w/ OpenLayers, OpenStreet Maps, Bootstrap,
jQuery UI.

!SLIDE

# Field-Catalog Development

- Group lead is Product Owner
- developed by 2-6 active Software Engineers @ any time: **CTM** team & others
- administered by ~ one Software Engineer / active project
- scrum: three times / week

!SLIDE

# Git <img src='img/git-logo.png' alt='' style="width:100px;height:100px;vertical-align:middle" />

- Distributed revision-control system
- every check out is a complete, free-standing repository

!NOTE
developers have a complete VCS w/o need to interact w/ central / other repositories

!SLIDE

<img src='img/octocat-original.png'  />

!NOTE
CTM has been using GitHub for most of our development for ~ 3 years

!SLIDE

# `github.com/ncareol`

- 17 private repositories
- 9 public repositories
- 13 teams
- 16 members
- initial plan: Bronze, 10 private repositories, $25 / month
- later: Silver, 20 private repositories, $50 / month

https://github.com/pricing

!NOTE
this is much cheaper than paying staff developers and / or system administrators to maintain similar functionality.
teams: we have many that have a team of contributors, and a team-admins for those
who are to administer the team's repositories
