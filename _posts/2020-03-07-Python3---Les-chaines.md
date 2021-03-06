---
keywords: fastai
description: Initiation aux chaînes de caractères en Python
title: Les chaines de caracteres
toc: true
badges: true
comments: false
categories: [python, ISN]
nb_path: _notebooks/2020-03-07-Python3 - Les chaines.ipynb
layout: notebook
---

<!--
#################################################
### THIS FILE WAS AUTOGENERATED! DO NOT EDIT! ###
#################################################
# file to edit: _notebooks/2020-03-07-Python3 - Les chaines.ipynb
-->

<div class="container" id="notebook-container">
        
    {% raw %}
    
<div class="cell border-box-sizing code_cell rendered">

</div>
    {% endraw %}

    {% raw %}
    
<div class="cell border-box-sizing code_cell rendered">
<div class="input">

<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">chaine</span> <span class="o">=</span> <span class="s2">&quot;Lycée Salvador Allende&quot;</span>
<span class="n">chaine</span><span class="p">[</span><span class="mi">0</span><span class="p">]</span>
</pre></div>

    </div>
</div>
</div>

</div>
    {% endraw %}

<div class="cell border-box-sizing text_cell rendered"><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<p>Par contre, il est impossible de modifier une chaîne de caractères ! On dit alors qu'il s'agit d'une liste <em>non mutable</em> :</p>

</div>
</div>
</div>
    {% raw %}
    
<div class="cell border-box-sizing code_cell rendered">
<div class="input">

<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">chaine</span><span class="p">[</span><span class="mi">1</span><span class="p">]</span><span class="o">=</span> <span class="s2">&quot;a&quot;</span>
</pre></div>

    </div>
</div>
</div>

</div>
    {% endraw %}

<div class="cell border-box-sizing text_cell rendered"><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<p>Si vous décidiez de lui ajouter des caractères en fin de chaîne à l'aide d'une concaténation du type suivant :</p>

</div>
</div>
</div>
    {% raw %}
    
<div class="cell border-box-sizing code_cell rendered">
<div class="input">

<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">chaine</span> <span class="o">=</span> <span class="n">chaine</span><span class="o">+</span><span class="s2">&quot; - Hérouville saint clair&quot;</span>
<span class="n">chaine</span>
</pre></div>

    </div>
</div>
</div>

</div>
    {% endraw %}

<div class="cell border-box-sizing text_cell rendered"><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<p><strong><em>Remarque</em></strong> : Contrairement aux apparences, la chaine n'a pas été modifiée <em>puisque les chaines sont non mutables</em>, une nouvelle chaine a été crée par <em>concaténation</em> des deux chaines placées autour du signe <strong><em>+</em></strong></p>

</div>
</div>
</div>
<div class="cell border-box-sizing text_cell rendered"><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<p>Il existe de nombreuses méthodes agissant sur les chaînes de caratères. Pour les voir, vous pouvez utiliser la fonction d'<em>autocompletion</em> de Jupyter en tapant dans une cellule de code</p>

<pre><code>chaine. 

