---
keywords: fastai
title: Title
nb_path: _notebooks/bash tutorial.ipynb
layout: notebook
---

<!--
#################################################
### THIS FILE WAS AUTOGENERATED! DO NOT EDIT! ###
#################################################
# file to edit: _notebooks/bash tutorial.ipynb
-->

<div class="container" id="notebook-container">
        
    {% raw %}
    
<div class="cell border-box-sizing code_cell rendered">
<div class="input">

<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-bash"><pre><span></span><span class="nb">echo</span> <span class="s2">&quot;Using conditional statement to create a project directory and project&quot;</span>

<span class="c1"># Variable section</span>
<span class="nb">export</span> <span class="nv">project_dir</span><span class="o">=</span><span class="nv">$HOME</span>/vscode  <span class="c1"># change vscode to different name to test git clone</span>
<span class="nb">export</span> <span class="nv">project</span><span class="o">=</span><span class="nv">$project_dir</span>/APCSP  <span class="c1"># change APCSP to name of project from git clone</span>
<span class="nb">export</span> <span class="nv">project_repo</span><span class="o">=</span><span class="s2">&quot;https://github.com/nighthawkcoders/APCSP.git&quot;</span>  <span class="c1"># change to project of choice</span>

<span class="nb">cd</span> ~    <span class="c1"># start in home directory</span>

<span class="c1"># Conditional block to make a project directory</span>
<span class="k">if</span> <span class="o">[</span> ! -d <span class="nv">$project_dir</span> <span class="o">]</span>
<span class="k">then</span> 
    <span class="nb">echo</span> <span class="s2">&quot;Directory </span><span class="nv">$project_dir</span><span class="s2"> does not exists... makinng directory </span><span class="nv">$project_dir</span><span class="s2">&quot;</span>
    mkdir -p <span class="nv">$project_dir</span>
<span class="k">fi</span>
<span class="nb">echo</span> <span class="s2">&quot;Directory </span><span class="nv">$project_dir</span><span class="s2"> exists.&quot;</span> 

<span class="c1"># Conditional block to git clone a project from project_repo</span>
<span class="k">if</span> <span class="o">[</span> ! -d <span class="nv">$project</span> <span class="o">]</span>
<span class="k">then</span>
    <span class="nb">echo</span> <span class="s2">&quot;Directory </span><span class="nv">$project</span><span class="s2"> does not exists... cloning </span><span class="nv">$project_repo</span><span class="s2">&quot;</span>
    <span class="nb">cd</span> <span class="nv">$project_dir</span>
    git clone <span class="nv">$project_repo</span>
    <span class="nb">cd</span> ~
<span class="k">fi</span>
<span class="nb">echo</span> <span class="s2">&quot;Directory </span><span class="nv">$project</span><span class="s2"> exists.&quot;</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">

<div class="output_area">

<div class="output_subarea output_stream output_stdout output_text">
<pre>Using conditional statement to create a project directory and project
Directory /home/wts/vscode exists.
Directory /home/wts/vscode/APCSP exists.
</pre>
</div>
</div>

</div>
</div>

</div>
    {% endraw %}

    {% raw %}
    
<div class="cell border-box-sizing code_cell rendered">
<div class="input">

<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-bash"><pre><span></span><span class="nb">echo</span> <span class="s2">&quot;Navigate to project, then navigate to area wwhere files were cloned&quot;</span>
<span class="nb">cd</span> <span class="nv">$project</span>
<span class="nb">pwd</span>

<span class="nb">echo</span> <span class="s2">&quot;&quot;</span>
<span class="nb">echo</span> <span class="s2">&quot;list top level or root of files with project pulled from github&quot;</span>
ls

<span class="nb">echo</span> <span class="s2">&quot;&quot;</span>
<span class="nb">echo</span> <span class="s2">&quot;list again with hidden files pulled from github&quot;</span>
ls -a   <span class="c1"># hidden files flag, many shell commands have flags</span>

<span class="nb">echo</span> <span class="s2">&quot;&quot;</span>
<span class="nb">echo</span> <span class="s2">&quot;list all files in long format&quot;</span>
ls -al   <span class="c1"># all files and long listing</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">

<div class="output_area">

<div class="output_subarea output_stream output_stdout output_text">
<pre>Navigate to project, then navigate to area wwhere files were cloned
/home/wts/vscode/APCSP

