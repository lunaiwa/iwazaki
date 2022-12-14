---
keywords: fastai
description: Documenting all errors encountered during SCRUM projects
title: Error Documentation
toc: true
comments: true
categories: [errors]
nb_path: _notebooks/2022-10-03-Error-Documentation.ipynb
layout: notebook
---

<!--
#################################################
### THIS FILE WAS AUTOGENERATED! DO NOT EDIT! ###
#################################################
# file to edit: _notebooks/2022-10-03-Error-Documentation.ipynb
-->

<div class="container" id="notebook-container">
        
<div class="cell border-box-sizing text_cell rendered"><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h3 id="Questions-in-Errors">Questions in Errors<a class="anchor-link" href="#Questions-in-Errors"> </a></h3>
</div>
</div>
</div>
<div class="cell border-box-sizing text_cell rendered"><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<p>What errors may arise in your project?</p>
<blockquote><p>Errors that may arise are the frontend not showing what it might need or the backend not performing as it should!</p>
</blockquote>

</div>
</div>
</div>
<div class="cell border-box-sizing text_cell rendered"><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<p>Make sure to document any bugs you encounter and how you solved the problem.</p>
<blockquote><p>Most bugs might be a changed letter or number error in the code, another error that might be encountered is missing lines of code!</p>
</blockquote>

</div>
</div>
</div>
<div class="cell border-box-sizing text_cell rendered"><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<p>What are “single” tests that you will perform on your project? Or, your part of the project?</p>
<blockquote><p>Single tests that might be performed on the project is the frontend testing and seeing if the user see what is needed and not the code.</p>
</blockquote>

</div>
</div>
</div>
<div class="cell border-box-sizing text_cell rendered"><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h3 id="Errors-Documentation">Errors Documentation<a class="anchor-link" href="#Errors-Documentation"> </a></h3>
</div>
</div>
</div>
<div class="cell border-box-sizing text_cell rendered"><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<p>1.ERROR
2.ERROR
3.404</p>

</div>
</div>
</div>
<div class="cell border-box-sizing text_cell rendered"><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h3 id="Error-Challenge">Error Challenge<a class="anchor-link" href="#Error-Challenge"> </a></h3>
</div>
</div>
</div>
<div class="cell border-box-sizing text_cell rendered"><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<p>What are some ways to (user) error proof this code?</p>
<blockquote><p>First add in a single test for the expectation, then test input and output, run the test!!!</p>
</blockquote>

</div>
</div>
</div>
<div class="cell border-box-sizing text_cell rendered"><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<p>The code should be able to calculate the cost of the meal of the user</p>

</div>
</div>
</div>
    {% raw %}
    
<div class="cell border-box-sizing code_cell rendered">
<div class="input">

<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">menu</span> <span class="o">=</span>  <span class="p">{</span><span class="s2">&quot;burger&quot;</span><span class="p">:</span> <span class="mf">3.99</span><span class="p">,</span>
         <span class="s2">&quot;fries&quot;</span><span class="p">:</span> <span class="mf">1.99</span><span class="p">,</span>
         <span class="s2">&quot;drink&quot;</span><span class="p">:</span> <span class="mf">0.99</span><span class="p">}</span>
<span class="n">total</span> <span class="o">=</span> <span class="mi">0</span>

<span class="c1">#shows the user the menu and prompts them to select an item</span>
<span class="nb">print</span><span class="p">(</span><span class="s2">&quot;Menu&quot;</span><span class="p">)</span>
<span class="k">for</span> <span class="n">k</span><span class="p">,</span><span class="n">v</span> <span class="ow">in</span> <span class="n">menu</span><span class="o">.</span><span class="n">items</span><span class="p">():</span>
    <span class="nb">print</span><span class="p">(</span><span class="n">k</span> <span class="o">+</span> <span class="s2">&quot;  $&quot;</span> <span class="o">+</span> <span class="nb">str</span><span class="p">(</span><span class="n">v</span><span class="p">))</span> <span class="c1">#why does v have &quot;str&quot; in front of it?</span>

<span class="c1">#ideally the code should prompt the user multiple times</span>
<span class="n">item</span> <span class="o">=</span> <span class="nb">input</span><span class="p">(</span><span class="s2">&quot;Please select an item from the menu&quot;</span><span class="p">)</span>
<span class="k">if</span> <span class="n">item</span> <span class="o">==</span> <span class="s2">&quot;fries&quot;</span><span class="p">:</span>
    <span class="n">total</span> <span class="o">=</span> <span class="mf">1.99</span>
<span class="k">if</span> <span class="n">item</span> <span class="o">==</span> <span class="s2">&quot;burger&quot;</span><span class="p">:</span>
    <span class="n">total</span> <span class="o">=</span> <span class="mf">3.99</span>
<span class="k">if</span> <span class="n">item</span> <span class="o">==</span> <span class="s2">&quot;drink&quot;</span><span class="p">:</span>
    <span class="n">total</span> <span class="o">=</span> <span class="o">.</span><span class="mi">99</span>



<span class="c1">#code should add the price of the menu items selected by the user </span>
<span class="nb">print</span><span class="p">(</span><span class="n">total</span><span class="p">)</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">

<div class="output_area">