</code></pre>
<p>puis en pressant la touche <em>TAB</em>. N'oubliez pas le <strong><em>.</em></strong> !</p>
<p>Vous devriez voir la liste des méthodes disponibles :</p>
<table>
<thead><tr>
<th style="text-align:center">.</th>
<th style="text-align:center">.</th>
<th style="text-align:center">.</th>
<th style="text-align:center">.</th>
</tr>
</thead>
<tbody>
<tr>
<td style="text-align:center">x.capitalize</td>
<td style="text-align:center">x.isalnum</td>
<td style="text-align:center">x.join</td>
<td style="text-align:center">x.rsplit </td>
</tr>
<tr>
<td style="text-align:center">x.casefold</td>
<td style="text-align:center">x.isalpha</td>
<td style="text-align:center">x.ljust</td>
<td style="text-align:center">x.rstrip </td>
</tr>
<tr>
<td style="text-align:center">x.center</td>
<td style="text-align:center">x.isdecimal</td>
<td style="text-align:center">x.lower</td>
<td style="text-align:center">x.split</td>
</tr>
<tr>
<td style="text-align:center">x.count</td>
<td style="text-align:center">x.isdigit</td>
<td style="text-align:center">x.lstrip</td>
<td style="text-align:center">x.splitlines</td>
</tr>
<tr>
<td style="text-align:center">x.encode</td>
<td style="text-align:center">x.isidentifier</td>
<td style="text-align:center">x.maketrans</td>
<td style="text-align:center">x.startswith</td>
</tr>
<tr>
<td style="text-align:center">x.endswith</td>
<td style="text-align:center">x.islower</td>
<td style="text-align:center">x.partition</td>
<td style="text-align:center">x.strip</td>
</tr>
<tr>
<td style="text-align:center">x.expandtabs</td>
<td style="text-align:center">x.isnumeric</td>
<td style="text-align:center">x.replace</td>
<td style="text-align:center">x.swapcase</td>
</tr>
<tr>
<td style="text-align:center">x.find</td>
<td style="text-align:center">x.isprintable</td>
<td style="text-align:center">x.rfind</td>
<td style="text-align:center">x.title</td>
</tr>
<tr>
<td style="text-align:center">x.format</td>
<td style="text-align:center">x.isspace</td>
<td style="text-align:center">x.rindex</td>
<td style="text-align:center">x.translate</td>
</tr>
<tr>
<td style="text-align:center">x.format_map</td>
<td style="text-align:center">x.istitle</td>
<td style="text-align:center">x.rjust</td>
<td style="text-align:center">x.upper</td>
</tr>
<tr>
<td style="text-align:center">x.index</td>
<td style="text-align:center">x.isupper</td>
<td style="text-align:center">x.rpartition</td>
<td style="text-align:center">x.zfill</td>
</tr>
</tbody>
</table>

</div>
</div>
</div>
    {% raw %}
    
<div class="cell border-box-sizing code_cell rendered">
<div class="input">

<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">chaine</span><span class="o">.</span>
</pre></div>

    </div>
</div>
</div>

</div>
    {% endraw %}

<div class="cell border-box-sizing text_cell rendered"><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<p>Inutile de toutes les connaître. Nous allons voir ici les fonctions les plus utiles.</p>
<h2 id="Couper-et-joindre">Couper et joindre<a class="anchor-link" href="#Couper-et-joindre"> </a></h2><p>La fonction <strong><em>split()</em></strong> permet de <strong><em>découper</em></strong> la chaîne de caractères qui lui est passée en paramètre suivant un ou des caractère(s) de séparation et renvoie une liste des chaînes découpées. Les caractères de séparation lui sont également passés en paramètre et, si ce n'est pas le cas, ce sera le caractère espace qui sera utilisé :</p>

</div>
</div>
</div>
    {% raw %}
    
<div class="cell border-box-sizing code_cell rendered">
<div class="input">

<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">chaine</span><span class="o">=</span><span class="s2">&quot;Lycée Salvador Allende - Hérouville saint clair&quot;</span>
<span class="n">chaine</span><span class="o">.</span><span class="n">split</span><span class="p">()</span>
</pre></div>

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
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">chaine</span><span class="o">.</span><span class="n">split</span><span class="p">(</span><span class="s1">&#39;-&#39;</span><span class="p">)</span>
</pre></div>

    </div>
</div>
</div>

</div>
    {% endraw %}

<div class="cell border-box-sizing text_cell rendered"><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<p>L'opération inverse s'appelle <strong><em>join()</em></strong>. Elle consiste a rendre une liste de chaînes de caractères pour former une chaîne en concaténant tous les éléments et en les assemblant à l'aide d'un caractère.</p>
<p>Cette méthode prend en paramètre une liste de caractères et s'applique à une chaîne de caractères désignant le ou les caractère(s) de liaison :</p>

</div>
</div>
</div>
    {% raw %}
    
<div class="cell border-box-sizing code_cell rendered">
<div class="input">

