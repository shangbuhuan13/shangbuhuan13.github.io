---
index: MonoRecon
permalink: /publications/MonoRecon
title: "Monocular piecewise depth estimation in dynamic scenes by exploiting superpixel relations"
authors: ['Yan Di', 'Henrique Morimitsu', 'Shan Gao', 'Xiangyang Ji'] 
authors_pub:['Yan Di, Henrique Morimitsu, Shan Gao, Xiangyang Ji']
venue: 'the IEEE/CVF International Conference on Computer Vision (ICCV)'
venue-abbr: 'ICCV'
venue-type: 'proceedings'
pages: 4363-4372
year: 2019
pdfurl: https://openaccess.thecvf.com/content_ICCV_2019/papers/Di_Monocular_Piecewise_Depth_Estimation_in_Dynamic_Scenes_by_Exploiting_Superpixel_ICCV_2019_paper.pdf
publisherurl: 
codeurl:
talkurl:
excerpt: 'Dense reconstruction.'
collection: publications
layout: archive
author_profile: true
---

{% include base_path %}

{%- if page.excerpt -%}
  ({{page.excerpt}})<br>
{%- endif -%}

{%- if page.pages -%}
  {%- for author in page.authors -%}
    {%- unless forloop.last -%}
      {{author}},&nbsp;
    {%- else -%}
      and {{author}}.
    {%- endunless -%}
  {%- endfor -%} <br>
  <i>{{ page.venue }} (<strong>{{ page.venue-abbr }}</strong>)</i>, pages {{ page.pages }}, {{ page.year }}.<br>
{%- else -%}
  {{ page.title }} <br>
  {%- for author in page.authors -%}
    {%- unless forloop.last -%}
      {{author}},&nbsp;
    {%- else -%}
      and {{author}}.
    {%- endunless -%}
  {%- endfor -%} <br>
  <i>{{ page.venue }} (<strong>{{ page.venue-abbr }}</strong>)</i>, (in print), {{ page.year }}.<br>
{%- endif -%}

{%- assign bibtex-id = {{ 'bibtex-' + page.index }} -%}

{%- if page.publisherurl -%}
  [[publisher]({{ page.publisherurl }})]&nbsp;
{%- endif -%}
{%- if page.pdfurl -%}
  [[pdf]({{ page.pdfurl }})]&nbsp;
{%- endif -%}
{%- if page.codeurl -%}
  [[code]({{ page.codeurl }})]&nbsp;
{%- endif -%}
[<a href="javascript:void(0)" onclick="(function(target, id) { if ($('#' + id).css('display') == 'block') { $('#' + id).hide('fast'); $(target).text('bibtex') } else { $('#' + id).show('fast'); $(target).text('bibtex▲') } })(this, '{{ bibtex-id }}');">bibtex</a>]
<div id='{{ bibtex-id }}' style="display:none">
  <pre>@inproceedings{ {{ page.index }},
    author    = {&nbsp;{%- for author in page.authors -%}
    {%- unless forloop.last -%}
      {{author}} and&nbsp;
    {%- else -%}
      {{author}}
    {%- endunless -%}
  {%- endfor -%}&nbsp;},
    title     = {Monocular piecewise depth estimation in dynamic scenes by exploiting superpixel relations},
    booktitle = {Proceedings of the IEEE/CVF International Conference on Computer Vision(ICCV)},
    pages     = {4363-4372},
    year      = {2019}
  }
  </pre>
</div>

{% if page.venue-type == 'proceedings' %}
<pre>
@inproceedings{ {{ page.index }},
  author    = {&nbsp;{%- for author in page.authors -%}
    {%- unless forloop.last -%}
      {{author}} and&nbsp;
    {%- else -%}
      {{author}}
    {%- endunless -%}
  {%- endfor -%}&nbsp;},
  title     = { {{ page.title }} },
  booktitle = { Proceedings of the {{page.venue}} ({{page.venue-abbr}}) },
  pages     = { {{ page.pages }} },
  year      = { {{ page.year }} }
}
</pre>
{% elsif page.venue-type == 'article' %}
<pre>
@article{ {{ page.index }},
  author    = {&nbsp;{%- for author in page.authors -%}
    {%- unless forloop.last -%}
      {{author}} and&nbsp;
    {%- else -%}
      {{author}}
    {%- endunless -%}
  {%- endfor -%}&nbsp;},
  title     = { {{ page.title }} },
  journal   = { {{ page.venue }} },
  pages     = { {{ page.pages }} },
  year      = { {{ page.year }} },
  doi       = { {{ page.publisher }} },
}
</pre>
{% endif %}
