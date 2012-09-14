---
layout: page
title: Page d'Accueil 
comments: false
tagline: 
---
{% include JB/setup %}

## Où es tu ?

Hey! Si tu sais pas où tu es, je t'informe que tu es actuellement sur le blog de *David Guyon*.

Ce blog parle de ses passions, son parcours et sa vie en général.Plus précisément, il contient des articles sur ses études en Ecosse, sur l'électronique et l'informatique et pour finir, sur son site de compositions musicales [SongAccoustic](http://www.songaccoustic.fr)

Pour plus d'informations sur ce mec, va sur la page [About David](about.html)

## Dernier Article

{% assign lastPost = site.posts.first %}
### {{ lastPost.title }} - *{{ lastPost.date | date_to_string }}*
{{ lastPost.content | split:'<!-- break -->' | first }}
{% if lastPost.content contains '<!-- break -->' %}
  [Lire la suite...]({{lastPost.url }})
{% endif %}
