class: title

# Docker: The Good, The Bad, The Ugly

.center[
.image[![Docker Whale](https://www.docker.com/sites/default/files/d8/2019-07/Moby-logo.png)]
]

.left-column[

<p>By: James Johnson</p>
<p>Advisor: Professor Mesick</p>
]

---

## Overview

1. Containers vs VMs
2. Docker-Compose
3. Examples
4. Security Implications
5. Conclusion

---

layout: false

## Containers vs VMs

.left-column[
.image-small[![Container VM](https://www.nakivo.com/blog/wp-content/uploads/2019/05/Docker-containers-are-not-lightweight-virtual-machines.png)]
]
.right-column[

- What's a container?
  - '... a standard unit of software that packages up code and all its dependencies so the application runs quickly and reliably from one computing environment to another.' - Docker Docs
- How is it different from a VM?
  - a VM is a fully virtualized computer. This means it has its own OS, own kernel, etc. A container shares the kernel from the host machine it is on and does not run a full OS.
- Are containers better than VMs?
  - It's up to you. Containers are good for some things and VM are better in some areas
    ]

---

## Docker-Compose

.left-column[

- `docker-compose` is a tool used for creating multiple containers that are linked in a 'network'.
- This is very useful when orchestrating large scale applications and need to have detailed blueprints for how each container is created.
- The container structure is layed out in a way that is easy to understand and can be easily update later.
  ]

.right-column[
.image-medium[![Docker-Compose](https://sweetcode.io/wp-content/uploads/2018/12/Picture1-8.png)]
]

---

## Example Time

.left-column[

#### My Uses

- Plex Stack
  - Plex, Sonarr, Radarr, Lidarr, Transmission, Jackett, Organizr
- ELK Stack
  - Elastic Search, Logstash, Kibana
- Web Server
  - Nginx, MySQL, Node
- Home Automation

#### Real World

- CI/CD Pipeline
- Deployments
- Microservices
  ]
  .right-column[.image-small[![Docker Ship](https://miro.medium.com/proxy/1*rI1KYe0Qa2jLCFXao6Ti1g.jpeg)]]

---

## The Ugly

- There are few known vulnerabilities with Docker
  - The number of ways people take over Images and Containers keep growing
- Open and Unsecured
  - Many people leave the Docker host vulnerable by leaving port 2375 open with no security
  - There are instructions on Docker's website for how to secure it
- Worms
  - Graboid
  - Other Cryptomining Viruses

---

## Conclusion

- Docker can be great when used properly.
- There are a lot of understandable use cases and there are a lot of cases where people try 'just because'
- It still is new, there will be security flaws
