# AubRUG March Presentation

Today we'll make the first steps to deploying a Rails application.
We'll use the excellent [Rails Tutorial](https://www.railstutorial.org/book/)
by Michael Hartl as our basis, including using the
[Cloud9](https://c9.io/) development environment.


## Set up GitHub, Cloud9, and Heroku Accounts

To jump-start your foray into the Ruby language and the Ruby on Rails
web framework, I suggest setting up accounts on GitHub, Cloud9,
and Heroku. They're all free, so no worries. (Skip these if you already
have accounts.)

### GitHub

Many Rubyists use [GitHub](https://github.com/) to maintain their
projects. GitHub offers hosting for unlimited open-source projects, so you'll
often find yourself using Ruby libraries which are maintained on GitHub,
not to mention storing your own projects online as well. Do the following
to register:

* Visit <http://github.com>
* Enter a username, email, and password, and "Sign Up".
* Choose the Free plan, then "Finish sign up".
* Optional for EDU users: request a discount/free upgrade by visiting
  <https://education.github.com/>

If you decide you want a host that allows for free private projects,
I recommend [Bitbucket](https://bitbucket.org/) as an alternative.
(Actually, I use both for various projects.)

### Cloud9

Setting up Ruby and Ruby on Rails to work on your personal computer
is a pain compared to actually writing Ruby and Ruby on Rails code.
(Particularly if you're a Windows user.) So to get started, we'll
recommend using a cloud development environment: all you need to write
and deploy a Rails application is a modern browser.

* Visit <https://c9.io/> and click "Sign Up"
* Click the GitHub logo to sign up with your GitHub account, and click
  "Authorize Application".

### Heroku

To relieve the pain point of getting a web app which works in your
Cloud9 account (or your local development environment)
to also work on the internet, we'll use Heroku for deployment. By just
`git push`ing your code, it will automatically be provisioned and
hosted at `https://app-name.herokuapp.com`.

* Visit <http://heroku.com/> and click "Sign up for free"
* Enter a first name, last name, and email, and "Create Free Account"
* Confirm your account by clicking the link sent to your email.
* Create a password. Your username is your email address.


## Installing Rails in Your Cloud9 Environment

Since we'll be coding in Cloud9, let's set our workspace using
the instructions at
<https://www.railstutorial.org/book/beginning#sec-up_and_running>
(section 1.2). This will walk you through doing the following:

* Setting up a Cloud9 workspace for the tutorial
* Installing the Ruby on Rails framework using RubyGems.

By the way, RubyGems is the package manager which allows Rubyists to
easily install and use Ruby libraries which will keep you from
reinventing the wheel.


## Hello World!

Section 1.3
<https://www.railstutorial.org/book/beginning#sec-the_hello_application>
fulfills the time-honored tradition of getting a new language to display
"Hello World!":

* Using the `rails` command to scaffold a new application
* Using Bundler to manage your RubyGems
* Using the `rails server` command to host a local application
* Overviewing the Model-View-Controller (MVC) web development pattern


## Version Control with Git

You've got to get Git. Git is a distributed version control system which
will allow us to do the following (and more):

* Track changes as we edit code
* Back up our code on GitHub.com
* Provide sane workflows for collaborating with multiple people
  on the same code
* Easily allow us to push our application to the live internet

Follow Section 1.4 through 1.4.2 at
<https://www.railstutorial.org/book/beginning#sec-version_control>
to get started on:

* Installing Git
* Setting up a Git-tracked project

We will use GitHub instead of Bitbucket to host our git repo(sitory)
since it's more popular for hosting many of the libraries you'll use
as a Ruby programmer. *That said, the tutorial makes a good argument for using
Bitbucket, so you could use that instead if you'd prefer by following
[1.4.3](https://www.railstutorial.org/book/beginning#sec-bitbucket).*

We'll start by wiring up Cloud9 to securely talk with GitHub using
[SSH](http://en.wikipedia.org/wiki/Secure_Shell).

* Run `cat ~/.ssh/id_rsa.pub` to display your
  [public key](https://en.wikipedia.org/wiki/Public-key_cryptography).
  Copy it to your clipboard.
* Visit <https://github.com/settings/ssh> while logged into GitHub
  and click "Add SSH key".
* Use the label "Cloud9" (or whatever) and paste your public key into
  the field. Click "Add key".

Next we'll set up a repository on GitHub to store our code.

* Click the plus (+) sign in the top menu and click "New Repository".
* Name it `rails-tutorial`. Do NOT initialize the project with a README.
* Run the following code in Cloud9 to push your project to GitHub:
    ```
    foo
    ```

