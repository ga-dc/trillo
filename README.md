# Trillo!

This demonstrates the progression of Trillo from an HTML/JS/CSS site making requests to an external API, to a full-stack Rails app that makes AJAX requests to itself.

Each branch of this repo represents a different step in the process. See the progress made in each step by clicking the Pull Requests button to the right and "comparing" two different branches.

## Things to note:

- `respond_to`

- `javascript_include_tag` and `stylesheet_link_tag`

- `=require_tree .`

- Not using `localhost`

- The location of the `$(document).ready(function(){})` that "starts" the Javascript

- How the "precompile" step smushed all the stylesheets into one stylesheet, and all the Javascripts into one file. Note, too, that the file name contains a big, long, incomprehensible code. This is a "fingerprint", generated by the "Sprockets" Gem. `=require_tree .` is important here.

## Bear in mind

You can put ERB inside Javascript. For example, in a `.html.erb` file:

```
<div>
  <button onclick='$("#<%= @user.id %>").val("I like turtles.");'>Click me!</button>
</div>
```

You can also have `.js.erb` files inside your `views` directory. These are just like regular Javascript files but with ERB dynamically adding data from the Rails app into it.

However, use of these should be sparing, since it makes code very hard to maintain.
