# ChatOps + Ansible = AwesomeOps

!

@AgentO3

@VividCortex

\#DevOpsCV

## ChatOps 30s or Less

!

## Command Evolution

!

## Explicit Path

!


ansible-playbook -i dev \
<br/>
path/to/playbooks/do-stuff.yml \
<br/>
-e "foo=bar fiz=buz"

!

ansible-playbook -i dev \
<br/>
<span class="highlight">path/to/playbooks/do-stuff.yml</span> \
<br/>
-e "foo=bar fiz=buz"


!

## Via Tags

!

ansible-playbook -i dev \
<br/>
plays.yml \
<br/>
-t do-stuff \
<br/>
-e "foo=bar fiz=buz"

!

ansible-playbook -i dev \
<br/>
<span class="highlight">plays.yml</span> \
<br/>
-t <span class="highlight">do-stuff</span> \
<br/>
-e "foo=bar fiz=buz"

!

```
# plays.yml

include: path/to/playbooks/do-stuff.yml
...

# do-stuff.yml

hosts: stuff-servers
tags: ["do-stuff"]
...
```

!

![Not Bad](http://fs181.www.ex.ua/show/47847299/47847299.png)

!

## Let's Make It Awesome

!

ansible-playbook -i dev \
<br/>
plays.yml -t do-stuff \
<br/>
-e "foo=bar fiz=buz"

!

ansible-playbook -i <span class="highlight">dev</span> \
<br/>
<span class="highlight">plays</span>.yml -t <span class="highlight">do-stuff</span> \
<br/>
-e "<span class="highlight">foo=bar fiz=buz</span>"

!

## ChatOpsified

!

hubot plays do-stuff foo=bar fiz=buz

!

## Where's The Inventory?

!

hubot plays use dev

!

## SUPER HAPPY <br/> FUN DEMO TIME!!!

!

## Thanks DevOps RVA

[Fork It!!!](https://gist.github.com/AgentO3/574b103d205d7a70c167)
