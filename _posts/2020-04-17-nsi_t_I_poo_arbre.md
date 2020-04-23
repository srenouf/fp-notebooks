---
keywords: fastai
description: Cours NSI Terminale - Thème 1.
title: Implémenter la classe arbre binaire
toc: false 
badges: true
comments: false
categories: [python, NSI, Terminale, Structure_donnees, POO, TP]
nb_path: _notebooks/2020-04-17-nsi_t_I_poo_arbre.ipynb
layout: notebook
---

<!--
#################################################
### THIS FILE WAS AUTOGENERATED! DO NOT EDIT! ###
#################################################
# file to edit: _notebooks/2020-04-17-nsi_t_I_poo_arbre.ipynb
-->

<div class="container" id="notebook-container">
        
    {% raw %}
    
<div class="cell border-box-sizing code_cell rendered">

</div>
    {% endraw %}

<div class="cell border-box-sizing text_cell rendered"><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<p>Dans ce TP nous allons implémenter une classe permettant de représenter un arbre binaire.</p>
<p>Voici le schéma de la structure envisagée pour la classe <strong>Arbrebin</strong></p>
<p><img src="/images/copied_from_nb/classeArbrebin.png" alt="classe Arbrebin"></p>
<p>La propriété <strong>valeur</strong> contiendra la valeur associée au noeud. Les propriétés <strong>gauche</strong> et <strong>droit</strong> seront les sous arbres gauche et droit. Ces deux propriétés seront donc des instances de la classe <strong>Arbrebin</strong>. Si il n'y a pas de sous arbre gauche ou droit, on indiquera la valeur <strong>None</strong> dans les propriétés correspondantes.</p>
<p>La méthode <strong>est_feuille</strong> renverra un bouléen selon que l'objet est une feuille ou non.
La méthode <strong>cree_fils_gauche()</strong> prend en paramètre une valeur et crée un fils à gauche dont la valeur est passée en paramètres.</p>
<h2 id="Exemple-d'utilisation-de-la-classe-Arbrebin">Exemple d'utilisation de la classe Arbrebin<a class="anchor-link" href="#Exemple-d'utilisation-de-la-classe-Arbrebin"> </a></h2><p>En supposant la classe <strong>Arbrebin</strong> créée, voici comment on l'utilise pour créer cet arbre :
<img src="/images/copied_from_nb/arbre1.png" alt="arbre exemple"></p>
<div class="highlight"><pre><span></span><span class="nv">arbre</span> <span class="o">=</span> Arbrebin<span class="o">(</span><span class="s2">&quot;A&quot;</span><span class="o">)</span>
<span class="nv">sous_arbre_gauche</span> <span class="o">=</span> arbre.cree_fils_gauche<span class="o">(</span><span class="s2">&quot;B&quot;</span><span class="o">)</span>
sous_arbre_gauche.cree_fils_gauche<span class="o">(</span><span class="s2">&quot;D&quot;</span><span class="o">)</span>
arbre.cree_fils_droit<span class="o">(</span><span class="s2">&quot;C&quot;</span><span class="o">)</span>

<span class="c1"># Quelques vérifications possibles</span>
print<span class="o">(</span>arbre.est_feuille<span class="o">())</span>
print<span class="o">(</span>arbre.droit.est_feuille<span class="o">())</span>
print<span class="o">(</span>arbre.gauche.valeur<span class="o">)</span>
<span class="c1"># Affiche False True B</span>
</pre></div>

</div>
</div>
</div>
    {% raw %}
    
<div class="cell border-box-sizing code_cell rendered">
<div class="input">

<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="k">class</span> <span class="nc">Arbrebin</span><span class="p">():</span>
    
    <span class="c1"># la méthode __repr__ définit ce qui sera affiché</span>
    <span class="c1"># lorsqu&#39;on tapera l&#39;objet dans Jupyter ou un terminal</span>
    <span class="c1"># Ici, on affiche juste al valeur du noeud</span>
    
    <span class="k">def</span> <span class="fm">__repr__</span><span class="p">(</span><span class="bp">self</span><span class="p">):</span>
        <span class="k">return</span> <span class="nb">str</span><span class="p">(</span><span class="bp">self</span><span class="o">.</span><span class="n">valeur</span><span class="p">)</span>
    
    <span class="c1"># Codez ici les méthodes demandées</span>
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
<div class=" highlight hl-ipython3"><pre><span></span><span class="c1"># Testez ici les méthodes de votre classe</span>
<span class="n">a</span> <span class="o">=</span> <span class="n">Arbrebin</span><span class="p">(</span><span class="mi">2</span><span class="p">)</span>
<span class="n">a</span>
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
<div class=" highlight hl-ipython3"><pre><span></span><span class="c1"># Tester l&#39;exemple de départ</span>

<span class="n">arbre</span> <span class="o">=</span> <span class="n">Arbrebin</span><span class="p">(</span><span class="s2">&quot;A&quot;</span><span class="p">)</span>
<span class="n">sous_arbre_gauche</span> <span class="o">=</span> <span class="n">arbre</span><span class="o">.</span><span class="n">cree_fils_gauche</span><span class="p">(</span><span class="s2">&quot;B&quot;</span><span class="p">)</span>
<span class="n">sous_arbre_gauche</span><span class="o">.</span><span class="n">cree_fils_gauche</span><span class="p">(</span><span class="s2">&quot;D&quot;</span><span class="p">)</span>
<span class="n">arbre</span><span class="o">.</span><span class="n">cree_fils_droit</span><span class="p">(</span><span class="s2">&quot;C&quot;</span><span class="p">)</span>

<span class="k">assert</span> <span class="ow">not</span> <span class="n">arbre</span><span class="o">.</span><span class="n">est_feuille</span><span class="p">()</span>
<span class="k">assert</span> <span class="n">arbre</span><span class="o">.</span><span class="n">droit</span><span class="o">.</span><span class="n">est_feuille</span><span class="p">()</span>
<span class="k">assert</span> <span class="n">arbre</span><span class="o">.</span><span class="n">gauche</span><span class="o">.</span><span class="n">valeur</span> <span class="o">==</span> <span class="s2">&quot;B&quot;</span>
</pre></div>

    </div>
</div>
</div>

</div>
    {% endraw %}

<div class="cell border-box-sizing text_cell rendered"><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<p>A présent, vous utiliserez la classe Arbrebin et les méthodes que vous avez développées pour représenter l'arbre suivant dans la variable <code>expr</code>
<img src="/images/copied_from_nb/expr.png" alt="expression"></p>
<p>Les opérations seront représentées par des chaînes de caractères. Les feuilles seront des entiers.</p>

</div>
</div>
</div>
    {% raw %}
    
<div class="cell border-box-sizing code_cell rendered">
<div class="input">

<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">expr</span> <span class="o">=</span> <span class="o">...</span>
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
<div class=" highlight hl-ipython3"><pre><span></span><span class="c1"># Validation de la réponse</span>
<span class="k">assert</span> <span class="n">expr</span><span class="o">.</span><span class="n">valeur</span> <span class="o">==</span> <span class="s2">&quot;+&quot;</span>
<span class="k">assert</span> <span class="n">expr</span><span class="o">.</span><span class="n">droit</span><span class="o">.</span><span class="n">valeur</span> <span class="o">==</span> <span class="mi">1</span>
</pre></div>

    </div>
</div>
</div>

</div>
    {% endraw %}

</div>
 
