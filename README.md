openshift-nodejs-todos
======================

Fork and rework of the excellent backbone boilerplates example option 1 to allow
it to run on Openshift.

Uses MongoDB and Express on top of Node.js, with a Backbone.js powered front
end. Forked from https://github.com/addyosmani/backbone-boilerplates

Currently has some issues with binding to the wrong port - it needs to be setup
to use the environment variable Openshift provides to identify which port is ok.

Installation
------------

Create an Openshift account and setup a Node.js project using their template.
Install a MongoDB cartridge to this project and then copy the code into your
Openshift repo, or add it as an upstream master as they describe in the FAQs.

Then edit server.js to point to your Mongo installation, and solve the above
issue by putting in the env var, either during a build hook, or by finding it
out and hardcoding it.