workflow 
  is nothing but pipeline
  .github/workflows

event:
  when workflow triggered activity takes place
job
  shell script
  is same as stages
runners:
  github hosted
  self hosted runners
action
  we can reuse the tasks, for example check out custom 

name: My first work flow

on:
  push: workflow trigger on a push event  on push event we can mention our branch default on main branch
  
jobs:
  build
    runs on: ubuntu-latest

    steps
    - uses actions/checkout@v3    checkout the code from the repository

    - run: echo "hello world"
