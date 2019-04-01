## How to...

### Running locally
```
$ git clone git@github.com:emi-fukuta/carte-custom.git
$ cd carte-custom
$ bundle install --path vendor/bundle
$ bundle exec jekyll serve --watch
```

You can view API specifications by accessing localhost: 4000.
Also, changes will be reflected automatically.


### Adding a new API call

You can add a new API call by simply adding a new post in the `_posts` folder. Jekyll by default forces you to specify a date in the file path: it makes us sad pandas too, but you'll have to stick to this format. You can use dates to control the order in which API calls are displayed in the interface.

Each API call can define a few values in its YAML header:

Variable | Mandatory | Default | Description
--- | --- | --- | ---
``title`` | Y | - | A short description of what that calls does.
``urlpath`` | N | - | The URL for the API call, including potential parameters.
``type`` | N | - | Set it to `PUT`, `GET`, `POST`, `DELETE` or nothing (for parts of your documentation that do not relate to an actual API call).

A typical header:

```
---
urlpath: '/stuff/:id'
title: 'Delete a thing'
type: 'DELETE'

layout: null
---
```

We then describe the request and response (or whatever else you wish to talk about) in the body of our post. Check the placeholders present in the `_posts` folder to get an idea of what it can look like.

### Grouping calls

Adding a category to your YAML header will allows you to group methods in the navigation. It is particularly helpful as you start having a lot of methods and need to organize them. For example:

```
---
category: Stuff
urlpath: '/stuff/:id'
title: 'Delete a thing'
type: 'DELETE'

layout: null
---
```

### Edit the design

The default UI is mostly described through the `css/style.css` file and a couple short jQuery scripts in the `/_layouts/default.html` layout. Hack it to oblivion.


### Reference

[Carte](https://github.com/Wiredcraft/carte)