<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">liste</span> <span class="o">=</span> <span class="p">[</span><span class="s1">&#39;Lycée Salvador Allende&#39;</span><span class="p">,</span> <span class="s1">&#39;Hérouville saint clair&#39;</span><span class="p">]</span>
<span class="s1">&#39; - &#39;</span><span class="o">.</span><span class="n">join</span><span class="p">(</span><span class="n">liste</span><span class="p">)</span>
</pre></div>

    </div>
</div>
</div>

</div>
    {% endraw %}

<div class="cell border-box-sizing text_cell rendered"><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h2 id="Majuscule-et-minuscule">Majuscule et minuscule<a class="anchor-link" href="#Majuscule-et-minuscule"> </a></h2><p>Deux autres méthodes standards peuvent être utiles:</p>
<p><strong><em>lower()</em></strong> et <strong><em>upper()</em></strong> permettant respectivement de convertir les caractères d'une chaîne en minuscules ou en majuscules.<br>
Attention, bien que parlant de <em>conversion</em>, ces méthodes ne modifient pas la chaîne de départ mais renvoient une nouvelle chaîne :</p>

</div>
</div>
</div>
    {% raw %}
    
<div class="cell border-box-sizing code_cell rendered">
<div class="input">

<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">chaine</span><span class="o">.</span><span class="n">upper</span><span class="p">()</span>
</pre></div>

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
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">chaine</span><span class="o">.</span><span class="n">lower</span><span class="p">()</span>
</pre></div>

    </div>
</div>
</div>

</div>
    {% endraw %}

<div class="cell border-box-sizing text_cell rendered"><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<p>La fonction <strong><em>capitalize()</em></strong> permet de ne mettre en majuscule que la première lettre d'une chaîne :</p>

</div>
</div>
</div>
    {% raw %}
    
<div class="cell border-box-sizing code_cell rendered">
<div class="input">

<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">chaine</span><span class="o">.</span><span class="n">capitalize</span><span class="p">()</span>
</pre></div>

    </div>
</div>
</div>

</div>
    {% endraw %}

<div class="cell border-box-sizing text_cell rendered"><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h2 id="rechercher-un-caract&#232;re,-une-position-etc...-dans-une-cha&#238;ne.">rechercher un caract&#232;re, une position etc... dans une cha&#238;ne.<a class="anchor-link" href="#rechercher-un-caract&#232;re,-une-position-etc...-dans-une-cha&#238;ne."> </a></h2><ul>
<li>La fonction <strong><em>len()</em></strong> permet, comme pour les listes, de connaîntre la longueur de la chaîne, c'est à dire compter le nombre de caractères.</li>
</ul>

</div>
</div>
</div>
    {% raw %}
    
<div class="cell border-box-sizing code_cell rendered">
<div class="input">

<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">chaine</span> <span class="o">=</span> <span class="s2">&quot;Lycée Salvador Allende&quot;</span>
<span class="nb">len</span><span class="p">(</span><span class="n">chaine</span><span class="p">)</span>
</pre></div>

    </div>
</div>
</div>

</div>
    {% endraw %}

<div class="cell border-box-sizing text_cell rendered"><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<ul>
<li>La méthode <strong><em>count()</em></strong> permet de compter le nombre d'occurrences d'une sous chaîne dans une chaîne de caractères.<br>
Le premier paramètre est la chaîne dans laquelle effectuer la recherche et le second paramètre est la sous chaîne :</li>
</ul>

</div>
</div>
</div>
    {% raw %}
    
<div class="cell border-box-sizing code_cell rendered">
<div class="input">

<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">chaine</span><span class="o">.</span><span class="n">count</span><span class="p">(</span><span class="s1">&#39;a&#39;</span><span class="p">)</span>
</pre></div>

    </div>
</div>
</div>

</div>
    {% endraw %}

<div class="cell border-box-sizing text_cell rendered"><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<ul>
<li>La méthode <strong><em>find()</em></strong> permet de trouver l'indice de la première occurrence d'une sous chaîne. Les paramètres sont les mêmes que pour la fonction <strong><em>count()</em></strong><br>
En cas d'échec, <strong><em>find()</em></strong> renvoie la valeur -1 ( 0 correspond à l'indice du premier caractère):
On utilisera <strong><em>rfind()</em></strong> pour la dernière ocurrence.</li>
</ul>