list top level or root of files with project pulled from github
<span class="ansi-blue-intense-fg ansi-bold">_action_files</span>       <span class="ansi-blue-intense-fg ansi-bold">_fastpages_docs</span>  index.html  <span class="ansi-blue-intense-fg ansi-bold">_notebooks</span>  <span class="ansi-blue-intense-fg ansi-bold">python</span>
<span class="ansi-blue-intense-fg ansi-bold">assets</span>              <span class="ansi-green-intense-fg ansi-bold">Gemfile</span>          <span class="ansi-blue-intense-fg ansi-bold">_layouts</span>    <span class="ansi-blue-intense-fg ansi-bold">_pages</span>      <span class="ansi-green-intense-fg ansi-bold">README.md</span>
_config.yml         <span class="ansi-blue-intense-fg ansi-bold">images</span>           LICENSE     <span class="ansi-blue-intense-fg ansi-bold">_plugins</span>    <span class="ansi-blue-intense-fg ansi-bold">_sass</span>
<span class="ansi-green-intense-fg ansi-bold">docker-compose.yml</span>  <span class="ansi-blue-intense-fg ansi-bold">_includes</span>        <span class="ansi-green-intense-fg ansi-bold">Makefile</span>    <span class="ansi-blue-intense-fg ansi-bold">_posts</span>      <span class="ansi-blue-intense-fg ansi-bold">_word</span>

list again with hidden files pulled from github
<span class="ansi-blue-intense-fg ansi-bold">.</span>                   <span class="ansi-green-intense-fg ansi-bold">docker-compose.yml</span>  .gitignore  <span class="ansi-green-intense-fg ansi-bold">Makefile</span>    <span class="ansi-green-intense-fg ansi-bold">README.md</span>
<span class="ansi-blue-intense-fg ansi-bold">..</span>                  <span class="ansi-blue-intense-fg ansi-bold">_fastpages_docs</span>     <span class="ansi-blue-intense-fg ansi-bold">images</span>      <span class="ansi-blue-intense-fg ansi-bold">_notebooks</span>  <span class="ansi-blue-intense-fg ansi-bold">_sass</span>
<span class="ansi-blue-intense-fg ansi-bold">_action_files</span>       <span class="ansi-green-intense-fg ansi-bold">Gemfile</span>             <span class="ansi-blue-intense-fg ansi-bold">_includes</span>   <span class="ansi-blue-intense-fg ansi-bold">_pages</span>      <span class="ansi-blue-intense-fg ansi-bold">.vscode</span>
<span class="ansi-blue-intense-fg ansi-bold">assets</span>              <span class="ansi-blue-intense-fg ansi-bold">.git</span>                index.html  <span class="ansi-blue-intense-fg ansi-bold">_plugins</span>    <span class="ansi-blue-intense-fg ansi-bold">_word</span>
_config.yml         .gitattributes      <span class="ansi-blue-intense-fg ansi-bold">_layouts</span>    <span class="ansi-blue-intense-fg ansi-bold">_posts</span>
.devcontainer.json  <span class="ansi-blue-intense-fg ansi-bold">.github</span>             LICENSE     <span class="ansi-blue-intense-fg ansi-bold">python</span>

