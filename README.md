# PrismCat
<img src="prismcat.png"  width="400">

## Explanation
PrismCat reads a file (or stdin) and highlights lines based on regex supplied in arguments. 

Colors follow the rainbow in priority e.g. (Error)>Red>Yellow>Green>Blue>Purple and are specified as arguments with their initial letter: -e -r -y -g -b -p, each taking a quoted regular expression as input. 

PrismCat can output to stdin, or to an html file (using the -o option) for future reference retaining the coloring. 

the -a flag eliminates all lines that aren't currently highlighted, filtering output to only the important lines. 

<body class="body_foreground body_background" style="font-size: normal;" >
<style type="text/css">
.ansi2html-content { display: inline; white-space: pre-wrap; word-wrap: break-word; }
.body_foreground { color: #AAAAAA; }
.body_background { background-color: #000000; }
.inv_foreground { color: #000000; }
.inv_background { background-color: #AAAAAA; }
.ansi4 { text-decoration: underline; }
.ansi91 { color: #ff0000; }
.ansi94 { color: #5c5cff; }
.ansi95 { color: #ff00ff; }
</style>
<pre class="ansi2html-content">

$ prism example.log.test -p '.*kernel.*' -e '.*PCI.*'
<span class="ansi95">Jul 27 14:41:58 combo kernel: Linux Plug and Play Support v0.97 (c) Adam Belay
</span>Jul 27 14:41:58 combo rc: Starting pcmcia:  succeeded
<span class="ansi95">Jul 27 14:41:58 combo kernel: usbcore: registered new driver usbfs
</span><span class="ansi95">Jul 27 14:41:58 combo kernel: usbcore: registered new driver hub
</span><span class="ansi91"></span><span class="ansi4 ansi91">Jul 27 14:41:58 combo kernel: ACPI: ACPI tables contain no PCI IRQ routing entries
</pre>
</body>

## Future
Eventually, PrismCat should be a full drop-in replacement for cat with the additional features provided in the current version