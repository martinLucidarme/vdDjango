Insertion of html templates as a base
for every app (section) to use the same html template

Create your apps (blog app in this example)
in blog>template>blog> index.html  = html do blog
we want a html template, a general basis for this

go to main project file (here: meusite)
settings.py> TEMPLATES > 'DIRS' = [BASE_DIR / 'name_of_DIR']

in this DIR: create the base html

in base.html, have to respect Django language
example {%block 'name'%}{%endblock%}   to create and close a block

in blog>template>blog> index.html:

{%extends 'base.html'%} => Every time you want to use the base template

{%block 'name'%} content {%endblock%}
{%block 'name'%} content {%endblock%}
etc...
