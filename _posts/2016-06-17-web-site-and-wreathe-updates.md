---
ID: 2795
post_title: Web site and Wreathe updates
author: Elliot Chandler
post_date: 2016-06-17 15:34:54
post_excerpt: ""
layout: post
permalink: >
  http://futuramerlin.com/news/2016/06/17/2795-web-site-and-wreathe-updates/
published: true
---
Following up on <a href="http://futuramerlin.com/c/2016/02/24/2767-important-update-for-wreathe-os-users/">the previous post on the Wreathe GNU/Linux distribution</a>:
<ul>
 	<li>No Wreathe versions except <em>Wreathe 5: Rain</em> and <em>Wreathe 7r2: Elegy</em> are currently supported; users running other versions of Wreathe are advised to update to <em>Wreathe 7r2: Elegy</em>.</li>
 	<li><em>Wreathe 5: Rain</em> support will end 1 October 2016; users currently running <em>Wreathe 5: Rain</em> are advised to update to <em>Wreathe 7r2: Elegy</em> before that date.</li>
 	<li><em>Wreathe 7r3: Elegiac</em> is now being actively developed, and will be based on the Gentoo GNU/Linux distribution. Driver issues are currently blocking development (the OS crashes before boot completes when using the proprietary NVIDIA drivers).</li>
</ul>
Regarding the Futuramerlin Web site:
<ul>
 	<li>A new design went live on 6 March 2016.</li>
 	<li>User acceptance feedback indicates that the new design is suboptimal.</li>
 	<li>The new design renders the Web site unusable in current versions of the Konqueror Web browser (the menu covers the page content).</li>
 	<li>I plan to change the way the design is implemented so that all browsers are served a basic HTML page, and then JavaScript is used for visual styling in browsers that support it. This should make most or all users able to access the Web site's content, but will detrimental effects as follow:
<ul>
 	<li>Users with JavaScript disabled and a browser that supports the site's CSS will see an un-styled version of the site.</li>
 	<li>Users with JavaScript whitelisting may be prompted to enable JavaScript for the site, even though using the site does not require JavaScript.</li>
</ul>
Unfortunately, I do not know how to resolve those two issues without making the Web site harder to use on mobile computers.</li>
 	<li>I may change some aspects of the design, or make it customisable, to increase user acceptance.</li>
</ul>
General updates:
<ul>
 	<li>I plan to add a publicly-accessible issue tracker to the Web site, or configure <a href="http://futuramerlin.com/d/s/mantis/">the existing login-only Mantis installation</a> to allow search engines to index it.</li>
</ul>