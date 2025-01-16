---
title: "My 2025 Homelab"
date: 2025-01-08T08:06:25+06:00
description: a walkthrough of my improved homelab setup
menu:
  sidebar:
    name: My 2025 Homelab
    identifier: My 2025 Homelab
    weight: 20
author:
  name: Jeff Carstensen
  image: /images/author/jeff.png
math: true
---

## Introduction

I've had an  a homelab setup since 2016 much in a hobbist use case till this last year. My homelab setup started with a Raspberry pi 3 for christmas in 2016 as I wanted to start using home assistant in my house. I still have the pi3 today and is now running klipper on my 3d printer.  After years of using an old laptop and older intel based desktops I got from second hand stores. I've finally invested in a proper NAS and purchased a four bay terramaster F4-424 NAS. It's been nice for once to have a off the shelf solution and not a hack together solution.  As I've transition the last year from using a homelab as a hobbist to a professional use case with my studies I thought it would be a good time to provide a basic walkthrough of my homelab setup.

## Hardware

As i mentioned before the main hub of my homelab setup got as major upgrade with the purchase of a four bay terramaster F4-424 NAS. it powered by the intel N100 series processor while not the most powerful processors out there. it delieves a good balenced of performance and engery efficiency. it currently has 8gb of DDR5 ram and an upgrade i hope to make this year is to increse it to 32gb. I currently have all 4 bays of the NAS populated with SATA SSD's with 2TB of mirrored storage available. This may sound merger compared to other homelabs, but I don't have a huge media server and really only using the NAS for file storage and a few VMs.Paired with the Terrmaster NAS is another N100 powered mini pc that is primarily used for my networking needs. finally the last main piece of hardware is my main desktop which is an M1 Mac Mini. I have paired it with an 27" Lg monitor. I hope to be able to upgrade this to the new M4 Mac Mini sometime this year.

## Software

My software choices are going to be controversial for some. the Terramaster came with their OS Terrmaster OS 5 preinstalled. I used it for about a week before I decided to do what many on youtube and the internet have done and install a third party software on the NAS. The Software I choose for this was Unraid. I had been using Proxmox for the last couple of years and enjoy the ease of use of it and it free price tag. However the terramaster was built to run off a usb drive from the factory and with this ability it made sense to use the internal usb port in the system to house the unraid install. as I wouldn't have to sacrifice any of the SATA drives space for the OS like i would in a Proxmox or Truenas setup. this is without it challenges however. Unraid is a challenge when using a share as as timemachine destination with backups from my Mac Mini. many time after a couple days it would just stop working. this has supposedly been fixed in the new unraid Version 7 release but i haven't had time to test it yet and was still having issues when using the releasse candidate.

As i mentioned in the hardware section the secondary piece of my homelab is a mini pc that is primarily used for my networking needs. Once again controversial choice in software here as well as I choose to run OPNsense over PFSense. I have used PFSense in the past and it is a great piece of software but has a documented issue with realtek network cards. the mini pc I purchased came with a dual 1gb realtek network card. This presented problems getting PFSense to work out of the box where OPNsense would work just fine. i come to actually perfer OPNsense in some ways over PFSense only being the ease of seting up MFA and the ability to install plugins on system such as the unifi controller for my switches and adguard for my ad blocking needs.

## Setup

I have taken the last year to try and make my homelab as simple as possible hence why I like Unraid UI. i run most of my homelab service on my nas in docker containers and with the exception of a few all of my services are running from the Unraid community store with just a few docker compose files. the ability to simply hit update when a update is available for services in unraid is a huge plus verses the other solutions I've had in the past where I used Proxmox with a vm from docker or using the great proxmox scripts repo to run services that still required to post a line of code in each container to update the service.


## Conclusion

I've been using a homelab setup for a while now. I've been using it for my personal projects and for my self study projects. with the exception of a few upgrades I would like to make this has served me well for the better part of the last year.
