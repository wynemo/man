curl
====

::

    # cookie
    curl 'http://foo.baar' -H 'Cookie: cookie1=123;cookie2=456'

    # post
    curl -s -D - -d "client_name=web&pin_code=123456" http://foo.bar