</div>
</div>
</div>
    {% raw %}
    
<div class="cell border-box-sizing code_cell rendered">
<div class="input">

<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">chaine</span><span class="o">.</span><span class="n">find</span><span class="p">(</span><span class="s1">&#39;a&#39;</span><span class="p">)</span>
</pre></div>

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
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">chaine</span><span class="o">.</span><span class="n">find</span><span class="p">(</span><span class="s1">&#39;b&#39;</span><span class="p">)</span>
</pre></div>

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
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">chaine</span><span class="o">.</span><span class="n">rfind</span><span class="p">(</span><span class="s1">&#39;a&#39;</span><span class="p">)</span>
</pre></div>

    </div>
</div>
</div>

</div>
    {% endraw %}

<div class="cell border-box-sizing text_cell rendered"><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<ul>
<li>index() est identique à find() mais retourne une erreur en cas d'échec</li>
</ul>

</div>
</div>
</div>
    {% raw %}
    
<div class="cell border-box-sizing code_cell rendered">
<div class="input">

<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">chaine</span><span class="o">.</span><span class="n">index</span><span class="p">(</span><span class="s1">&#39;a&#39;</span><span class="p">)</span>
</pre></div>

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
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">chaine</span><span class="o">.</span><span class="n">index</span><span class="p">(</span><span class="s1">&#39;b&#39;</span><span class="p">)</span>
</pre></div>

    </div>
</div>
</div>

</div>
    {% endraw %}

<div class="cell border-box-sizing text_cell rendered"><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<ul>
<li>La fonction <strong><em>replace()</em></strong> permet, comme son nom l'indique, de remplacer une sous chaîne par une autre à l'intérieur d'une chaîne de caractères.<br>
Les paramètres sont, dans l'ordre : la chaîne de caractères à modifier, la sous chaîne à remplacer, la sous chaîne de remplacement,et, éventuellement, le nombre maximum d'occurrences à remplacer (si non spécifié, toutes les occurrences seront remplacées).</li>
</ul>

</div>
</div>
</div>
    {% raw %}
    
<div class="cell border-box-sizing code_cell rendered">
<div class="input">

<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">chaine</span><span class="o">.</span><span class="n">replace</span><span class="p">(</span><span class="s1">&#39;a&#39;</span><span class="p">,</span><span class="s1">&#39;@&#39;</span><span class="p">)</span>
</pre></div>

    </div>
</div>
</div>

</div>
    {% endraw %}

<div class="cell border-box-sizing text_cell rendered"><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<p>et bien sûr, la variable <em>chaine</em> n'est pas modifiée, c'est une nouvelle chaine qui est renvoyée par cette méthode !</p>

</div>
</div>
</div>
    {% raw %}
    
<div class="cell border-box-sizing code_cell rendered">
<div class="input">

<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">chaine</span>
</pre></div>

    </div>
</div>
</div>

</div>
    {% endraw %}

<div class="cell border-box-sizing text_cell rendered"><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h2 id="Conversion-cha&#238;ne-&lt;-&gt;-nombres">Conversion cha&#238;ne &lt;-&gt; nombres<a class="anchor-link" href="#Conversion-cha&#238;ne-&lt;-&gt;-nombres"> </a></h2><p>Il ne faut pas confondre les objets 12 et "12". Le premier désigne un nombre, le second est une chaîne de caractère. Les comportements et les opérations sont différents.</p>

</div>
</div>
</div>
    {% raw %}
    
<div class="cell border-box-sizing code_cell rendered">
<div class="input">

<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="mi">12</span> <span class="o">==</span> <span class="s2">&quot;12&quot;</span>
</pre></div>

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
<div class=" highlight hl-ipython3"><pre><span></span><span class="mi">12</span><span class="o">+</span><span class="mi">1</span>
</pre></div>

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
<div class=" highlight hl-ipython3"><pre><span></span><span class="s2">&quot;12&quot;</span><span class="o">+</span><span class="s2">&quot;1&quot;</span>
</pre></div>

    </div>
