Title: Erlang thread efficiency
Date: 2010-04-15 1:29
Category: Tech
Tags: tech, programming
Slug: java-erlang-threading
Author: Vaibhav Mishra
Summary: Erlang thread advantage over Java


<div dir="ltr" style="text-align: left;" trbidi="on">
Java is a great language, personally I prefer python and bash for scripting and none of my script goes more than 20 lines so it is not really a benchmark but recently I got a chance to modify a script written in Java, or must I say optimize it, I did my homework and look for several approaches, since it is a thread based application some of the solution I found is<br />
<ol>
<li>Use <a href="http://jcp.org/en/jsr/detail?id=1">real time system</a> - this does not work out because Ubuntu 10.04 real time kernel doesnot play nice and I am too egoist to go for previous version.</li>
<li>Increase hardware - since my real options are only in the clouds hnce effectively VM which generally zeroed the effect of increasing hardware so this also fell off.</li>
<li>Use some real skills -- I did some digging around and increase the performance of script by remove just 2 characters, and that did it, it was flying high in the test environment and I thought I finished or did I...</li>
</ol>
There lies a twist , it turns out Java Have a limit on number of threads it can create, before running out of memory or some other bullshit limit and believe me I tried really hard to figure ut optimization , even remove all the code from the thread and simply putting it to sleep, but I hit the wall, 5000 threads, 5092 to be precise.<br />
and in production my script fails.<br />
<br />
so the obvious solution was to run script simultaneously in several JVMs which would require several machines or at least one super- machine , or change the language, and believe me I didn't like this, but this was a special case , so I turned to option of using other language , few options are<br />
<br />
<ul>
<li>C or <a href="http://en.wikipedia.org/wiki/Native_POSIX_Thread_Library">NPLT which is essentially C</a>-- this was good, really awesome , great performance promises like spawning 100000 threads in 2s ,but really it is C, memory management etc., so I put it as a last resort.</li>
<li>erlang - This comes out to be seemingly more viable solution , since it is more high level, a language of new paradigm so perfect for learning and also tailor made for concurrency.</li>
</ul>
naturally <a href="http://erlang.org/">Erlang</a> is the choice , but it seems to have a huge learning curve, everything is different but still , it seems far more elegant than C, and promises to create greater than 32000 threads in action with no seemingly achievable upper limit. let's hope this goes well.</div>
