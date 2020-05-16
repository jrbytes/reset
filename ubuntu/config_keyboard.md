On uBuntu 18.04:

Another options is to use Dconf-Editor, a powerful GUI for most uBuntu settings. 
If not installed, open Terminal and type:

```bash
apt-get update
apt-get install dconf-editor -y
```

Open dconf Editor  
Then /org/gnome/desktop/input-sources/xkb-options.

On a fresh uBuntu installation, Custom value will be blank. Turn Use default value OFF then:

Insert `['numpad:microsoft']` (if blank) or
append , 'numpad:microsoft' (after whatever is there, if not blank)
For example, ['caps:none', 'numpad:microsoft'] which both disables Caps Lock and uses the NumPad as in Windows.