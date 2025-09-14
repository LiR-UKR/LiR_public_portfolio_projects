
##---------Lib from bs4 import BeautifulSoup
##Beautiful Soup – это Python библиотека для синтаксического разбора файлов HTML/XML, которая может преобразовать даже неправильную разметку в дерево синтаксического разбора.

soup.title              # <title>The Dormouse's story</title>
soup.title.name         # u'title'
soup.title.string       # u'The Dormouse's story'
soup.title.parent.name  # u'head'
soup.p                  # <p class="title"><b>The Dormouse's story</b></p>
soup.p['class']         # u'title'
soup.a                  # <a class="sister" href="http://example.com/elsie" id="link1">Elsie</a>

soup.find_all('a')      # [<a class="sister" href="http://example.com/elsie" id="link1">Elsie</a>,
                        #  <a class="sister" href="http://example.com/lacie" id="link2">Lacie</a>,
                        #  <a class="sister" href="http://example.com/tillie" id="link3">Tillie</a>]

soup.find(id="link3")   # <a class="sister" href="http://example.com/tillie" id="link3">Tillie</a>

One common task is extracting all the URLs found within a page’s <a> tags:
for link in soup.find_all('a'):
    print(link.get('href'))



params = передавать допольнительные теги фильтрации и данные{class_/href_/meta:"Какой-то текст"}
requests.get(url,headers,params={key:value}) - простой запрос на получение и анализ данных с сайта
---------------------------------
session = request.Session()
requests = session.post(....)
requests = session.get(....)
---------------------------------
при попомщи post можно вставить все данные ввода на сайт, просмотрев его предварительно названия через F12
data ={key:value,name:login, password: "1234567",custName: "Name", Telephone:"123456"}
requests.post(url,headers,data=dict{key:value}) - запрос получение страницы через авторизацию, для сервисов

------------------------------------------------------------
find_all(name, attrs, recursive, string, limit, **kwargs)
name    - это имя тега
limit   - кол тегов
attribute=True - все элементы с определенным атрибутом независимо от его значения,
recursive=False - искать элемент только в прямых дочерних элементах в теге
string - содержимое тега на заданную строку
------------------------------------------Parser Typical usage
Python’s html.parser    ->  BeautifulSoup(markup, "html.parser"
lxml’s HTML parser      ->  BeautifulSoup(markup, "lxml")
lxml’s XML parser       ->  BeautifulSoup(markup, "lxml-xml") BeautifulSoup(markup, "xml")
html5lib                ->  BeautifulSoup(markup, "html5lib")

$ apt-get install python3-html5lib
$ pip install html5lib
----------------------------------------------------------
----------------------------------------------------------


Method names
renderContents -> encode_contents

replaceWith -> replace_with

replaceWithChildren -> unwrap

findAll -> find_all

findAllNext -> find_all_next

findAllPrevious -> find_all_previous

findNext -> find_next

findNextSibling -> find_next_sibling

findNextSiblings -> find_next_siblings

findParent -> find_parent

findParents -> find_parents

findPrevious -> find_previous

findPreviousSibling -> find_previous_sibling

findPreviousSiblings -> find_previous_siblings

getText -> get_text

nextSibling -> next_sibling

previousSibling -> previous_sibling

