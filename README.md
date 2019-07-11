# IEWS(Immediate Earthquake Warning System)
![](https://img.shields.io/badge/Python-3.6-blue.svg)
![](https://img.shields.io/badge/alpha-running-brightgreen.svg)
![](https://img.shields.io/badge/beta-unknown-grey.svg)
![](https://img.shields.io/badge/release-unknown-grey.svg)

IEWS_CA alpha version is now running on server. System status: http://iews.siweihe.tech/status

## Introduction
System uses realtime earthquake data from IRIS. Still under active development.
The system is aimed to quickly analyze earthquake waveform and provide reliable earthquake warning.

## Current Status
1. Able to fetch single station realtime waveform.
2. Able to alert new seismic event from single station waveform data.

## Usage
1. run pyslink2mseed_SLA.py to collect realtime waveform data from CI_SLA station.
2. run mseedAnalysis.py to plot waveform from last 10 minutes (update every second).

pyslink2mseed_SLA.py is used to fetch latest data.

mseedAnalysis.py is used to display latest data, with not much analysis.

mseedAnalysis_server.py works without GUI(<strong>Need smtplib</strong> to send email). This file focuses on analyzing the waveform.

<strong>Note: The system cannot provide accurate magnitude analysis and warning at this stage</strong>

## Plan
The system will first focus on LA, US. Welcome more people to contribute to this repo.

## Credit
Part of the code is from @iannesbitt: https://github.com/iannesbitt/pyslink2mseed

## Resources
1. seedlink -> https://ds.iris.edu/ds/nodes/dmc/services/seedlink/
2. seismic stations search -> http://www.iris.washington.edu/gmap/#network=_REALTIME&planet=earth