list all files in long format
total 120
drwxrwxr-x 18 wts wts  4096 Aug 23 15:19 <span class="ansi-blue-intense-fg ansi-bold">.</span>
drwxrwxr-x  7 wts wts  4096 Aug 23 15:19 <span class="ansi-blue-intense-fg ansi-bold">..</span>
drwxrwxr-x  2 wts wts  4096 Aug 23 15:19 <span class="ansi-blue-intense-fg ansi-bold">_action_files</span>
drwxrwxr-x  4 wts wts  4096 Aug 23 15:19 <span class="ansi-blue-intense-fg ansi-bold">assets</span>
-rw-rw-r--  1 wts wts  3716 Aug 23 15:19 _config.yml
-rw-rw-r--  1 wts wts   420 Aug 23 15:19 .devcontainer.json
-rwxrwxr-x  1 wts wts  1136 Aug 23 15:19 <span class="ansi-green-intense-fg ansi-bold">docker-compose.yml</span>
drwxrwxr-x  2 wts wts  4096 Aug 23 15:19 <span class="ansi-blue-intense-fg ansi-bold">_fastpages_docs</span>
-rwxrwxr-x  1 wts wts  1304 Aug 23 15:19 <span class="ansi-green-intense-fg ansi-bold">Gemfile</span>
drwxrwxr-x  8 wts wts  4096 Aug 25 14:45 <span class="ansi-blue-intense-fg ansi-bold">.git</span>
-rw-rw-r--  1 wts wts    84 Aug 23 15:19 .gitattributes
drwxrwxr-x  4 wts wts  4096 Aug 23 15:19 <span class="ansi-blue-intense-fg ansi-bold">.github</span>
-rw-rw-r--  1 wts wts   917 Aug 23 15:19 .gitignore
drwxrwxr-x  5 wts wts  4096 Aug 23 15:19 <span class="ansi-blue-intense-fg ansi-bold">images</span>
drwxrwxr-x  2 wts wts  4096 Aug 23 15:19 <span class="ansi-blue-intense-fg ansi-bold">_includes</span>
-rw-rw-r--  1 wts wts  1061 Aug 23 15:19 index.html
drwxrwxr-x  2 wts wts  4096 Aug 23 15:19 <span class="ansi-blue-intense-fg ansi-bold">_layouts</span>
-rw-rw-r--  1 wts wts 11351 Aug 23 15:19 LICENSE
-rwxrwxr-x  1 wts wts  1422 Aug 23 15:19 <span class="ansi-green-intense-fg ansi-bold">Makefile</span>
drwxrwxr-x  4 wts wts  4096 Aug 28 18:45 <span class="ansi-blue-intense-fg ansi-bold">_notebooks</span>
drwxrwxr-x  2 wts wts  4096 Aug 23 15:19 <span class="ansi-blue-intense-fg ansi-bold">_pages</span>
drwxrwxr-x  2 wts wts  4096 Aug 23 15:19 <span class="ansi-blue-intense-fg ansi-bold">_plugins</span>
drwxrwxr-x  2 wts wts  4096 Aug 23 15:19 <span class="ansi-blue-intense-fg ansi-bold">_posts</span>
drwxrwxr-x  2 wts wts  4096 Aug 23 15:19 <span class="ansi-blue-intense-fg ansi-bold">python</span>
-rwxrwxr-x  1 wts wts  3614 Aug 23 15:19 <span class="ansi-green-intense-fg ansi-bold">README.md</span>
drwxrwxr-x  3 wts wts  4096 Aug 23 15:19 <span class="ansi-blue-intense-fg ansi-bold">_sass</span>
drwxrwxr-x  2 wts wts  4096 Aug 23 15:19 <span class="ansi-blue-intense-fg ansi-bold">.vscode</span>
drwxrwxr-x  2 wts wts  4096 Aug 23 15:19 <span class="ansi-blue-intense-fg ansi-bold">_word</span>
</pre>
</div>
</div>

</div>
</div>

</div>
    {% endraw %}

    {% raw %}
    
<div class="cell border-box-sizing code_cell rendered">
<div class="input">

<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-bash"><pre><span></span><span class="nb">echo</span> <span class="s2">&quot;Look for posts&quot;</span>
<span class="nb">export</span> <span class="nv">posts</span><span class="o">=</span><span class="nv">$project</span>/_posts  <span class="c1"># _posts inside project</span>
<span class="nb">cd</span> <span class="nv">$posts</span>  <span class="c1"># this should exist per fastpages</span>
<span class="nb">pwd</span>  <span class="c1"># present working directory</span>
ls -l  <span class="c1"># list posts</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">

<div class="output_area">

