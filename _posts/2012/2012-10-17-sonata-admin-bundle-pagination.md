---
layout: post
category: symfony
tags: [symfony, sonata-admin]
---

So today I had to find a way to configure/modify the SonataAdminBundle's pagination. My first tought was "let's ask about it on irc, there should be a quick, nice and easy way", yeah well there isn't. The method I found is quick and easy, but it's not really nice imho :) Basically you have to overwrite the listAction in your AdminController files, so if you have lots of entities then the quickness is gone.

Here's the modified action:
<script src="https://gist.github.com/3905984.js"> </script>

If you want some flexibility, you can set it up with a parameter, so
`$pager->setMaxPerPage(50);`<br>
will become something like this:
`$pager->setMaxPerPage($this->container->getParameter('items_per_page'));`

If you want to tweak the paginator some more, you can do it at the same way, the available functions are in the [Pager.php](https://github.com/sonata-project/SonataAdminBundle/blob/2.0/Datagrid/Pager.php), be sure to use them before the createView() is called.