---
ID: 224
post_title: 'New project: Patche — Single user easy repository'
author: Elliot Chandler
post_date: 2015-04-02 01:13:53
post_excerpt: ""
layout: post
permalink: >
  http://futuramerlin.com/news/2015/04/02/224-new-project-patche-single-user-easy-repository/
published: true
---
Turns out, according to <a href="http://textfiles.com/jason/">SketchCow</a> (<a href="https://web.archive.org/web/20150402005504/http://textfiles.com/jason/">IA</a>) (Jason Scott, Free Range Archivist at the Internet Archive) (#internetarchive on EFNet, 2015-04-01), the Internet Archive doesn't do well with more than about 500 files in a single item. So, git-annex putting my ~171,000 files into a single item <em>really</em> probably wouldn't work. Hence,

A new project:

"<big>Patche</big>".

It's not written yet.

[caption id="attachment_225" align="alignright" width="176"]<a href="http://futuramerlin.com/c/wp-content/uploads/2015/04/chibi_patche_by_jakly-d3fer12.png"><img class="size-medium wp-image-225" src="http://futuramerlin.com/c/wp-content/uploads/2015/04/chibi_patche_by_jakly-d3fer12-176x300.png" alt="I found this artwork (IA) (PNG (IA) by Jakly (IA) on DeviantArt of a character named Patche, which I'm including here for fun. I hope Jakly doesn't mind." width="176" height="300" /></a> I found <a href="http://jakly.deviantart.com/art/Chibi-Patche-207280982">this artwork</a> (<a href="https://web.archive.org/web/20150402004101/http://jakly.deviantart.com/art/Chibi-Patche-207280982">IA</a>) (<a href="http://fc06.deviantart.net/fs70/f/2011/122/a/8/chibi_patche_by_jakly-d3fer12.png">PNG</a> (<a href="https://archive.org/download/chibi_patche_by_jakly-d3fer12/chibi_patche_by_jakly-d3fer12.png">IA</a>) by <a href="http://jakly.deviantart.com/">Jakly</a> (<a href="https://web.archive.org/web/20150402004213/http://jakly.deviantart.com/">IA</a>)) (2 May 2011) on DeviantArt of a character named Patche, which I'm including here for fun. I hope Jakly doesn't mind.[/caption]

&nbsp;

Usage:

<tt>patche init passphrase authkey secretkey</tt> — Create a new repository from the current directory. A <tt>.pch</tt> bundle will be created in the current directory, containing the <tt>.pconf</tt> configuration file containing the passphrase, authkey, and secretkey, an empty <tt>.ptub</tt> (patch URL bundle) directory, and a <tt>.pshadow</tt> bundle containing a copy of the files in the current directory (including the aforementioned bundle and its contents). The <tt>.pinite</tt> template (created using an rsync patch file (<tt>rsync --write-batch=FILE</tt> (according to the rsync manpage dated "22 Jun 2014")) when copying to the <tt>.pshadow</tt> bundle) will be uploaded to the Internet Archive, and a <tt>.pinitu</tt> file will be created in the <tt>.ptub</tt> directory, containing the URL of the uploaded template.

<tt>patche clone foo/bar passphrase authkey secretkey</tt> — Create a new repository in the current folder using the template from <tt>https://archive.org/download/foo/bar.pinite</tt>, the encryption passphrase "passphrase", the authorization key "authkey", and the secret key "secretkey".

<tt>patche commit message</tt> — Uploads the changes since the last commit to the Internet Archive as a <tt>.patche</tt> file, with the optional commit message "message". Adds a <tt>.pchu</tt> file with the URL of the <tt>.patche</tt> file to the <tt>.ptub</tt> directory.

<tt>patche patch foo/bar</tt> — Merge the patch at <tt>https://archive.org/download/foo/bar.patche</tt> into the repository in the current directory.