---
permalink: /
title: "Benbriel's Personal Website"
excerpt: "About me"
author_profile: true
redirect_from: 
  - /about/
  - /about.html
---

Test title.
======
This is my website. It's a [test](https://es.wikipedia.org/wiki/Test). One can even write in $\LaTeX$! For example,

\\[\begin{equation} \label{test} a^2 = b^2 + c^2 \end{equation}\\]

Equations can even be referenced, like \eqref{test}.

\\[\begin{equation} \label{test2} \frac{\mathrm{d}}{\mathrm{d} x} \int_{a}^{x} f(s)ds = f(x) + C \end{equation}\\]

For example, one can write the Lagrangian of a point particle moving in one dimension space under a certain potential as $\mathcal{L}=T-V$, meaning

\\[\mathcal{L}=\frac{m}{2} \dot{q}^2 - V(q) \\]

where $m$ is the mass of the particle, $q$ is its position, and $\dot{q}$ is its velocity. In Hamiltonian mechanics, the momentum $p$ is defined as $p=\partial_q \mathcal{L}=m \dot{q}$. The Hamiltonian is defined as $H=p \dot{q} - \mathcal{L}$, so replacing $\dot{q}$, it yields

\\[H = \frac{p^2}{2 m} + V(q) \\]

Now, one could use the Hamilton equations of motion to solve for the position and momentum, however, we're taking the long way. Due to the simmetries of the Hamiltonian, $H'=H + \partial_t S$ gives the same equations of motion, where $S=S(q,p,t)$ is any function of the position, momentum and time. The idea is to look for an action $S$ such that the new Hamiltonian is zero, thus forming the Hamilton-Jacobi equations. This is a very general problem, so in this case it turns tedious and much longer than using the Euler-Lagrange equations. If one defines $\partial_q S=p$, then one gets a differential equation for the action $S$, of the form

\\[\frac{\left( \partial_q S \right)^2}{2 m} + V(q) + \partial_t S = 0 \\]

This equation is generally hard to solve. However, identifying cyclic coordinates, or the direct coordinate independence of $H$. In this case, $\partial_t H=0$. This lets one choose an action $S=W(q) - E t$, where in this case $E$ corresponds to the total energy of the particle. Replacing this new $S$,

