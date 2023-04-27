---
keywords: fastai
title: DevOps Lesson
toc: true
categories: []
type: pbl
nb_path: _notebooks/2023-04-26-devops-lesson.ipynb
layout: notebook
---

<!--
#################################################
### THIS FILE WAS AUTOGENERATED! DO NOT EDIT! ###
#################################################
# file to edit: _notebooks/2023-04-26-devops-lesson.ipynb
-->

<div class="container" id="notebook-container">
        
    {% raw %}
    
<div class="cell border-box-sizing code_cell rendered">
<div class="input">

<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="kn">import</span> <span class="nn">socket</span>

<span class="c1"># Change the following host and see what IP it prints!</span>
<span class="n">host</span> <span class="o">=</span> <span class="s2">&quot;google.com&quot;</span>
<span class="n">ip</span> <span class="o">=</span> <span class="n">socket</span><span class="o">.</span><span class="n">gethostbyname</span><span class="p">(</span><span class="n">host</span><span class="p">)</span>

<span class="nb">print</span><span class="p">(</span><span class="n">ip</span><span class="p">)</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">

<div class="output_area">

<div class="output_subarea output_stream output_stdout output_text">
<pre>142.250.189.14
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
<div class=" highlight hl-ipython3"><pre><span></span><span class="k">with</span> <span class="n">socket</span><span class="o">.</span><span class="n">socket</span><span class="p">(</span><span class="n">socket</span><span class="o">.</span><span class="n">AF_INET</span><span class="p">,</span> <span class="n">socket</span><span class="o">.</span><span class="n">SOCK_STREAM</span><span class="p">)</span> <span class="k">as</span> <span class="n">s</span><span class="p">:</span>
    <span class="n">s</span><span class="o">.</span><span class="n">connect</span><span class="p">((</span><span class="n">ip</span><span class="p">,</span> <span class="mi">80</span><span class="p">))</span>
    <span class="nb">print</span><span class="p">(</span><span class="s2">&quot;Successfully connected!&quot;</span><span class="p">)</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">

<div class="output_area">

<div class="output_subarea output_stream output_stdout output_text">
<pre>Successfully connected!
</pre>
</div>
</div>

</div>
</div>

</div>
    {% endraw %}

<div class="cell border-box-sizing text_cell rendered"><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h2 id="Check-In">Check-In<a class="anchor-link" href="#Check-In"> </a></h2><ol>
<li>What is an IP address?</li>
<li>What is a TCP port?</li>
</ol>

</div>
</div>
</div>
    {% raw %}
    
<div class="cell border-box-sizing code_cell rendered">
<div class="input">

<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="k">with</span> <span class="n">socket</span><span class="o">.</span><span class="n">socket</span><span class="p">(</span><span class="n">socket</span><span class="o">.</span><span class="n">AF_INET</span><span class="p">,</span> <span class="n">socket</span><span class="o">.</span><span class="n">SOCK_STREAM</span><span class="p">)</span> <span class="k">as</span> <span class="n">s</span><span class="p">:</span>
    <span class="n">s</span><span class="o">.</span><span class="n">connect</span><span class="p">((</span><span class="n">ip</span><span class="p">,</span> <span class="mi">80</span><span class="p">))</span>

    <span class="c1"># Send a GET request to &quot;/&quot;</span>
    <span class="n">s</span><span class="o">.</span><span class="n">sendall</span><span class="p">(</span><span class="sa">b</span><span class="s2">&quot;GET / HTTP/1.1</span><span class="se">\r\n\r\n</span><span class="s2">&quot;</span><span class="p">)</span>

    <span class="c1"># Recieve &amp; print 2048 bytes of data</span>
    <span class="n">data</span> <span class="o">=</span> <span class="n">s</span><span class="o">.</span><span class="n">recv</span><span class="p">(</span><span class="mi">2048</span><span class="p">)</span>
    <span class="nb">print</span><span class="p">(</span><span class="n">data</span><span class="o">.</span><span class="n">decode</span><span class="p">())</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">

<div class="output_area">

