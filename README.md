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

Variables and secrets :
-----------------------
1. env
variable for single work flow
env  
  can not be accessed with any other workflow
  so it is scoped
  we can define for job/ specific step
2. configuration variables
     can be used for multiple work flows
     defined in repositorysetting/organization/environment setting
3. context variables from github metadata
   based on condition we execute based on branch/environment/username
   so we get related to repo/job
   ${{ github.repository }}
   ${{ github.workflow }}
   ${{ github.trigger.actor }}
   https://docs.github.com/en/actions/reference/workflows-and-actions/contexts
  
