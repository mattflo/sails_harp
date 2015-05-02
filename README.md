# Harp + Sails
The goal of this exercise was to use harp’s convention based pre-processing pipeline alongside
sails convenient json/rest capabilities. Having it all run in one express app
is also convenient for deployment and for not having to deal with cross origin
request issues.

I couldn’t find any examples of this in the wild, so I wanted to share it. The most
important bits can be found in this [commit](https://github.com/mattflo/sails_harp/commit/54fbc1457c67c015811196fe3f246b9a445cb3f8).

## Prereqs

1. node and npm
2. harp `npm install -g harp`
3. sails `npm install -g sails`

## Try it out

1. `git clone https://github.com/mattflo/sails_harp`
2. `cd sails_harp`
3. `sails lift`
4. `open http://localhost:1337`

## Steps

* create a new sails app `sails new my_new_sails`
* change to your new director `cd my_new_sails`
* create a public directory for harp `mkdir public`
* initialize your harp application `cd public && harp init`
* add harp and express to package.json and configure the middleware in `config/http.js`. see this [commit](https://github.com/mattflo/sails_harp/commit/54fbc1457c67c015811196fe3f246b9a445cb3f8).

## Sources
* http://harpjs.com/docs/environment/lib
* http://sailsjs.org/#!/documentation/concepts/Middleware