<div class="output_subarea output_stream output_stdout output_text">
<pre>Look for posts
/home/wts/vscode/APCSP/_posts
total 228
-rw-rw-r-- 1 wts wts 21306 Aug 23 15:19 2022-06-01-TT160-deploy.md
-rw-rw-r-- 1 wts wts  5861 Aug 23 15:19 2022-07-07-PBL-binary.md
-rw-rw-r-- 1 wts wts  3085 Aug 23 15:19 2022-07-08-PBL-grade_calc.md
-rw-rw-r-- 1 wts wts  3698 Aug 23 15:19 2022-07-08-PBL-graph.md
-rw-rw-r-- 1 wts wts  5729 Aug 23 15:19 2022-07-08-PBL-life.md
-rw-rw-r-- 1 wts wts 14387 Aug 23 15:19 2022-07-08-PBL-snake.md
-rw-rw-r-- 1 wts wts   334 Aug 23 15:19 2022-07-10-PBL-database.md
-rw-rw-r-- 1 wts wts  2908 Aug 23 15:19 2022-07-10-PBL-jokes.md
-rw-rw-r-- 1 wts wts  4046 Aug 23 15:19 2022-07-10-PBL-rapidapi.md
-rw-rw-r-- 1 wts wts  6685 Aug 23 15:19 2022-07-19-PBL-calculator.md
-rw-rw-r-- 1 wts wts 23325 Aug 23 15:19 2022-07-25-CSP-workshop.md
-rw-rw-r-- 1 wts wts  2333 Aug 23 15:19 2022-08-15-TP000-student_score_history.md
-rw-rw-r-- 1 wts wts  4363 Aug 23 15:19 2022-08-15-TP100-pseudo_code.md
-rw-rw-r-- 1 wts wts  7968 Aug 23 15:19 2022-08-15-TR100-tool_setup.md
-rw-rw-r-- 1 wts wts 15026 Aug 23 15:19 2022-08-15-TT100-tools.md
-rw-rw-r-- 1 wts wts  5590 Aug 23 15:19 2022-08-15-TT101-vscode-wsl.md
-rw-rw-r-- 1 wts wts  2155 Aug 23 15:19 2022-08-22-TR110-intro_python.md
-rw-rw-r-- 1 wts wts  5173 Aug 23 15:19 2022-08-22-TT110-fastpages.md
-rw-rw-r-- 1 wts wts  2798 Aug 23 15:19 2022-08-22-TT110-focus.md
-rw-rw-r-- 1 wts wts  2737 Aug 23 15:19 2022-08-29-TR120-data_abstract.md
-rw-rw-r-- 1 wts wts 10683 Aug 23 15:19 2022-08-29-TT120-agile.md
-rw-rw-r-- 1 wts wts  4498 Aug 23 15:19 2022-08-29-TT120-html_fragments.md
-rw-rw-r-- 1 wts wts  9037 Aug 23 15:19 2022-09-05-TP130-create_performance_task.md
-rw-rw-r-- 1 wts wts  7753 Aug 23 15:19 2022-09-05-TP131-create-task-bria.md
-rw-rw-r-- 1 wts wts  8066 Aug 23 15:19 2022-09-05-TR130-creative_development.md
-rw-rw-r-- 1 wts wts  3520 Aug 23 15:19 2022-09-05-TT130-applab.md
-rw-rw-r-- 1 wts wts   720 Aug 23 15:19 README.md
</pre>
</div>
</div>

</div>
</div>

</div>
    {% endraw %}

    {% raw %}
    
<div class="cell border-box-sizing code_cell rendered">
<div class="input">

<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-bash"><pre><span></span><span class="nb">echo</span> <span class="s2">&quot;Look for notebooks&quot;</span>
<span class="nb">export</span> <span class="nv">notebooks</span><span class="o">=</span><span class="nv">$project</span>/_notebooks  <span class="c1"># _notebooks is inside project</span>
<span class="nb">cd</span> <span class="nv">$notebooks</span>   <span class="c1"># this should exist per fastpages</span>
<span class="nb">pwd</span>  <span class="c1"># present working directory</span>
ls -l  <span class="c1"># list notebooks</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">

<div class="output_area">

<div class="output_subarea output_stream output_stdout output_text">
<pre>Look for notebooks
/home/wts/vscode/APCSP/_notebooks
total 144
-rw-rw-r-- 1 wts wts 14243 Aug 23 15:19 2022-06-01-TT150-webapi_tutorial.ipynb
-rw-rw-r-- 1 wts wts  8653 Aug 23 15:19 2022-07-21-PBL-neo4j_intro.ipynb
-rw-rw-r-- 1 wts wts 11694 Aug 23 15:19 2022-08-22-TP110-python_hello.ipynb
-rw-rw-r-- 1 wts wts 20003 Aug 23 15:19 2022-08-22-TT110-anthony_and_sahil.ipynb
-rw-rw-r-- 1 wts wts  9525 Aug 23 15:19 2022-08-22-TT110-bash_tutorial.ipynb
-rw-rw-r-- 1 wts wts 35721 Aug 25 14:44 2022-08-25-tool_check.ipynb
-rw-rw-r-- 1 wts wts 10141 Aug 23 15:19 2022-08-29-TP120-python_lists.ipynb
-rw-rw-r-- 1 wts wts 12632 Aug 23 15:19 2022-09-05-TT130-js_tutorial.ipynb
drwxrwxr-x 2 wts wts  4096 Aug 23 15:19 <span class="ansi-blue-intense-fg ansi-bold">images</span>
-rw-rw-r-- 1 wts wts   771 Aug 23 15:19 README.md
</pre>
</div>
</div>