\\[\frac{W'^2}{2 m} + V(q) = E \Rightarrow W(q) = \int \sqrt{2 m (E - V(q))} dq \\]

Then, having solved for $S$, the chosen canonical transformations say $\partial_E S = \beta$, where $\beta$ is another constant. This implies

\\[\beta = -t + \int \frac{dq}{\sqrt{\frac{2}{m} \left( E - V(q) \right)}} \\]

Replacing $V(q)$ for a specific potential does not assure that one can write $q$ as $q(t)$ but t(q), however, for most simple cases, the integral can be solved, and the solution $q(t)$ is found.

For example, a harmonic oscillator has a potential that can be written as $V(q)=\frac{k}{2}q^2$, where $k$ is a constant. Replacing on the above equation and solving the integral, one gets

\\[\sqrt{k m}(t+\beta) = m \arcsin{\left( \sqrt{\frac{k}{2 E}} q \right)} \\]

Finally, one can simplify for $q(t)$ to get

\\[q(t) = \sqrt{\frac{2 E}{k}} \sin{\left( \sqrt{\frac{k}{m}}(t + \beta) \right)} \\]

Where $E$ can be interpreted as the initial energy of the system, and $\beta$ as the initial phase. This returns a sine wave, as expected.


A data-driven personal website
======
Like many other Jekyll-based GitHub Pages templates, academicpages makes you separate the website's content from its form. The content & metadata of your website are in structured markdown files, while various other files constitute the theme, specifying how to transform that content & metadata into HTML pages. You keep these various markdown (.md), YAML (.yml), HTML, and CSS files in a public GitHub repository. Each time you commit and push an update to the repository, the [GitHub pages](https://pages.github.com/) service creates static HTML pages based on these files, which are hosted on GitHub's servers free of charge.

Many of the features of dynamic content management systems (like Wordpress) can be achieved in this fashion, using a fraction of the computational resources and with far less vulnerability to hacking and DDoSing. You can also modify the theme to your heart's content without touching the content of your site. If you get to a point where you've broken something in Jekyll/HTML/CSS beyond repair, your markdown files describing your talks, publications, etc. are safe. You can rollback the changes or even delete the repository and start over -- just be sure to save the markdown files! Finally, you can also write scripts that process the structured data on the site, such as [this one](https://github.com/academicpages/academicpages.github.io/blob/master/talkmap.ipynb) that analyzes metadata in pages about talks to display [a map of every location you've given a talk](https://academicpages.github.io/talkmap.html).

Getting started
======
1. Register a GitHub account if you don't have one and confirm your e-mail (required!)
1. Fork [this repository](https://github.com/academicpages/academicpages.github.io) by clicking the "fork" button in the top right. 
1. Go to the repository's settings (rightmost item in the tabs that start with "Code", should be below "Unwatch"). Rename the repository "[your GitHub username].github.io", which will also be your website's URL.
1. Set site-wide configuration and create content & metadata (see below -- also see [this set of diffs](http://archive.is/3TPas) showing what files were changed to set up [an example site](https://getorg-testacct.github.io) for a user with the username "getorg-testacct")
1. Upload any files (like PDFs, .zip files, etc.) to the files/ directory. They will appear at https://[your GitHub username].github.io/files/example.pdf.  
1. Check status by going to the repository settings, in the "GitHub pages" section

Site-wide configuration
------
The main configuration file for the site is in the base directory in [_config.yml](https://github.com/academicpages/academicpages.github.io/blob/master/_config.yml), which defines the content in the sidebars and other site-wide features. You will need to replace the default variables with ones about yourself and your site's github repository. The configuration file for the top menu is in [_data/navigation.yml](https://github.com/academicpages/academicpages.github.io/blob/master/_data/navigation.yml). For example, if you don't have a portfolio or blog posts, you can remove those items from that navigation.yml file to remove them from the header. 

Create content & metadata
------
For site content, there is one markdown file for each type of content, which are stored in directories like _publications, _talks, _posts, _teaching, or _pages. For example, each talk is a markdown file in the [_talks directory](https://github.com/academicpages/academicpages.github.io/tree/master/_talks). At the top of each markdown file is structured data in YAML about the talk, which the theme will parse to do lots of cool stuff. The same structured data about a talk is used to generate the list of talks on the [Talks page](https://academicpages.github.io/talks), each [individual page](https://academicpages.github.io/talks/2012-03-01-talk-1) for specific talks, the talks section for the [CV page](https://academicpages.github.io/cv), and the [map of places you've given a talk](https://academicpages.github.io/talkmap.html) (if you run this [python file](https://github.com/academicpages/academicpages.github.io/blob/master/talkmap.py) or [Jupyter notebook](https://github.com/academicpages/academicpages.github.io/blob/master/talkmap.ipynb), which creates the HTML for the map based on the contents of the _talks directory).

**Markdown generator**

I have also created [a set of Jupyter notebooks](https://github.com/academicpages/academicpages.github.io/tree/master/markdown_generator
) that converts a CSV containing structured data about talks or presentations into individual markdown files that will be properly formatted for the academicpages template. The sample CSVs in that directory are the ones I used to create my own personal website at stuartgeiger.com. My usual workflow is that I keep a spreadsheet of my publications and talks, then run the code in these notebooks to generate the markdown files, then commit and push them to the GitHub repository.

How to edit your site's GitHub repository
------
Many people use a git client to create files on their local computer and then push them to GitHub's servers. If you are not familiar with git, you can directly edit these configuration and markdown files directly in the github.com interface. Navigate to a file (like [this one](https://github.com/academicpages/academicpages.github.io/blob/master/_talks/2012-03-01-talk-1.md) and click the pencil icon in the top right of the content preview (to the right of the "Raw | Blame | History" buttons). You can delete a file by clicking the trashcan icon to the right of the pencil icon. You can also create new files or upload files by navigating to a directory and clicking the "Create new file" or "Upload files" buttons. 

Example: editing a markdown file for a talk
![Editing a markdown file for a talk](/images/editing-talk.png)

For more info
------
More info about configuring academicpages can be found in [the guide](https://academicpages.github.io/markdown/). The [guides for the Minimal Mistakes theme](https://mmistakes.github.io/minimal-mistakes/docs/configuration/) (which this theme was forked from) might also be helpful.
