# Rails as an API Study

Use your favorite search engine and the provided readings to research and answer
the following questions (no prior knowledge is expected).

In your answers, be sure to cite any relevant sources you consulted in your
search. We ask you to write answers in your own words in order to see how you
process what you've read. Please do not answer with direct quotes from source
material. Instead, digest what you've read and repeat it in your own voice.

Please note:

-   Many of the readings will mention the "view" layer. We won't be covering the
    view layer in this program.
-   We'll use our [rails-api-template](https://github.com/ga-wdi-boston/rails-api-template)
    repository as the basis for our rails applications.
    This template excludes the "view" layer.

## Required Readings

-   [Starting Ruby on Rails: What I Wish I Knew | BetterExplained](http://betterexplained.com/articles/starting-ruby-on-rails-what-i-wish-i-knew/)
-   [Intermediate Rails: Understanding Models, Views and Controllers | BetterExplained](http://betterexplained.com/articles/intermediate-rails-understanding-models-views-and-controllers/)
-   [Getting Started with Rails — Ruby on Rails Guides](http://guides.rubyonrails.org/getting_started.html)
-   [The Rails Command Line — Ruby on Rails Guides](http://guides.rubyonrails.org/command_line.html)
-   [Rails Routing from the Outside In — Ruby on Rails Guides](http://guides.rubyonrails.org/routing.html)
-   [Action Controller Overview — Ruby on Rails Guides](http://guides.rubyonrails.org/action_controller_overview.html)

## Define Model Responsiblities

In your own words, define what the responsibilities of the model layer are in
Rails.

```md
Models are Ruby classes. They communicate with the database, store and validate
data. Models contain the data for the application, the state of the application
and all the business logic. It notifies the View of the state changes. In short,
Model is the data structure that your program uses.
```

## Define Controller Responsiblities

In your own words, define what the responsibilities of the controller layer are
in Rails.

```md
The controller layer in Rails receives an HTTP request and translates it into
a command the application can understand. It acts as a translator between the
language of HTTP and the language of your application, or model layer.
The controller also translates the results of your application(the model layer)
to the language of HTTP.
The second responsibility of a controller is authorization. Based on the
incoming HTTP request, it decides whether to pass the action on to the model
layer or deny the request.
```

## Define Router Responsiblities

In your own words, define what the router does in Rails.

```md
The Rails router recognizes URLs and dispatches them to a controller's action.
It also generates paths and URLs.
When an HTTP request arrives from the user's browser, it needs to know which
controller action should be run. It looks at the HTTP verb and the URL that it
being requested and matches it with the appropriate controller action to run.
```

## The Request-Response Cycle in Rails

Starting with a client making a GET request to a particular URL, describe how
the parts of Rails interact to produce and send a response.

```md
1. A user opens his browser, types in a URL, and presses Enter.
2. When the user presses Enter, the browser sends a GET request for that URL.
3. The GET request hits the Rails router. The router maps the URL to the
   correct controller action to handle the request.
4. The action receives the GET request and passes it on to the view.
5. The view renders the page as HTML.
6. The controller sends the HTML back to the browser.
   The page loads and the user sees the page with the form.
```