</div>
</div>

</div>
    {% endraw %}

    {% raw %}
    
<div class="cell border-box-sizing code_cell rendered">
<div class="input">

<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-bash"><pre><span></span><span class="nb">echo</span> <span class="s2">&quot;Look for images in notebooks, print working directory, list files&quot;</span>
<span class="nb">cd</span> <span class="nv">$notebooks</span>/images  <span class="c1"># this should exist per fastpages</span>
<span class="nb">pwd</span>
ls -l
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">

<div class="output_area">

<div class="output_subarea output_stream output_stdout output_text">
<pre>Look for images in notebooks, print working directory, list files
/home/wts/vscode/APCSP/_notebooks/images
total 100
-rw-rw-r-- 1 wts wts 101617 Aug 23 15:19 <span class="ansi-magenta-intense-fg ansi-bold">kernels.png</span>
</pre>
</div>
</div>

</div>
</div>

</div>
    {% endraw %}

    {% raw %}
    
<div class="cell border-box-sizing code_cell rendered">
<div class="input">

<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-bash"><pre><span></span><span class="nb">echo</span> <span class="s2">&quot;Navigate to project, then navigate to area wwhere files were cloned&quot;</span>

<span class="nb">cd</span> <span class="nv">$project</span>
<span class="nb">echo</span> <span class="s2">&quot;show the contents of README.md&quot;</span>
<span class="nb">echo</span> <span class="s2">&quot;&quot;</span>

cat README.md  <span class="c1"># show contents of file, in this case markdown</span>
<span class="nb">echo</span> <span class="s2">&quot;&quot;</span>
<span class="nb">echo</span> <span class="s2">&quot;end of README.md&quot;</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">

<div class="output_area">

<div class="output_subarea output_stream output_stdout output_text">
<pre>Navigate to project, then navigate to area wwhere files were cloned
show the contents of README.md

