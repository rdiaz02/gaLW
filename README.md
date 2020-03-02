<h2>Genetic algorithms, evolutionarily stable strategies, and the loser/winner
effects</h2>

<p>(A long time ago, around the year 2000) I spent some time working on the
loser/winner effects. This is a problem that requires game theory (what is
a good strategy depends on what your opponents do) but I could not find
simple analytical solutions. So I used genetic algorithms, which seems
natural enough here since we are dealing with the evolution of behavioral
strategies.</p>

<p>There are several libraries for genetic algorithms. I started using <a
href="http://lancet.mit.edu/ga/">galib</a>, a very nice library. However, I
found it hard to use of it for my problem, where fitness is the result of
repeated interactions between the genotypes (and not something you evaluate in
a sweep over the population at each generation); this is doable with galib, but I found it hard
and awkward. Thus, to learn more C++ and to have more control,
I wrote a set classes and methods for
genetic algorithms (ga.cpp, ga.h). And the code for the loser/winner part
(fighting.cpp), plus a few helper functions, etc.</p>

<p>Please note that the documentation is non-existent (you'll need to read the
comments), that there are a few comments in Spanish and spanglish, and that
indentation and line width are "peculiar" (set to fit my monitor and usage of XEmacs).
Its been a while since I worked on these issues. But I'd appreciate that, if
you use this code, you let me know. </p>

<p>To run it you will need to install <a
href="http://www.oonumerics.org/blitz/">Blitz++</a> and
<b>libRmath</b>, the stand-alone math library from <a
href="http://www.r-project.org">R</a>. If you use <a
href="http://www.debian.org">Debian GNU/Linux</a>, this is (was) as easy as:</p>
<pre>
apt-get install blitz
apt-get install r-mathlib
</pre>

<p>I've also run it with other GNU/Linux distributions.</p>

<p><a href="gaLW.tar.gz">Download</a> the code. This software is
released     under the <a href="http://www.gnu.org/licenses/licenses.html#GPL">GNU
    GPL</a>.</p>

