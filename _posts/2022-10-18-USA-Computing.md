---
keywords: fastai
description: test 
title: USA Computing Olympiad
toc: true
comments: truediv
categories: [USA Computing Olympiad]
nb_path: _notebooks/2022-10-18-USA-Computing.ipynb
layout: notebook
---

<!--
#################################################
### THIS FILE WAS AUTOGENERATED! DO NOT EDIT! ###
#################################################
# file to edit: _notebooks/2022-10-18-USA-Computing.ipynb
-->

<div class="container" id="notebook-container">
        
<div class="cell border-box-sizing text_cell rendered"><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h3 id="Problem-1.-Milk-Pails---Bronze">Problem 1. Milk Pails - Bronze<a class="anchor-link" href="#Problem-1.-Milk-Pails---Bronze"> </a></h3>
</div>
</div>
</div>
    {% raw %}
    
<div class="cell border-box-sizing code_cell rendered">
<div class="input">

<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">fin</span> <span class="o">=</span> <span class="nb">open</span><span class="p">(</span><span class="s1">&#39;pails.in&#39;</span><span class="p">,</span> <span class="s1">&#39;r&#39;</span><span class="p">)</span>

<span class="n">buck1</span><span class="p">,</span> <span class="n">buck2</span><span class="p">,</span> <span class="n">buck3</span> <span class="o">=</span> <span class="nb">map</span><span class="p">(</span><span class="nb">int</span><span class="p">,</span> <span class="n">fin</span><span class="o">.</span><span class="n">readline</span><span class="p">()</span><span class="o">.</span><span class="n">split</span><span class="p">())</span>

<span class="n">ans</span> <span class="o">=</span> <span class="mi">0</span>

<span class="c1"># x and y below take care of all </span>
<span class="c1"># possible combinations of the two buckets.</span>

<span class="k">for</span> <span class="n">x</span> <span class="ow">in</span> <span class="nb">range</span><span class="p">(</span><span class="mi">1001</span><span class="p">):</span>
	<span class="k">if</span> <span class="p">(</span><span class="n">buck1</span> <span class="o">*</span> <span class="n">x</span><span class="p">)</span> <span class="o">&gt;</span> <span class="n">buck3</span><span class="p">:</span>
		<span class="k">break</span>
	<span class="k">for</span> <span class="n">y</span> <span class="ow">in</span> <span class="nb">range</span><span class="p">(</span><span class="mi">1001</span><span class="p">):</span>
		<span class="n">current</span> <span class="o">=</span> <span class="p">(</span><span class="n">buck1</span> <span class="o">*</span> <span class="n">x</span><span class="p">)</span> <span class="o">+</span> <span class="p">(</span><span class="n">buck2</span> <span class="o">*</span> <span class="n">y</span><span class="p">)</span>
		<span class="k">if</span> <span class="n">current</span> <span class="o">&gt;</span> <span class="n">buck3</span><span class="p">:</span>
			<span class="k">break</span>
		<span class="n">ans</span> <span class="o">=</span> <span class="nb">max</span><span class="p">(</span><span class="n">ans</span><span class="p">,</span> <span class="n">current</span><span class="p">)</span>

<span class="k">with</span> <span class="nb">open</span><span class="p">(</span><span class="s1">&#39;pails.out&#39;</span><span class="p">,</span> <span class="s1">&#39;w&#39;</span><span class="p">)</span> <span class="k">as</span> <span class="n">fout</span><span class="p">:</span>
	<span class="n">fout</span><span class="o">.</span><span class="n">write</span><span class="p">(</span><span class="nb">str</span><span class="p">(</span><span class="n">ans</span><span class="p">)</span> <span class="o">+</span> <span class="s1">&#39;</span><span class="se">\n</span><span class="s1">&#39;</span><span class="p">)</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">

<div class="output_area">

<div class="output_subarea output_text output_error">
<pre>
<span class="ansi-red-fg">---------------------------------------------------------------------------</span>
<span class="ansi-red-fg">FileNotFoundError</span>                         Traceback (most recent call last)
<span class="ansi-green-intense-fg ansi-bold">/Users/sony/iwazaki-1/_notebooks/2022-10-18-USA-Computing.ipynb Cell 4</span> in <span class="ansi-cyan-fg">&lt;cell line: 1&gt;</span><span class="ansi-blue-fg">()</span>
<span class="ansi-green-fg">----&gt; &lt;a href=&#39;vscode-notebook-cell:/Users/sony/iwazaki-1/_notebooks/2022-10-18-USA-Computing.ipynb#X10sZmlsZQ%3D%3D?line=0&#39;&gt;1&lt;/a&gt;</span> fin = open(&#39;pails.in&#39;, &#39;r&#39;)
<span class="ansi-green-intense-fg ansi-bold">      &lt;a href=&#39;vscode-notebook-cell:/Users/sony/iwazaki-1/_notebooks/2022-10-18-USA-Computing.ipynb#X10sZmlsZQ%3D%3D?line=2&#39;&gt;3&lt;/a&gt;</span> buck1, buck2, buck3 = map(int, fin.readline().split())
<span class="ansi-green-intense-fg ansi-bold">      &lt;a href=&#39;vscode-notebook-cell:/Users/sony/iwazaki-1/_notebooks/2022-10-18-USA-Computing.ipynb#X10sZmlsZQ%3D%3D?line=4&#39;&gt;5&lt;/a&gt;</span> ans = 0

<span class="ansi-red-fg">FileNotFoundError</span>: [Errno 2] No such file or directory: &#39;pails.in&#39;</pre>
</div>
</div>

</div>
</div>

</div>
    {% endraw %}

<div class="cell border-box-sizing text_cell rendered"><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h3 id="Diamond-Collector">Diamond Collector<a class="anchor-link" href="#Diamond-Collector"> </a></h3>
</div>
</div>
</div>
</div>
 
