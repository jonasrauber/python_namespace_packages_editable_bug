-----
Works
-----

```bash
sudo pip3 install main_package/
sudo pip3 install some_plugin/

python3 -c "import mainpackage; print(mainpackage.a)"
# -> hello

python3 -c "import mainpackage.ext.someplugin; print(mainpackage.ext.someplugin.a)"
# -> plugin
```

-----
Fails
-----

```bash
sudo pip3 install -e main_package/
sudo pip3 install -e some_plugin/

python3 -c "import mainpackage; print(mainpackage.a)"
# -> hello

python3 -c "import mainpackage.ext.someplugin; print(mainpackage.ext.someplugin.a)"
# -> ERROR

# Traceback (most recent call last):
#   File "<string>", line 1, in <module>
# ModuleNotFoundError: No module named 'mainpackage.ext.someplugin'
```