<div class="output_subarea output_stream output_stdout output_text">
<pre>HTTP/1.1 200 OK
Date: Wed, 26 Apr 2023 20:52:04 GMT
Expires: -1
Cache-Control: private, max-age=0
Content-Type: text/html; charset=ISO-8859-1
Content-Security-Policy-Report-Only: object-src &#39;none&#39;;base-uri &#39;self&#39;;script-src &#39;nonce-I6rYAT4cKhWK3B8_hzVosw&#39; &#39;strict-dynamic&#39; &#39;report-sample&#39; &#39;unsafe-eval&#39; &#39;unsafe-inline&#39; https: http:;report-uri https://csp.withgoogle.com/csp/gws/other-hp
P3P: CP=&#34;This is not a P3P policy! See g.co/p3phelp for more info.&#34;
Server: gws
X-XSS-Protection: 0
X-Frame-Options: SAMEORIGIN
Set-Cookie: 1P_JAR=2023-04-26-20; expires=Fri, 26-May-2023 20:52:04 GMT; path=/; domain=.google.com; Secure
Set-Cookie: AEC=AUEFqZcmXwwABrucuvamKJLByf3t_TkV_zy5XmS5mSCtumJ5KtiEVmzXVA; expires=Mon, 23-Oct-2023 20:52:04 GMT; path=/; domain=.google.com; Secure; HttpOnly; SameSite=lax
Set-Cookie: NID=511=HB-jM__FEcPwAv4Z_u4Uo6Uc2gLd2d53FnkbDzuKjxGmvHRgCCKFCMIRZ1IRRK2cXdXfAXgSBHyMr10Gm-sueqaNcpV2FoH0xF9-KmlMPrWqsgVuest6pJ899eai9hnjuQWvnf0uYLqs0H5GEnfjV2GBJN1Dde0ut--Y65Pyz9o; expires=Thu, 26-Oct-2023 20:52:04 GMT; path=/; domain=.google.com; HttpOnly
Accept-Ranges: none
Vary: Accept-Encoding
Transfer-Encoding: chunked

5998
&lt;!doctype html&gt;&lt;html itemscope=&#34;&#34; itemtype=&#34;http://schema.org/WebPage&#34; lang=&#34;en&#34;&gt;&lt;head&gt;&lt;meta content=&#34;Search the world&#39;s information, including webpages, images, videos and more. Google has many special features to help you find exactly what you&#39;re looking for.&#34; name=&#34;description&#34;&gt;&lt;meta content=&#34;noodp&#34; name=&#34;robots&#34;&gt;&lt;meta content=&#34;text/html; charset=UTF-8&#34; http-equiv=&#34;Content-Type&#34;&gt;&lt;meta content=&#34;/images/branding/googleg/1x/googleg_standard_color_128dp.png&#34; itemprop=&#34;image&#34;&gt;&lt;title&gt;Google&lt;/title&gt;&lt;script nonce=&#34;I6rYAT4cKhWK3B8_hzVosw&#34;&gt;(function(){window.google={kEI:&#39;9I5JZKyCOIXRkPIP09ig8Ac&#39;,kEXPI:&#39;0,1359409,6059,206,4804,2316,383,246,5,1129120,1197694,707,380089,16115,19397,9287,22430,1362,12316,4748,12835,4998,13228,3847,38444,2872,2891,3926,213,7615,606,30668,19390,10632,15324,432,3,346,1244,1,16916,2652,4,1528,2302,29064,9871,3194,11443,2215,2980,1457,16786,5797,2560,4094,7596
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
<div class=" highlight hl-ipython3"><pre><span></span><span class="kn">import</span> <span class="nn">requests</span>

