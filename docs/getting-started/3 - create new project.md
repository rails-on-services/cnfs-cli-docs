---
id: Creating a new Project
sidebar_position: 3
---

The best way to read this guide is to follow it step by step. All steps are essential to run this example
 application and no additional code or steps are needed.

By following along with this guide, you'll create a CNFS project called blog, a (very) simple set of infrastructure
for a weblog. Before you can start building the application, you need to make sure that you have CNFS itself installed.

:::tip
The examples below use $ to represent your terminal prompt in a UNIX-like OS, though it may have been customized to
 appear differently. If you are using Windows, your prompt will look something like C:\source_code>.

:::

## Installing Cnfs

Before you install CNFS, you should check to make sure that your system has the proper prerequisites installed. These include:

- Ruby
- SQLite3

### Installing Ruby

Open up a command line prompt. On macOS open Terminal.app; on Windows choose "Run" from your Start menu
 and type cmd.exe. Any commands prefaced with a dollar sign $ should be run in the command line.
 Verify that you have a current version of Ruby installed:

```shell
$ ruby --version
ruby 2.7.0
```

CNFS requires Ruby version 2.7.0 or later. It is preferred to use latest Ruby version.
If the version number returned is less than that number (such as 2.3.7, or 1.8.7), you'll need to install a fresh copy of Ruby.

To install Rails on Windows, you'll first need to install [Ruby Installer](https://rubyinstaller.org).

For more installation methods for most Operating Systems take a look at [ruby-lang.org](https://www.ruby-lang.org/en/documentation/installation).

### Installing SQLite3

You will also need an installation of the SQLite3 database. Many popular UNIX-like OSes ship with an 
acceptable version of SQLite3. Others can find installation instructions at the SQLite3 website.

Verify that it is correctly installed and in your load PATH:

```shell
$ sqlite3 --version
```

The program should report its version.

### Installing CNFS

To install CNFS, use the gem install command provided by RubyGems:

```shell
gem install cnfs-core
```

To verify that you have everything installed correctly, you should be able to run the following in a new terminal:

```shell
$ cnfs --version
```

If it says something like "Cnfs 0.1.0", you are ready to continue.


## Creating the Blog Application

CNFS comes with a number of scripts called generators that are designed to make your development life easier 
by creating everything that's necessary to start working on a particular task. One of these is the new 
application generator, which will provide you with the foundation of a fresh CNFS application so that 
you don't have to write it yourself.

To use this generator, open a terminal, navigate to a directory where you have rights to create files, and run:

```shell
cnfs new blog
```

This will create a CNFS application called Blog in a blog directory and install the gem dependencies that are 
already mentioned in Gemfile using bundle install.

:::info

You can see all of the command line options that the CNFS application generator accepts by running `cnfs new --help`.

:::

After you create the blog application, switch to its folder:

```shell
$ cd blog
```

The blog directory will have a number of generated files and folders that make up the structure of a CNFS application.
 Most of the work in this tutorial will happen in the segments folder, but here's a basic rundown on the function 
of each of the files and folders that Rails creates by default:

```shell
/home/admin/projects/scratch/pr1
|-- Gemfile
|-- Gemfile.lock
|-- README.md
|-- app
|   |-- controllers
|   |   `-- pr1
|   |       `-- concerns
|   |-- generators
|   |   `-- pr1
|   |       `-- concerns
|   |-- models
|   |   `-- pr1
|   |       `-- concerns
|   `-- views
|       `-- pr1
|           `-- concerns
|-- config
|   |-- application.rb
|   |-- boot.rb
|   |-- environment.rb
|   |-- initializers
|   |   `-- logging.rb
|   `-- segments.yml
|-- lib
|   `-- cnfs
|       `-- extension.rb
|-- segments
|   |-- backend.yml
|   |-- builders.yml
|   |-- dependencies.yml
|   |-- frontend
|   |-- frontend.yml
|   |-- images.yml
|   |-- plans.yml
|   |-- production.yml
|   |-- providers.yml
|   |-- provisioners.yml
|   |-- repositories.yml
|   |-- resources.yml
|   |-- runtimes.yml
|   |-- services.yml
|   |-- staging.yml
|   `-- users.yml
`-- src

```