<div class="output_subarea output_stream output_stdout output_text">
<pre>Menu
burger  $3.99
fries  $1.99
drink  $0.99
3.99
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
<div class=" highlight hl-ipython3"><pre><span></span><span class="c1"># prices of the different meals</span>
<span class="n">menu</span> <span class="o">=</span>  <span class="p">{</span><span class="s2">&quot;burger&quot;</span><span class="p">:</span> <span class="mf">3.99</span><span class="p">,</span>
         <span class="s2">&quot;fries&quot;</span><span class="p">:</span> <span class="mf">1.99</span><span class="p">,</span>
         <span class="s2">&quot;drink&quot;</span><span class="p">:</span> <span class="mf">0.99</span><span class="p">}</span>
<span class="n">total</span> <span class="o">=</span> <span class="mf">0.0</span>
<span class="n">current_order</span> <span class="o">=</span> <span class="p">[]</span>
<span class="c1"># order of the user</span>

<span class="c1"># this is where the user prints the order</span>
<span class="nb">print</span><span class="p">(</span><span class="s2">&quot;Menu:&quot;</span><span class="p">)</span>
<span class="k">for</span> <span class="n">k</span><span class="p">,</span><span class="n">v</span> <span class="ow">in</span> <span class="n">menu</span><span class="o">.</span><span class="n">items</span><span class="p">():</span>
    <span class="nb">print</span><span class="p">(</span><span class="n">k</span> <span class="o">+</span> <span class="s2">&quot;  $&quot;</span> <span class="o">+</span> <span class="nb">str</span><span class="p">(</span><span class="n">v</span><span class="p">))</span> 
<span class="n">item</span> <span class="o">=</span> <span class="nb">input</span><span class="p">(</span><span class="s2">&quot;Select an Item&quot;</span><span class="p">)</span>
<span class="n">item</span> <span class="o">=</span> <span class="n">item</span><span class="o">.</span><span class="n">lower</span><span class="p">()</span>
<span class="k">while</span> <span class="n">item</span> <span class="ow">in</span> <span class="n">menu</span><span class="o">.</span><span class="n">keys</span><span class="p">():</span>
    <span class="n">quantity</span> <span class="o">=</span> <span class="nb">float</span><span class="p">(</span><span class="nb">input</span><span class="p">(</span><span class="s2">&quot;How Many&quot;</span><span class="p">))</span>

    <span class="n">current_order</span><span class="o">.</span><span class="n">append</span><span class="p">(</span><span class="nb">str</span><span class="p">(</span><span class="n">item</span><span class="p">)</span> <span class="o">+</span> <span class="s2">&quot; X &quot;</span> <span class="o">+</span> <span class="nb">str</span><span class="p">(</span><span class="n">quantity</span><span class="p">))</span>
    <span class="n">total</span> <span class="o">+=</span> <span class="p">(</span><span class="n">menu</span><span class="p">[</span><span class="n">item</span><span class="p">]</span> <span class="o">*</span> <span class="n">quantity</span><span class="p">)</span>
    <span class="nb">print</span><span class="p">(</span><span class="nb">str</span><span class="p">(</span><span class="nb">int</span><span class="p">(</span><span class="n">quantity</span><span class="p">))</span> <span class="o">+</span> <span class="s2">&quot; &quot;</span> <span class="o">+</span> <span class="n">item</span> <span class="o">+</span> <span class="s2">&quot;(s)&quot;</span> <span class="o">+</span> <span class="s2">&quot; added&quot;</span><span class="p">)</span>
    
<span class="c1"># user orders more or finishes order</span>
    <span class="n">item</span> <span class="o">=</span> <span class="nb">input</span><span class="p">(</span><span class="s2">&quot;Would you like to add more or finish order &#39;done&#39;&quot;</span><span class="p">)</span>
    <span class="n">item</span> <span class="o">=</span> <span class="n">item</span><span class="o">.</span><span class="n">lower</span><span class="p">()</span>
 <span class="c1">#order is being printed   </span>
<span class="nb">print</span><span class="p">(</span><span class="s2">&quot;Order:&quot;</span><span class="p">)</span>
<span class="nb">print</span><span class="p">(</span><span class="n">current_order</span><span class="p">)</span>
<span class="nb">print</span><span class="p">(</span><span class="s2">&quot;Price:&quot;</span><span class="p">)</span>
<span class="nb">print</span><span class="p">(</span><span class="s2">&quot;$&quot;</span> <span class="o">+</span> <span class="nb">str</span><span class="p">(</span><span class="nb">round</span><span class="p">(</span><span class="n">total</span><span class="p">,</span><span class="mi">2</span><span class="p">)))</span>


<span class="c1"># single item code </span>

<span class="c1"># if item == &quot;burger&quot; or item == &quot;fries&quot; or item == &quot;drink&quot;:</span>
<span class="c1">#     print(&quot;! The total of the order is&quot;, item, &quot;will be &quot;,menu[item])</span>
<span class="c1"># else:</span>
<span class="c1">#     print(&quot;Try again!&quot;)</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">

<div class="output_area">

<div class="output_subarea output_stream output_stdout output_text">
<pre>Menu:
burger  $3.99
fries  $1.99
drink  $0.99
4 burger(s) added
19 fries(s) added
2 drink(s) added
Order:
[&#39;burger X 4.0&#39;, &#39;fries X 19.0&#39;, &#39;drink X 2.0&#39;]
Price:
$55.75
</pre>
</div>
</div>

</div>
</div>

</div>
    {% endraw %}

</div>
 

