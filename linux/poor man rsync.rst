poor man rysnc
==============

::

    push files to server:

    server:
    nc -l -p 38383 | openssl aes-128-cbc -d -k 'secret' | tar zxf -
    
    client:
    tar czf - . | openssl aes-128-cbc -k 'secret' | nc dabin.info 38383


    pull files from server: (needs server to send ctrl + c)
    
    server:
    
    tar czf - 'Kung Fu porn-461.mp4' | openssl aes-128-cbc -k 'secret' | nc -l -p 38383
    
    client:
    
    nc dabin.info 38383 | openssl aes-128-cbc -d -k 'secret' | pv | tar zvvxf 
