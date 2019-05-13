# Hyde-Blog Extension

hyde-blog is an extension for [Hyde]() that adds static blogging functionality.

## Installation

Add hyde-blog to your `shard.yml` file

```yml
dependencies:
  hyde:
    github: hydecr/hyde
  hyde-blog:
    github: hydect/hyde-blog  
```

Activate the extension in your `config.cr`

```crystal
activate :blog do |blog|
  # Configure the extension here
end
```

## Configuration

#### prefix

The base path for your blog defaults to the site root, but that can be overridden with the prefix option.

```crystal
# Will set the blog path to {{base_url}}/blog
blog.prefix = "blog"
```

#### permalink

The permalink for viewing your blog posts. Ideally this should be set once and then left alone, otherwise you kind of lose the perm part of permalink.

```crystal
# All configuration values are available here, as well as year, month,
# and day which are parsed from the `date` field.
blog.permalink = "{year}/{month}/{day}/{title}.html" 
```

#### pretty_urls

You might also consider enabling the pretty urls feature if you want your blog posts to appear as directories instead of HTML files.

```crystal
blog.pretty_urls = true
```

#### layout

Set the layout to be used for blog posts.

```crystal
blog.layout = "blog_layout"
```

#### taglink

Set the path at which you can find articles tagged with a particular tag.

```crystal
blog.taglink = "tags/{tag}.html"
```

## Contributing

1. Fork it (<https://github.com/your-github-user/hyde-blog/fork>)
2. Create your feature branch (`git checkout -b my-new-feature`)
3. Commit your changes (`git commit -am 'Add some feature'`)
4. Push to the branch (`git push origin my-new-feature`)
5. Create a new Pull Request

## Contributors

- [Chris Watson](https://github.com/your-github-user) - creator and maintainer
