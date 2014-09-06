Vagrant VM with Selenium and headless Chrome
============================================

Vagrantfile and Ansible playbook to setup an Ubuntu machine with a headless chrome browser for when full-blown browser automation is necessary.

    vagrant up
    vagrant ssh

Then, to check that it's working:

    vagrant@precise64:~$ python
    Python 2.7.3 (default, Feb 27 2014, 19:58:35) 
    [GCC 4.6.3] on linux2
    Type "help", "copyright", "credits" or "license" for more information.
    >>> from selenium import webdriver
    >>> driver = webdriver.Chrome()
    >>> driver.get('http://news.google.com')
    >>> driver.page_source
    u'<!DOCTYPE html><html xmlns="http://www.w3.org/1999/xhtml" ... etc ...

