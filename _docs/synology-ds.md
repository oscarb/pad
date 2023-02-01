---
title: Synology DiskStation guide v2
tags:
  - nas
published: true
---

# Synology DiskStation guide v2

* TOC
{:toc}

## Docker without sudo 


Test line break  
continues on a new line...  
or...? 

Test not 
continue 
on new line

Create a group called `docker`  

	sudo synogroup --add docker
    
Add current user to group  

	sudo synogroup --member docker $USER
    
Change ownership of `docker.sock` 

	sudo chown root:docker /var/run/docker.sock
    
    
[Source](https://davejansen.com/manage-docker-without-needing-sudo-on-your-synology-nas/)