[//]: # (This template replaces README.md when someone creates a new repo with the fastpages template.)

![](https://github.com/nighthawkcoders/APCSP/workflows/CI/badge.svg) 
![](https://github.com/nighthawkcoders/APCSP/workflows/GH-Pages%20Status/badge.svg) 
[![](https://img.shields.io/static/v1?label=fastai&amp;message=fastpages&amp;color=57aeac&amp;labelColor=black&amp;style=flat&amp;logo=data:image/png;base64,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)](https://github.com/fastai/fastpages)

https://nighthawkcoders.github.io/APCSP/

# My Blog


_powered by [fastpages](https://github.com/fastai/fastpages)_


## What To Do Next?

Great!  You have setup your repo.  Now its time to start writing content.  Some helpful links:

- [Writing Blogs With Jupyter](https://github.com/fastai/fastpages#writing-blog-posts-with-jupyter)

- [Writing Blogs With Markdown](https://github.com/fastai/fastpages#writing-blog-posts-with-markdown)

- [Writing Blog Posts With Word](https://github.com/fastai/fastpages#writing-blog-posts-with-microsoft-word)

- [(Optional) Preview Your Blog Locally](_fastpages_docs/DEVELOPMENT.md)

Note: you may want to remove example blog posts from the `_posts`,  `_notebooks` or `_word` folders (but leave them empty, don&#39;t delete these folders) if you don&#39;t want these blog posts to appear on your site.

Please use the [nbdev &amp; blogging channel](https://forums.fast.ai/c/fastai-users/nbdev/48) in the fastai forums for any questions or feature requests.

end of README.md
</pre>
</div>
</div>

</div>
</div>

</div>
    {% endraw %}

    {% raw %}
    
<div class="cell border-box-sizing code_cell rendered">
<div class="input">

<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-bash"><pre><span></span><span class="nb">echo</span> <span class="s2">&quot;Show the shell environment variables, key on left of equal value on right&quot;</span>
<span class="nb">echo</span> <span class="s2">&quot;&quot;</span>

env
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">

<div class="output_area">

<div class="output_subarea output_stream output_stdout output_text">
<pre>Show the shell environment variables, key on left of equal value on right

SHELL=/bin/bash
SESSION_MANAGER=local/wts-HP-Pavilion-x360-Convertible-11m-ad0xx:@/tmp/.ICE-unix/1856,unix/wts-HP-Pavilion-x360-Convertible-11m-ad0xx:/tmp/.ICE-unix/1856
QT_ACCESSIBILITY=1
SNAP_REVISION=105
COLORTERM=truecolor
XDG_CONFIG_DIRS=/etc/xdg/xdg-ubuntu:/etc/xdg
PYTHONUNBUFFERED=1
XDG_MENU_PREFIX=gnome-
project=/home/wts/vscode/APCSP
GNOME_DESKTOP_SESSION_ID=this-is-deprecated
CONDA_EXE=/home/wts/anaconda3/bin/conda
_CE_M=
APPLICATION_INSIGHTS_NO_DIAGNOSTIC_CHANNEL=true
SNAP_REAL_HOME=/home/wts
SNAP_USER_COMMON=/home/wts/snap/code/common
GNOME_SHELL_SESSION_MODE=ubuntu
SSH_AUTH_SOCK=/run/user/1000/keyring/ssh
SNAP_INSTANCE_KEY=
ELECTRON_RUN_AS_NODE=1
XMODIFIERS=@im=ibus
DESKTOP_SESSION=ubuntu
SSH_AGENT_PID=1818
GDK_PIXBUF_MODULE_FILE=/home/wts/snap/code/common/.cache/gdk-pixbuf-loaders.cache
VSCODE_AMD_ENTRYPOINT=vs/workbench/api/node/extensionHostProcess
GTK_MODULES=gail:atk-bridge
PWD=/home/wts/vscode/APCSP
GSETTINGS_SCHEMA_DIR=/snap/code/105/usr/share/glib-2.0/schemas
XDG_SESSION_DESKTOP=ubuntu
LOGNAME=wts
CONDA_ROOT=/home/wts/anaconda3
XDG_SESSION_TYPE=x11
CONDA_PREFIX=/home/wts/anaconda3
GPG_AGENT_INFO=/run/user/1000/gnupg/S.gpg-agent:0:1
VSCODE_CODE_CACHE_PATH=/home/wts/.config/Code/CachedData/e4503b30fc78200f846c62cf8091b76ff5547662
XAUTHORITY=/run/user/1000/gdm/Xauthority
SNAP_CONTEXT=rFv0xLIe4JVRVHAhzG5nDRZm7M8YpuWmHcEdiWsiqWTVMpoQMybN
GJS_DEBUG_TOPICS=JS ERROR;JS LOG
WINDOWPATH=2
project_dir=/home/wts/vscode
HOME=/home/wts
USERNAME=wts
IM_CONFIG_PHASE=1
LANG=en_US.UTF-8
LS_COLORS=rs=0:di=01;34:ln=01;36:mh=00:pi=40;33:so=01;35:do=01;35:bd=40;33;01:cd=40;33;01:or=40;31;01:mi=00:su=37;41:sg=30;43:ca=30;41:tw=30;42:ow=34;42:st=37;44:ex=01;32:*.tar=01;31:*.tgz=01;31:*.arc=01;31:*.arj=01;31:*.taz=01;31:*.lha=01;31:*.lz4=01;31:*.lzh=01;31:*.lzma=01;31:*.tlz=01;31:*.txz=01;31:*.tzo=01;31:*.t7z=01;31:*.zip=01;31:*.z=01;31:*.dz=01;31:*.gz=01;31:*.lrz=01;31:*.lz=01;31:*.lzo=01;31:*.xz=01;31:*.zst=01;31:*.tzst=01;31:*.bz2=01;31:*.bz=01;31:*.tbz=01;31:*.tbz2=01;31:*.tz=01;31:*.deb=01;31:*.rpm=01;31:*.jar=01;31:*.war=01;31:*.ear=01;31:*.sar=01;31:*.rar=01;31:*.alz=01;31:*.ace=01;31:*.zoo=01;31:*.cpio=01;31:*.7z=01;31:*.rz=01;31:*.cab=01;31:*.wim=01;31:*.swm=01;31:*.dwm=01;31:*.esd=01;31:*.jpg=01;35:*.jpeg=01;35:*.mjpg=01;35:*.mjpeg=01;35:*.gif=01;35:*.bmp=01;35:*.pbm=01;35:*.pgm=01;35:*.ppm=01;35:*.tga=01;35:*.xbm=01;35:*.xpm=01;35:*.tif=01;35:*.tiff=01;35:*.png=01;35:*.svg=01;35:*.svgz=01;35:*.mng=01;35:*.pcx=01;35:*.mov=01;35:*.mpg=01;35:*.mpeg=01;35:*.m2v=01;35:*.mkv=01;35:*.webm=01;35:*.ogm=01;35:*.mp4=01;35:*.m4v=01;35:*.mp4v=01;35:*.vob=01;35:*.qt=01;35:*.nuv=01;35:*.wmv=01;35:*.asf=01;35:*.rm=01;35:*.rmvb=01;35:*.flc=01;35:*.avi=01;35:*.fli=01;35:*.flv=01;35:*.gl=01;35:*.dl=01;35:*.xcf=01;35:*.xwd=01;35:*.yuv=01;35:*.cgm=01;35:*.emf=01;35:*.ogv=01;35:*.ogx=01;35:*.aac=00;36:*.au=00;36:*.flac=00;36:*.m4a=00;36:*.mid=00;36:*.midi=00;36:*.mka=00;36:*.mp3=00;36:*.mpc=00;36:*.ogg=00;36:*.ra=00;36:*.wav=00;36:*.oga=00;36:*.opus=00;36:*.spx=00;36:*.xspf=00;36:
XDG_CURRENT_DESKTOP=Unity
VSCODE_IPC_HOOK=/run/user/1000/vscode-5f62299e-1.70.2-main.sock
VTE_VERSION=6003
SNAP_ARCH=amd64
SNAP_INSTANCE_NAME=code
SNAP_USER_DATA=/home/wts/snap/code/105
CONDA_PROMPT_MODIFIER=(base) 
VSCODE_CLI=1
DISABLE_WAYLAND=1
PYDEVD_USE_FRAME_EVAL=NO
GNOME_TERMINAL_SCREEN=/org/gnome/Terminal/screen/e013f978_ca54_45dd_8e86_6662d4286690
INVOCATION_ID=a48ee9faaed945789c0e6cb07aa6687a
MANAGERPID=1640
SNAP_REEXEC=
CHROME_DESKTOP=code-url-handler.desktop
posts=/home/wts/vscode/APCSP/_posts
GJS_DEBUG_OUTPUT=stderr
JPY_PARENT_PID=7326
LESSCLOSE=/usr/bin/lesspipe %s %s
XDG_SESSION_CLASS=user
PYTHONPATH=/home/wts/.vscode/extensions/ms-toolsai.jupyter-2022.7.1102252217/pythonFiles:/home/wts/.vscode/extensions/ms-toolsai.jupyter-2022.7.1102252217/pythonFiles/lib/python
TERM=xterm-256color
_CE_CONDA=
LESSOPEN=| /usr/bin/lesspipe %s
USER=wts
PYTHONIOENCODING=utf-8
notebooks=/home/wts/vscode/APCSP/_notebooks
SNAP=/snap/code/105
GNOME_TERMINAL_SERVICE=:1.90
CONDA_SHLVL=1
SNAP_COMMON=/var/snap/code/common
SNAP_VERSION=e4503b30
DISPLAY=:0
VSCODE_PID=6993
SHLVL=3
GDK_PIXBUF_MODULEDIR=/snap/code/105/usr/lib/x86_64-linux-gnu/gdk-pixbuf-2.0/2.10.0/loaders
SNAP_LIBRARY_PATH=/var/lib/snapd/lib/gl:/var/lib/snapd/lib/gl32:/var/lib/snapd/void
PAGER=cat
SNAP_COOKIE=rFv0xLIe4JVRVHAhzG5nDRZm7M8YpuWmHcEdiWsiqWTVMpoQMybN
JUPYTER_PATH=/home/wts/.vscode/extensions/ms-toolsai.jupyter-2022.7.1102252217/temp/jupyter
QT_IM_MODULE=ibus
project_repo=https://github.com/nighthawkcoders/APCSP.git
VSCODE_CWD=/home/wts/vscode
SNAP_DATA=/var/snap/code/105
CONDA_PYTHON_EXE=/home/wts/anaconda3/bin/python
XDG_RUNTIME_DIR=/run/user/1000
PS1=[PEXP\[\]ECT_PROMPT&gt;
CONDA_DEFAULT_ENV=base
SNAP_NAME=code
ELECTRON_NO_ATTACH_CONSOLE=1
JOURNAL_STREAM=8:50375
XDG_DATA_DIRS=/usr/share/ubuntu:/usr/local/share/:/usr/share/:/var/lib/snapd/desktop
GDK_BACKEND=x11
PATH=/home/wts/anaconda3/bin:/home/wts/anaconda3/condabin:/home/wts/.local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/games:/usr/local/games:/snap/bin
GDMSESSION=ubuntu
ORIGINAL_XDG_CURRENT_DESKTOP=ubuntu:GNOME
DBUS_SESSION_BUS_ADDRESS=unix:path=/run/user/1000/bus
VSCODE_NLS_CONFIG={&#34;locale&#34;:&#34;en-us&#34;,&#34;availableLanguages&#34;:{},&#34;_languagePackSupport&#34;:true}
VSCODE_HANDLES_UNCAUGHT_ERRORS=true
OLDPWD=/home/wts/vscode/APCSP/_notebooks/images
_=/usr/bin/env
</pre>
</div>
</div>

</div>
</div>

</div>
    {% endraw %}

    {% raw %}
    
<div class="cell border-box-sizing code_cell rendered">
<div class="input">

<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-bash"><pre><span></span><span class="nb">cd</span> <span class="nv">$project</span>

<span class="nb">echo</span> <span class="s2">&quot;&quot;</span>
<span class="nb">echo</span> <span class="s2">&quot;show the secrets of .git&quot;</span>
<span class="nb">cd</span> .git
ls -l

<span class="nb">echo</span> <span class="s2">&quot;&quot;</span>
<span class="nb">echo</span> <span class="s2">&quot;look at config file&quot;</span>
cat config
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">

<div class="output_area">

<div class="output_subarea output_stream output_stdout output_text">
<pre>
show the secrets of .git
total 68
drwxrwxr-x  2 wts wts  4096 Aug 23 15:19 <span class="ansi-blue-intense-fg ansi-bold">branches</span>
-rw-rw-r--  1 wts wts   265 Aug 23 15:19 config
-rw-rw-r--  1 wts wts    73 Aug 23 15:19 description
-rw-rw-r--  1 wts wts   102 Aug 25 14:45 FETCH_HEAD
-rw-rw-r--  1 wts wts    23 Aug 23 15:19 HEAD
drwxrwxr-x  2 wts wts  4096 Aug 23 15:19 <span class="ansi-blue-intense-fg ansi-bold">hooks</span>
-rw-rw-r--  1 wts wts 20021 Aug 25 14:44 index
drwxrwxr-x  2 wts wts  4096 Aug 23 15:19 <span class="ansi-blue-intense-fg ansi-bold">info</span>
drwxrwxr-x  3 wts wts  4096 Aug 23 15:19 <span class="ansi-blue-intense-fg ansi-bold">logs</span>
drwxrwxr-x 12 wts wts  4096 Aug 25 14:44 <span class="ansi-blue-intense-fg ansi-bold">objects</span>
-rw-rw-r--  1 wts wts    41 Aug 25 14:45 ORIG_HEAD
-rw-rw-r--  1 wts wts   271 Aug 23 15:19 packed-refs
drwxrwxr-x  5 wts wts  4096 Aug 23 15:19 <span class="ansi-blue-intense-fg ansi-bold">refs</span>

look at config file
[core]
	repositoryformatversion = 0
	filemode = true
	bare = false
	logallrefupdates = true
[remote &#34;origin&#34;]
	url = https://github.com/nighthawkcoders/APCSP
	fetch = +refs/heads/*:refs/remotes/origin/*
[branch &#34;master&#34;]
	remote = origin
	merge = refs/heads/master
</pre>
</div>
</div>

</div>
</div>

</div>
    {% endraw %}

<div class="cell border-box-sizing text_cell rendered"><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<hr>
<p>toc: true</p>
<h2 id="categories:-[markdown]">categories: [markdown]<a class="anchor-link" href="#categories:-[markdown]"> </a></h2>
</div>
</div>
</div>
<div class="cell border-box-sizing text_cell rendered"><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<p>BASH TUTORIAL THINGS</p>

</div>
</div>
</div>
</div>
 