</div>
</div>

</div>
    {% endraw %}

<div class="cell border-box-sizing text_cell rendered"><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<p>Il peut être néanmoins possible de convertir un nombre en chaîne et réciproquement comme on va le voir sur les exemples ci-dessous</p>

</div>
</div>
</div>
    {% raw %}
    
<div class="cell border-box-sizing code_cell rendered">
<div class="input">

<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="nb">int</span><span class="p">(</span><span class="s2">&quot;12&quot;</span><span class="p">)</span>
</pre></div>

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
<div class=" highlight hl-ipython3"><pre><span></span><span class="nb">str</span><span class="p">(</span><span class="mi">12</span><span class="p">)</span>
</pre></div>

    </div>
</div>
</div>

</div>
    {% endraw %}

<div class="cell border-box-sizing text_cell rendered"><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h2 id="Comparaison-de-cha&#238;nes-de-caract&#232;res">Comparaison de cha&#238;nes de caract&#232;res<a class="anchor-link" href="#Comparaison-de-cha&#238;nes-de-caract&#232;res"> </a></h2><p>De même qu'il est possible de comparer deux nombres, on peut aussi comparer des chaines par rapport à l'ordre lexicographique :</p>

</div>
</div>
</div>
    {% raw %}
    
<div class="cell border-box-sizing code_cell rendered">
<div class="input">

<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="s2">&quot;a&quot;</span><span class="o">&lt;</span><span class="s2">&quot;b&quot;</span>
</pre></div>

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
<div class=" highlight hl-ipython3"><pre><span></span><span class="s2">&quot;a&quot;</span><span class="o">&lt;=</span><span class="s2">&quot;r&quot;</span><span class="o">&lt;=</span><span class="s2">&quot;z&quot;</span>
</pre></div>

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
<div class=" highlight hl-ipython3"><pre><span></span><span class="s2">&quot;a&quot;</span><span class="o">&lt;=</span><span class="s2">&quot;R&quot;</span><span class="o">&lt;=</span><span class="s2">&quot;z&quot;</span>
</pre></div>

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
<div class=" highlight hl-ipython3"><pre><span></span><span class="s2">&quot;toto&quot;</span><span class="o">&lt;</span><span class="s2">&quot;titi&quot;</span>
</pre></div>

    </div>
</div>
</div>

</div>
    {% endraw %}

<div class="cell border-box-sizing text_cell rendered"><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h2 id="Tranches-de-cha&#238;nes">Tranches de cha&#238;nes<a class="anchor-link" href="#Tranches-de-cha&#238;nes"> </a></h2><p>Le tranchage (<em>slicing</em>) fonctionne exactement comme pour les listes. Observez les exemples suivants.</p>

</div>
</div>
</div>
    {% raw %}
    
<div class="cell border-box-sizing code_cell rendered">
<div class="input">

<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">chaine</span> <span class="o">=</span> <span class="s2">&quot;Lycée Salvador Allende&quot;</span>
<span class="c1"># obtenir la fin d&#39;une chaîne</span>
<span class="n">chaine</span><span class="p">[</span><span class="mi">6</span><span class="p">:]</span>
</pre></div>

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
<div class=" highlight hl-ipython3"><pre><span></span><span class="c1"># obtenir le début d&#39;une chaîne</span>
<span class="n">chaine</span><span class="p">[:</span><span class="mi">5</span><span class="p">]</span>
</pre></div>

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
<div class=" highlight hl-ipython3"><pre><span></span><span class="c1"># Un intervalle</span>
<span class="n">chaine</span><span class="p">[</span><span class="mi">6</span><span class="p">:</span><span class="mi">14</span><span class="p">]</span>
</pre></div>

    </div>
</div>
</div>

</div>
    {% endraw %}

<div class="cell border-box-sizing text_cell rendered"><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<p>Et avec des index négatifs ...</p>

</div>
</div>
</div>
    {% raw %}
    
<div class="cell border-box-sizing code_cell rendered">
<div class="input">

