# Docker Livereload

Build on Alpine.
Based on [node-livereload](https://github.com/napcs/node-livereload)

To use, add this to your `docker-compose.yml` file:
```yml
livereload:
  image: franckdelage/livereload
  ports:
    - "35729:35729"
  volumes:
    - /your/watch/directory:/usr/src/livereload-watch
```

It's possible to override the `command` to tell livereload to watch more additional file extensions

```yml
livereload:
  image: franckdelage/livereload
  command: "/usr/src/livereload-watch -u true -d --exts 'phtml,sass'"
```

> `--exts 'phtml,sass'` are additional file extentions. Check [Livereload Command Options](https://github.com/napcs/node-livereload#command-line-options) for more options.
