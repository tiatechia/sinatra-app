# Sinatra

Up to this point, we have been working with a database that exists only on your computer.  Active Record helped us quickly set the database up and interact with it using ruby instead of SQL.

But ideally, we want end users to be able to query the database and (maybe, if they have permission) create, update, and delete records.

We could handle that distribution/access problem in a few ways, but in this case, we will be setting up a web server that will allow users to access the database using http requests.  Our end users will request a web page, like: 'somedomain.com/users', and our server will return a web page which lists the users in our database.

For now, this server will be a local server that can only be accessed in our Cloud 9 workspace, because we are still in development.  Instead of having a domain like `google.com`, we will have a local domain: `localhost`, and we will specify the port number.  We will be using a very light ruby web freamwork called Sinatra, and Sinatra uses port 4567, so a full domain might look like: `localhost:4567/users`.

We will learn more about http requests, servers, and how the internet works next week.

##Today, let's spin up Sinatra and see what it does.

Follow the steps below to set up your environment.

1. Log into GitHub and fork this repo to your own account.
1. Click the clone or download link and copy the ssh clone name.  (Toggle between https and ssh until you see Clone with ssh indicator.)
1. In a folder on your computer, open the Windows command prompt and type `git clone ` and then paste the name of the repo you copied.  It might look like `git clone git@github.com:Gmfholley/sinatra-app.git`.
1. Change your directory into the folder you just made: `cd sinatra-app`.
1. At the prompt type `ruby --version ` to ensure Ruby is installed.
    1. If you get an error that states Ruby is not found, you will need to [install Ruby](https://rubyinstaller.org/downloads/). You must be an administrator on the computer to install Ruby. In general, download the recommeded Ruby version on the page. Once installed, reopen your command prompt.
    1. If you continue to get an error after installing Ruby, you will need to make sure Ruby is located on your Windows PATH (directories where Windows looks to run commands without specifiying the full path). To add Ruby to your path, you can either do so in bash or at the command prompt.
        1. BASH:
        1. Command prompt: 
    **@todo In a bash shell: echo $PATH, which gem, export PATH=$PATH:/c/Ruby25-x64/,echo $PATH
    ** In the command prompt: 
    **for psql, will need to find the folder and add the path OR run the full path
1. Type `gem install bundler` to install the Ruby bundler gem.
1. Type `bundle install` to install all the gems for this repo.
    1. If you get a message regarding updating bundler or another gem, run the command given to you for upgrading, e.g.: `bundle update --bundler`.

##Now you're ready to get started.

1. [Test your setup](./set_up.md)
1. [Set up Models](./set_up_models.md)
1. [Add validations](./add_validations.md)
1. [Run server](./serve_your_data.md)
1. [Create layouts](./create_layouts.md)
1. [Set up a restful route](./create_restful_route.md)
1. [Add hearts to tweets](./hearting_tweets.md)
1. [Handle errors](./handling_errors.md)