<span class="c1"># Change the URL to whatever you&#39;d like</span>
<span class="n">response</span> <span class="o">=</span> <span class="n">requests</span><span class="o">.</span><span class="n">get</span><span class="p">(</span><span class="s2">&quot;https://google.com&quot;</span><span class="p">)</span>

<span class="nb">print</span><span class="p">(</span><span class="s2">&quot;Status code:&quot;</span><span class="p">,</span> <span class="n">response</span><span class="o">.</span><span class="n">status_code</span><span class="p">)</span>
<span class="nb">print</span><span class="p">(</span><span class="s2">&quot;Headers:&quot;</span><span class="p">,</span> <span class="n">response</span><span class="o">.</span><span class="n">headers</span><span class="p">)</span>
<span class="nb">print</span><span class="p">(</span><span class="s2">&quot;Response text:&quot;</span><span class="p">,</span> <span class="n">response</span><span class="o">.</span><span class="n">text</span><span class="p">[:</span><span class="mi">100</span><span class="p">])</span>

<span class="c1"># Add a line to print the &quot;Content-Type&quot; header of the response</span>
<span class="c1"># Try an image URL!</span>
</pre></div>

    </div>
</div>
</div>

</div>
    {% endraw %}

<div class="cell border-box-sizing text_cell rendered"><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h1 id="NGINX">NGINX<a class="anchor-link" href="#NGINX"> </a></h1>
</div>
</div>
</div>
    {% raw %}
    
<div class="cell border-box-sizing code_cell rendered">
<div class="input">

<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">aws</span> <span class="o">=</span> <span class="s2">&quot;3.130.255.192&quot;</span>

<span class="n">response</span> <span class="o">=</span> <span class="n">requests</span><span class="o">.</span><span class="n">get</span><span class="p">(</span><span class="s2">&quot;http://&quot;</span> <span class="o">+</span> <span class="n">aws</span><span class="p">)</span>
<span class="nb">print</span><span class="p">(</span><span class="n">response</span><span class="o">.</span><span class="n">text</span><span class="p">)</span>
</pre></div>

    </div>
</div>
</div>

</div>
    {% endraw %}

<div class="cell border-box-sizing text_cell rendered"><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h2 id="Configuration">Configuration<a class="anchor-link" href="#Configuration"> </a></h2><div class="highlight"><pre><span></span><span class="k">server</span> <span class="p">{</span>
    <span class="kn">//</span> <span class="s">Listen</span> <span class="no">on</span> <span class="s">virtual</span> <span class="s">&quot;port</span> <span class="mi">80</span><span class="s">&quot;</span>
    <span class="s">listen</span> <span class="mi">80</span><span class="p">;</span>
    <span class="kn">listen</span> <span class="s">[::]:80</span><span class="p">;</span>
    <span class="kn">server_name</span> <span class="mi">3</span><span class="s">.130.255.192</span><span class="p">;</span>

    <span class="kn">location</span> <span class="s">/</span> <span class="p">{</span>
        <span class="kn">//</span> <span class="s">Inform</span> <span class="s">server</span> <span class="s">about</span> <span class="s">original</span> <span class="s">client</span>
        <span class="s">proxy_set_header</span>        <span class="s">Host</span> <span class="nv">$host</span><span class="p">;</span>
        <span class="kn">proxy_set_header</span>        <span class="s">X-Real-IP</span> <span class="nv">$remote_addr</span><span class="p">;</span>
        <span class="kn">proxy_set_header</span>        <span class="s">X-Forwarded-For</span> <span class="nv">$proxy_add_x_forwarded_for</span><span class="p">;</span>
        <span class="kn">proxy_set_header</span>        <span class="s">X-Forwarded-Proto</span> <span class="nv">$scheme</span><span class="p">;</span>

        <span class="kn">//</span> <span class="s">Forward</span> <span class="s">all</span> <span class="s">requests</span> <span class="s">transparently</span> <span class="s">to</span> <span class="s">the</span> <span class="s">server</span> <span class="s">running</span> <span class="no">on</span> <span class="s">our</span> <span class="s">computer</span>
        <span class="s">proxy_pass</span>              <span class="s">http://localhost:9099</span><span class="p">;</span>
    <span class="p">}</span>
<span class="p">}</span>
</pre></div>
<h3 id="Load-Balancing">Load Balancing<a class="anchor-link" href="#Load-Balancing"> </a></h3><div class="highlight"><pre><span></span><span class="k">upstream</span> <span class="s">example.com</span> <span class="p">{</span>
    <span class="kn">server</span> <span class="s">server1.example.com</span><span class="p">;</span>
    <span class="kn">server</span> <span class="s">server1.example.com</span><span class="p">;</span>
<span class="p">}</span>
</pre></div>
<h3 id="HTTP-Headers">HTTP Headers<a class="anchor-link" href="#HTTP-Headers"> </a></h3><div class="highlight"><pre><span></span><span class="k">server</span> <span class="p">{</span>
    <span class="kn">add_header</span> <span class="s">X-Cool-Header</span> <span class="s">&quot;I</span> <span class="s">love</span> <span class="s">APCSP!&quot;</span><span class="p">;</span>

    <span class="kn">location</span> <span class="s">/pages</span> <span class="p">{</span>
        <span class="kn">add_header</span> <span class="s">X-Cooler-Header</span> <span class="s">&quot;This</span> <span class="s">is</span> <span class="s">my</span> <span class="s">secret</span> <span class="s">header!&quot;</span><span class="p">;</span>
    <span class="p">}</span>
<span class="p">}</span>
</pre></div>
<h2 id="Check-In">Check In<a class="anchor-link" href="#Check-In"> </a></h2><ol>
<li>Research 1 HTTP header and describe, in detail, its purpose.</li>
<li>Write a line in a sample NGINX configuration that will add that specific header to the <code>/information</code> location</li>
<li>Explain the purpose of the load balancing performed by NGINX</li>
<li>Modify the following code block to obtain the value of the secret header on <code>/products</code> of the AWS site</li>
</ol>

</div>
</div>
</div>
    {% raw %}
    
<div class="cell border-box-sizing code_cell rendered">
<div class="input">

<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">aws</span> <span class="o">=</span> <span class="s2">&quot;3.130.255.192&quot;</span>

<span class="n">response</span> <span class="o">=</span> <span class="n">requests</span><span class="o">.</span><span class="n">get</span><span class="p">(</span><span class="s2">&quot;http://&quot;</span> <span class="o">+</span> <span class="n">aws</span><span class="o">+</span> <span class="s2">&quot;/products&quot;</span><span class="p">)</span>

<span class="nb">print</span><span class="p">(</span><span class="s2">&quot;The secret header is:&quot;</span><span class="p">,</span> <span class="s2">&quot;...&quot;</span><span class="p">)</span>
</pre></div>

    </div>
</div>
</div>

</div>
    {% endraw %}

<div class="cell border-box-sizing text_cell rendered"><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h1 id="Hacks">Hacks<a class="anchor-link" href="#Hacks"> </a></h1><ul>
<li>Complete the above check-in questions and change the hosts (0.1)</li>
<li>Complete the above code-segment to retrieve the secret header (0.1)</li>
</ul>
<h2 id="Bonus-(0.05)">Bonus (0.05)<a class="anchor-link" href="#Bonus-(0.05)"> </a></h2><p>Create a diagram showing the layers of abstraction that allow us to use HTTP (IP, TCP, etc.)</p>

</div>
</div>
</div>
<div class="cell border-box-sizing text_cell rendered"><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h1 id="CORS-Hacks">CORS Hacks<a class="anchor-link" href="#CORS-Hacks"> </a></h1><ol>
<li>Explain what CORS is and what it stands for</li>
<li>Describe how you would be able to implement CORS into your own websites</li>
<li>Describe why you would want to implement CORS into your own websites</li>
<li>How could use CORS to benefit yourself in the future?</li>
</ol>
<p>Total: 0.2 points</p>
<h1 id="KASM-Hacks">KASM Hacks<a class="anchor-link" href="#KASM-Hacks"> </a></h1><ol>
<li>What is the purpose of "sudo" when running commands in terminal?</li>
<li>What are some commands which allow us to look at how the storage of a machine is set up as?</li>
<li>What do you think are some alternatives to running "curl -O" to get the zip file for KASM?</li>
<li>What kind of commands do you think the "install.sh" command has and why is it necessary to call it?</li>
<li>Explain in at least 3-4 sentences how deploying KASM is related to/requires other topics talked about in the lesson and/or potential ways to add things mentioned in the lesson to this guide.</li>
</ol>
<p>Total: 0.2 points</p>
<h1 id="AWS/RDS-Hacks">AWS/RDS Hacks<a class="anchor-link" href="#AWS/RDS-Hacks"> </a></h1><p>See the <a href="https://firestorm0986.github.io/SLAAT/posts/sqlite-aws/">setup post</a></p>
<ul>
<li>Create your own database in the EC2 I have created (ec2-database-connect)<ul>
<li>name it with your first and last name (example: aditya-nawandhar) (0.1)</li>
<li>Create a table using the commands on the link provided. (0.1)</li>
<li>using commands from the link provided make columns and rows with test data (can be anything) (example: “name” and “class” are the columns with rows being something like “Aditya” and “Junior”). At least 4 test rows (0.1)</li>
<li>additional points if the data matches CPT (Bonus: 0.05)</li>
</ul>
</li>
</ul>
<p>Total: 0.3</p>

</div>
</div>
</div>
</div>
 