<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">chaine</span><span class="p">[</span><span class="o">-</span><span class="mi">1</span><span class="p">]</span>
</pre></div>

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
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">chaine</span><span class="p">[:</span><span class="o">-</span><span class="mi">1</span><span class="p">]</span>
</pre></div>

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
<div class=" highlight hl-ipython3"><pre><span></span><span class="c1"># ce dernier exemple est très pratique pour renverser un itérable</span>
<span class="n">chaine</span><span class="p">[::</span><span class="o">-</span><span class="mi">1</span><span class="p">]</span>
</pre></div>

    </div>
</div>
</div>

</div>
    {% endraw %}

<div class="cell border-box-sizing text_cell rendered"><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h2 id="Parcourir-une-cha&#238;ne-de-caract&#232;res">Parcourir une cha&#238;ne de caract&#232;res<a class="anchor-link" href="#Parcourir-une-cha&#238;ne-de-caract&#232;res"> </a></h2><p>Une chaîne de raractère en Python rentre dans la catégorie des <em>itérables</em> au même titre que les listes. On retrouve donc les deux modes de parcours déjà rencontrés sur les listes, à savoir :</p>

</div>
</div>
</div>
    {% raw %}
    
<div class="cell border-box-sizing code_cell rendered">
<div class="input">

<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="c1"># Le parcours caractères par caractères :</span>
<span class="n">chaine</span> <span class="o">=</span> <span class="s2">&quot;ISN&quot;</span>
<span class="k">for</span> <span class="n">c</span> <span class="ow">in</span> <span class="n">chaine</span><span class="p">:</span>
    <span class="nb">print</span><span class="p">(</span><span class="n">c</span><span class="p">)</span>
</pre></div>

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
<div class=" highlight hl-ipython3"><pre><span></span><span class="c1"># Le parcours par indice</span>
<span class="n">chaine</span> <span class="o">=</span> <span class="s2">&quot;ISN&quot;</span>
<span class="k">for</span> <span class="n">i</span> <span class="ow">in</span> <span class="nb">range</span><span class="p">(</span><span class="nb">len</span><span class="p">(</span><span class="n">chaine</span><span class="p">)):</span>
    <span class="nb">print</span><span class="p">(</span><span class="n">chaine</span><span class="p">[</span><span class="n">i</span><span class="p">])</span>
</pre></div>

    </div>
</div>
</div>

</div>
    {% endraw %}

<div class="cell border-box-sizing text_cell rendered"><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h2 id="Mise-en-pratique">Mise en pratique<a class="anchor-link" href="#Mise-en-pratique"> </a></h2><h3 id="Exercice-1">Exercice 1<a class="anchor-link" href="#Exercice-1"> </a></h3><p>Écrire une fonction <strong>nb_chiffres</strong> qui prend en paramètre une chaîne de caractère et qui renvoie le nombre de chiffres contenus dans la chaîne</p>

</div>
</div>
</div>
    {% raw %}
    
<div class="cell border-box-sizing code_cell rendered">
<div class="input">

<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="k">def</span> <span class="nf">nb_chiffres</span><span class="p">(</span><span class="n">chaine</span><span class="p">):</span>
    <span class="c1"># YOUR CODE HERE</span>
    <span class="k">raise</span> <span class="ne">NotImplementedError</span><span class="p">()</span>
</pre></div>

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
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">chaine</span> <span class="o">=</span> <span class="s2">&quot;Lycée Allende - 14200 Hérouville&quot;</span>
<span class="k">assert</span> <span class="n">nb_chiffres</span><span class="p">(</span><span class="n">chaine</span><span class="p">)</span><span class="o">==</span><span class="mi">5</span>
</pre></div>

    </div>
</div>
</div>

</div>
    {% endraw %}

<div class="cell border-box-sizing text_cell rendered"><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h3 id="Exercice-2">Exercice 2<a class="anchor-link" href="#Exercice-2"> </a></h3><p>Écrire une fonction <strong>is_email</strong> qui prend en paramètre une chaîne de caractère et renvoie True si celle-ci est une adresse mail. On va simplifier en considérant qu'on a une adresse email si la chaîne possède les 2 propriétés suivantes :</p>
<ul>
<li>Un seul caractère @</li>
<li>Un seul caractère .(point) après @.</li>
</ul>

