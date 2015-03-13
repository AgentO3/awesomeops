# Evolution Of The Ansible Commands

!

## Explicit Paths

!

ansible-playbook -i dev path/to/playbooks/do-stuff.yml -e "foo=bar fiz=buz"

!

## Top Level Playbooks

!

project
> playbooks
> > roles
> > do-stuff.yml
> plays.yml
> dev

!

- include: playbooks/do-stuff.yml tags=do-stuff
  vars:
    foo: bar
    fiz: buz

- include: playbooks/something-else.yml tags=something-else
  vars:
      foo: buz
      fiz: bar

!

## Using Tags

!

ansible-playbook -i dev plays.yml -t do-stuff -e "foo=bar fiz=buz"

!

## Not Bad But I Think We Can Do Better

!

ansible-playbook -i <span>dev</span> <span>plays</span>.yml -t <span>do-stuff</span> -e "<span>foo=bar fiz=buz</span>"

!

## ChatOpsified

hubot plays do-stuff foo=bar fiz=buz

!

## Where Did The Inventory Go?

!

## Hubot Haz Brainz

!

hubot plays use dev

!

## This is my inventory. There are many like it, but this one is mine.

!

## SUPER HAPPY FUN DEMO TIME!!!
