#### Boucles Jekyll :

Faire une boucle sur une nav :  
* ajouter un titre à toutes les pages à ajouter
* ajouter "navigation_weight: (la place numérique de la page dans la nav)" ou ajouter 01.(nomdufichier), etc
* ajouter dans le header :  
    * dans le ul :   
        {% assign navigation_pages = site.html_pages | sort: 'navigation_weight' %}  
        {% for p in navigation_pages %}  
        {% if p.navigation_weight %}  
    * dans le a de li :  
        href="{{ p.url }}" {% if p.url == page.url %}class="active"{% endif %}>  
        {{ p.title }}  
    * après le li :  
        {% endif %}  
        {% endfor %}  
        
Faire une boucle pour appeler des articles :
* avant le li : {% for post in site.posts %}
* dans le a href : "{{ post.url }}">{{ post.title }}
* après le li : {% endfor %}