</div>
</div>
</div>
    {% raw %}
    
<div class="cell border-box-sizing code_cell rendered">
<div class="input">

<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="k">def</span> <span class="nf">is_email</span><span class="p">(</span><span class="n">chaine</span><span class="p">):</span>
    <span class="c1"># YOUR CODE HERE</span>
    <span class="k">raise</span> <span class="ne">NotImplementedError</span><span class="p">()</span>
</pre></div>

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
<div class=" highlight hl-ipython3"><pre><span></span><span class="k">assert</span> <span class="n">is_email</span><span class="p">(</span><span class="s2">&quot;olivier.lecluse@monfai.com&quot;</span><span class="p">)</span>
<span class="k">assert</span> <span class="ow">not</span> <span class="n">is_email</span><span class="p">(</span><span class="s2">&quot;olivier.lecluse_AT_monfai.com&quot;</span><span class="p">)</span>
<span class="k">assert</span> <span class="ow">not</span> <span class="n">is_email</span><span class="p">(</span><span class="s2">&quot;olivier.lecluse@monfai&quot;</span><span class="p">)</span>
</pre></div>

    </div>
</div>
</div>

</div>
    {% endraw %}

<div class="cell border-box-sizing text_cell rendered"><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h3 id="Exercice-3">Exercice 3<a class="anchor-link" href="#Exercice-3"> </a></h3><p>Un nombre est un palindrome s'il s'écrit de la même manière de gauche à droite ou de droite à gauche. Exemple : 12521.</p>
<p>Ecrire une fonction <strong>est_palindrome</strong> prenant en paramètre un nombre et renvoyant <strong><em>True</em></strong> ou <strong><em>False</em></strong> selon que c'est un palindrom ou non.</p>

</div>
</div>
</div>
    {% raw %}
    
<div class="cell border-box-sizing code_cell rendered">
<div class="input">

<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="k">def</span> <span class="nf">est_palindrome</span><span class="p">(</span><span class="n">n</span><span class="p">):</span>
    <span class="c1"># YOUR CODE HERE</span>
    <span class="k">raise</span> <span class="ne">NotImplementedError</span><span class="p">()</span>
</pre></div>

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
<div class=" highlight hl-ipython3"><pre><span></span><span class="k">assert</span> <span class="n">est_palindrome</span><span class="p">(</span><span class="mi">12521</span><span class="p">)</span>
<span class="k">assert</span> <span class="ow">not</span> <span class="n">est_palindrome</span><span class="p">(</span><span class="mi">12520</span><span class="p">)</span>
</pre></div>

    </div>
</div>
</div>

</div>
    {% endraw %}

<div class="cell border-box-sizing text_cell rendered"><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h3 id="Exercice-4">Exercice 4<a class="anchor-link" href="#Exercice-4"> </a></h3><p>Ecrire une fonction <strong>somme_chiffres</strong> prenant un entier en paramètre et renvoyant la somme des chiffres de ce nombre.</p>
<p>somme_chiffres(125) renvoie 8 puisque 1+2+5=8</p>

</div>
</div>
</div>
    {% raw %}
    
<div class="cell border-box-sizing code_cell rendered">
<div class="input">

<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="k">def</span> <span class="nf">somme_chiffres</span><span class="p">(</span><span class="n">n</span><span class="p">):</span>
    <span class="c1"># YOUR CODE HERE</span>
    <span class="k">raise</span> <span class="ne">NotImplementedError</span><span class="p">()</span>
</pre></div>

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
<div class=" highlight hl-ipython3"><pre><span></span><span class="k">assert</span> <span class="n">somme_chiffres</span><span class="p">(</span><span class="mi">125</span><span class="p">)</span><span class="o">==</span><span class="mi">8</span>
</pre></div>

    </div>
</div>
</div>

</div>
    {% endraw %}

</div>
 

