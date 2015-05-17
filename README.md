# Collections

This gem build a new Shared Collection (integration settgings) to be use in Cenit.

Cenit is an open source social platform as a service for data and business integration.

## Using cenit cmd

  cenit collection foo --user-name=Miguel --user-email=sanchojaf@gmail.com --github-username=sanchojaf


By default its possible read the options from `./gitconfig`

### Bootstrap a new collection

Before proceeding, take a minute to setup your git environment, specifically setup your name and 
email for git and your username and token for GitHub:

```bash
$ git config --global user.email johndoe@example.com
$ git config --global user.name 'John Doe'
$ git config --global github.user johndoe
$ git config --global github.token 55555555555555
```

Then you can only do.

   cenit collection foo
   
the-perfect-gem

### Structure

```
% tree
.
├── cenit-collection-foo.gemspec
├── Gemfile
├── .gitignore
├── .rspec
├── README.md
├── Rakefile
├── LICENSE
└── lib
    └── cenit
        └── collection
            └── foo
                 └── connections
                 └── webhooks
                 └── connection_sets
                 └── translators
                 └── events
                 └── flows
                 └── libraries
                 └── index.json
                 └── build.rb
                 └── version.rb
            └── foo.rb
└── spec
    └── cenit
        └── collection
            └── foo_spec.rb
    └── spec_helper.rb
    └── support
        └── samples
```

### Consider the next steps in your new collection repo

* Move to the new collection folder.

   cd my_collection

* Create a new git and related GitHub's repository

   rake create_repo
   
* Commit and push until you are happy with your changes, see a real example in https://github.com/cenit-hub/cenit-collection-twilio

* Generate a version

   rake version:write

* Tag and push release to git

  rake git:release

* Shared your collection in https://rubygems.org

  rake release

## About Cenit

### Why were doing this 

A common story for companies is the blending of solutions around its core business value. 
Features developed by them, third-party's adaptations and other SaaS to facilitate operations. 

Once grown enough a new expansion requires a huge integration effort. But available integration 
solutions are heavy process. Some of them also need B2B transactions using complex EDI standards 
required for large companies or business sectors.

This facts overkill many companies that can’t overcome these challenges.

### General Features

* 100% Open Source platform as a service (Open-PaaS).
* Hub with a great design that provides powerful yet simple abstractions, making a complex problem tractable.
* Primary concepts are: Data Type, Webhook, Flow, Event, Connection and Transform.
* Dynamic load schemas: XSD, JSON and EDI grammars.
* Powerful transform to translates and modified any formats to any format.
* Full Stack HTTP API and incremental API's helper libraries in several languages.
* Export and import integration settings (collections), and automatically saves its as a repo on github.
* Social networking features to share collections.

### Shared Collections

There are now over 25 pre-built shared integration collections out the box for connecting 
to internet services, fulfilment solutions, accounting, communications, ERP, multi-channels, etc.

### Join us

* Github project: https://github.com/openjaf/cenit
* Email: support@cenitsaas.com
* Website: http://www.cenitsaas.com
