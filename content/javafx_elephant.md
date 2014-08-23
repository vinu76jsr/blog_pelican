Title: We got elephant out, now what to expect in JavaFX 1.3/1.5(post-marina)
Date: 2009-03-7 7:58
Category: Programming
Tags: programming, javafx
Slug: javafx-1-5
Author: Vaibhav Mishra
Summary: JavaFX 1.5


<div dir="ltr" style="text-align: left;" trbidi="on">
<div style="text-align: justify;">
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; The title is inspired from Jim Weaver's post on JavaFX, I here present what's new we get in Marina(JavaFX 1.2) and what should be there in next iteration, but first some background.</div>
<div style="text-align: justify;">
I followed <a href="http://www.javafx.com/">JavaFX</a> from it's version 1.0, heard the news here and there about it got a little exited ,tried using Jim Weaver's book somewhere in mid-2008 but dropped because the text is obscure and the technology has come a long way, after that Sun promoted it as a great RIA tech(I don't know time before because I was not following it) and with it's version 1.0 it was good but not great , a promising technology but lack of component still does not make it much worthy,</div>
<div style="text-align: justify;">
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; I got pretty excited about this language because <a href="http://weblogs.java.net/blog/spericas/archive/2009/02/as_many_of_you.html">of this</a> . here's also pic, I probably a, not a good gamer and my scores reflect that</div>
<div class="separator" style="clear: both; text-align: justify;">
<a href="http://2.bp.blogspot.com/_8IgrExDrA8Y/Sk4R5BnNwVI/AAAAAAAABzw/lk2heBsU9fk/s1600-h/Screenshot-JNebulaFx.png" imageanchor="1" style="clear: left; float: left; margin-bottom: 1em; margin-right: 1em;"><img border="0" src="http://2.bp.blogspot.com/_8IgrExDrA8Y/Sk4R5BnNwVI/AAAAAAAABzw/lk2heBsU9fk/s320/Screenshot-JNebulaFx.png" xj="true" /></a></div>
<div style="text-align: justify;">
They promised of providing components&nbsp;in a later iteration, then comes version 1.1 , the big thing was Mobile support but not something which make someone like me with a short attention span to get very excited, but I drilled the language syntax(the JavaFX script language ) because&nbsp;of this <a href="http://www.weiqigao.com/blog/2008/12/11/javafx_1_0_on_linux_netbeans_plugin.html">entry</a>&nbsp;(Thanks Mr. Weiqi Gaofor that)and had a few custome application component up and running for quite a some time just for learning purposes, the platform was not <a href="http://jonathangiles.net/blog/?p=374&amp;cpage=1#comment-31446">much&nbsp;stable</a> (at least&nbsp; the smarter ones say and I observed <a href="http://www.bloggingaboutjava.org/cms/wordpress/2008/01/scripting-the-java-platform/#comment-30772">here</a> and <a href="http://xwisdomhtml.com/javafx-vs-air.html">there</a>) but it still provides a smaller learning curve, and that was really great, I heard the complaints from the community about having to learn another language, but I am just a student and probably will like to stay like this because now I had not to worry about these things , I am free to choose whatever I want to learn and I did it, maybe those people were justified or maybe not but I am not in a position, neither did I have the credibility to pass judgement . </div>
<div style="text-align: justify;">
I even started some fun project in the beginning just for learning, here is one of them and as a matter of fact it is currently compiling well with JavaFX 1.2 installed but was made in 1.1 era</div>
<div style="text-align: justify;">
<b>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; TennisFX</b> -here is the pic it i what it shows here nothing functional when I shelved it knwing it'll require lot of game mathematics and I don't know some stuff which I was not good at the time.</div>
<div class="separator" style="clear: both; text-align: justify;">
<a href="http://2.bp.blogspot.com/_8IgrExDrA8Y/Sk4TowH2MAI/AAAAAAAABz4/3UDtHHKQrvI/s1600-h/Screenshot-Tennis+FX%21.png" imageanchor="1" style="margin-left: 1em; margin-right: 1em;"><img border="0" src="http://2.bp.blogspot.com/_8IgrExDrA8Y/Sk4TowH2MAI/AAAAAAAABz4/3UDtHHKQrvI/s400/Screenshot-Tennis+FX%21.png" xj="true" /></a></div>
<div class="separator" style="clear: both; text-align: justify;">
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; Then the date of <a href="http://java.sun.com/javaone/">JavaONE</a> approach, I like these things(although I don't understand much) and have over 3GB worth of tech talks downloaded in my system through <a href="http://www.parleys.com/">Parleys</a> and tried my luck with 'Dude <a href="http://java.sun.com/javaone/2009/contest/">where's my pass' contest</a> (I must say <a href="http://www.youtube.com/watch?v=4I7oGbVruio&amp;feature=player_em">my video</a> was embarrasing , I was wearing Vest and it didn't look good , that and some unworthy voice acting to press content into stipulated 30seconds contributed to my demise), and as expected I got bumped but, that was fun, tried my hand in JavaFX programming contest, this is my application as it look the night before the submission date( sorry I couldn't pass the screenshot because it needs to be updated to JavaFX 1.2), I could not submit because of some media component bug at the last minute(or I must say last 4 hours, and was totally my fault) but it was a great experience (the idea was huge but I lacked the resources, time, and most importantly experience required but that's another story, ), 3days after we got the <a href="http://java.sun.com/javafx/1/reference/releasenotes/production-suite-release-notes-1-2.html">Marina release</a>(JavaFX 1.2 was codenamed Marina)</div>
<div style="text-align: justify;">
Marina release was great, it bridged the huge gap, provided a leap in terms of components, Caspian was great and layouts(although JFXtras is doing great in that department, but it good to have a great thing out of the box) let me give you a feel of what they did and what should be next.</div>
<div style="text-align: justify;">
<b>1.</b><a href="http://fxexperience.com/2009/06/caspian-skin/"><b>Project Caspian</b></a> – I didn't know it is a separate project or what but it really is great, it is the name of Look and feel we get out of box, it look lean and attractive and provided a better alternative then what we have in Swing(In the attractiveness department, I didn't know much about stability), if it is good enough in technical terms I suggest it to be included in Swing but, just a request , you're free to ignore, I didn't mind and Swing have very good L&amp;F available like Substance and others, so that is covered up.</div>
<div class="separator" style="clear: both; text-align: justify;">
<a href="http://3.bp.blogspot.com/_8IgrExDrA8Y/Sk4WpAoKqYI/AAAAAAAAB0A/WyAXNjgvC1I/s1600-h/button.png" imageanchor="1" style="margin-left: 1em; margin-right: 1em;"><img border="0" src="http://3.bp.blogspot.com/_8IgrExDrA8Y/Sk4WpAoKqYI/AAAAAAAAB0A/WyAXNjgvC1I/s400/button.png" xj="true" /></a></div>
<div style="text-align: justify;">
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; I am farely content with this one.</div>
<div style="text-align: justify;">
<b>2.The component set</b> – it is much better then perhaps having nothing(that's what we had in version 1.1 , that TextBox thing was not properly documented), a fairly good list including Progressbar , button, scrollbar(it is a welcome addtion, it's a paint to implement it yourself) and other traditional ones.</div>
<div style="text-align: justify;">
What it lacks is a good component to provide Data representation, Joshua Marinacci showed a<a href="http://jfxstudio.wordpress.com/2009/06/20/a-custom-virtual-list/"> lazy list</a> version of data representation so we're expecting something on the line in next version, listview will suffice till then , also if some receptive one are hearing there is a problem with hyperlink control launching browser , that's a fundamental thing if you're talking about hyperlink, however we get a pretty rich control set in terms of 0.1 version increase. </div>
<div style="text-align: justify;">
<b>3.RSS support </b></div>
<div style="text-align: justify;">
It came up early and <a href="http://blogs.sun.com/rakeshmenonp/entry/javafx_rss_and_atom_task">came up good</a>, ask a beginner like me who again with lack of much experience delved into lines of Rome Library(it is good but not beginner freindly), I don't care if this is inspired by Rome or what but this brings in very good support I must say in terms of out of the box functionality.</div>
<div style="text-align: justify;">
I have nothing to complain about here because it is more that what I(or I must say almost anybody else ) expected.</div>
<div style="text-align: justify;">
<b>4.Charting support</b></div>
<div style="text-align: justify;">
This release bring out Charting support , good first hand approach , some said it is inspired by JfreeChart, I had used JfreeChart for a while and it simply didn't matter, Charting support is always welcome, due to it's impact for business users it deserves special treatment.</div>
<div style="text-align: justify;">
This is another good thing, just evolve it more.</div>
<div style="text-align: justify;">
<b>5, Runtime improvement</b></div>
<div style="text-align: justify;">
This is the huge thing (or I must say only thing because Project Caspian bring on a huge change into paradigm) if JavaFX had to be a success in Desktop and browser and they're slowly approaching that persona. But.....</div>
<div style="text-align: justify;">
I have a huge request, I didn't if you guys are right person to ask for it but please let the plugin load asynchronously in the browser, I don't want my browser to hang each time I load a web page with Java content, this is more of a generic request but can hinder JavaFX acceptance for browser.</div>
<div style="text-align: justify;">
<b><a href="http://blogs.sun.com/dwarak/entry/using_persistence_in_javafx">6.Persistence storage</a></b></div>
<div style="text-align: justify;">
Java have a<a href="http://javablog.co.uk/2007/10/25/persistence-options-in-java-part-1-local-filesystem/"> myriad of persistence option available</a>(try the <a href="http://my.safaribooksonline.com/9780768680591">book by IBM guys</a> if you want to have deeper look) and this iteration of JavaFX support this with introduction of persistence storage mechanism in JavaFX, works great for small things and a nice improvement.</div>
<div style="text-align: justify;">
We need a supported embedded database technology, I know we have Derby or JavaDB(although they're one and the same thing almost) but something more smaller, may be DerbyLite in the line of SQLlite with less functionality( a smaller support base in terms of SQL language) or why go relational, get something in the line of Bigtable, call it smalltable and just make it small.</div>
<div style="text-align: justify;">
And for what should be(or maybe) done in later iteration of JavaFX(besides those requested above), just requesting if someone is hearing</div>
<div style="text-align: justify;">
1. Lose that security dialog box, <a href="http://code.google.com/p/pulpcore/">others did it</a>&nbsp;, I know that fulfills Java's Security sandbox feature but hinders User's experience which is a much larger thing if you're on RIA track, get a compromise,</div>
<div style="text-align: justify;">
2. Allow lazy loading of application, let us choose our custom screen while application is loading , that spinning java logo is good but it looks monotonous after some time.</div>
<div style="text-align: justify;">
3. Include building a game viral tutorial in JavaFX, with distribution system <a href="http://wiki.zembly.com/wiki/Working_with_Java_Fx">as zembly</a>(another great technology, pardon me if I am not using proper term) and inclusion of <a href="http://www.projectdarkstar.com/">project darkstar</a> into the landscape.</div>
<div style="text-align: justify;">
4. Provide a remoting API, (get inspiration of <a href="http://www.exadel.com/web/portal/flamingo">project flamingo</a> and <a href="http://code.google.com/p/cairngorm-fx/">Cairngorm-fx</a>), I think Stephen Chin said&nbsp;<a href="http://steveonjava.com/2009/05/31/javafx-1-2-top-10/">here</a>&nbsp;(&nbsp;read the comments&nbsp;) that it is in the to-do list of <a href="http://code.google.com/p/jfxtras/">JFXtras</a> , so maybe we'll get it by year end.</div>
<div style="text-align: justify;">
5. Provide more open event like the nice thing Mr. Joshua Marinacci are doing in <a href="http://jfxstudio.org/">JFXstudio website</a>, it is great, you had JavaFX challenge but I think this release deserve a JavaFX challnge 2.0.</div>
</div>
