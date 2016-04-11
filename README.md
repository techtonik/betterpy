
#### A road to better Python

Companies like Google often develop own replacements
for standard libraries that are never merged in upstream.
They may even use [their own Git](http://commondatastorage.googleapis.com/chrome-infra-docs/flat/depot_tools/docs/html/depot_tools.html)

Merging upstream needs time and dedication, because
upstream volunteer work is not backed up economically.
Even reading through all the proposals, comments and
opinions takes a lot of time, resulting on DDoS of
volunteer service.

**Better Python** is the one that doesn't disrupt
**the flow** of intentions and information models that
are floating in your head. It is about mapping the
usability of the language with UX tools like CJM
(customer journey mapping) and evolving it bit by bit.


#### Library Evolution

Or why "good modules enter `stdlib` to die".

**Evolution** is process of endless births and deaths.
Standard library of Python is **engineered**, not
__evolved__. And it is really really hard to get
everything right - it takes an enormous amount of time
and brain space to read and write PEPs. And it takes
guts to finally accept them. It is better to be a part
of a **fitness** function than an architect of the
worlds.

Every time you need to use Python for something, it
shows its strong sides and weak sides, and these are
highly dependent on the situation. One library may be
good for one thing and completely fail on another.
For example:

    getopt --> optparse --> argparse
    
looks like an evolution, but some things in argparse
were done wrong for somebody and in his/her use it is

    getopt --> optparse
                 --> argparse

which means that both optparse and argparse are used
in parallel, because it is **easier and more logical**
to use it for this purpose. In fact, people are even
find uses for `getopt` module nowadays, so the **graph**
looks like this:

    getopt
      --> optparse
            --> argparse

Of course we don't have **usage statistics** for Python
library, because this "volunteer work is not backed up
economically". And we need to get even deeper - down to
separate **stories**.

There are plenty of
[other command line tools](https://github.com/vinta/awesome-python#command-line-tools)
around that better address specific problems, so mapping
stories to libraries using graphs (such as ones provided
by [ruruki](https://github.com/optiver/ruruki-eye)),
will make it possible to build **distributed fitness
function for Python library evolution**. Function that
uses humans and their current intentions to select the
**best fit**.


#### Bits and pieces

* https://github.com/techtonik/transpilery - gathering
  snippets for same purpose in different languages

