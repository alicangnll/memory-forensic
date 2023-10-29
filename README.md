# AFF4 Acquisition Tool for Python
<h1>What is this ?</h1>
<p>This program takes a memory image in AFF4 format and you can easily analyze the memory image with this memory image.</p>
<h1>How can i use it?</h1>
<p>You must be run "pymem_snapshot.py" file on Windows</p>
<h1>OS Compatibility</h1>
<p>Windows</p>
<h1>Program Compatibility</h1>
<p>FTK Memory Analyzer (Stable)</p>
<p>Volatility (Testing)</p>
<br>
<h1>Memory Analyze 101</h1>
<h2>Byte Markers and Meanings</h2>
<h3>Files</h3>
<ul>
<li>ELF File : 7f 45 4c 46 02 01 01</li>
<li>JPEG File : ff d8 ff e0</li>
<li>7Z File : 37 7a bc af 27</li>
<li>AVI File : 41 56 49 20</li>
<li>BZ File : 42 5A 68</li>
<li>DOCX File : 50 4b 03 04 14</li>
<li>DOC File : d0 cf 11 e0 a1 / d0 cf 11 e0 a1 b1</li>
<li>PNG File : 89 50 4e 47 / 89 50 4e 47 0d 0a 1a 0a</li>
<li>RAR File : 52 61 72 21</li>
<li>ZIP File : 50 4b 30 30</li>
<li>EXE File : 4d 5a 90 00 03</li>
<li>PST File : 21 42 4e a5 6f b5 a6</li>
<li>LNK File : 4c 00 00 00 01 14 02 00 00 00 00 00 c0 00 00 00 00 00 00 46</li>
</ul>

<h3>File Tags</h3>
<ul>
<li>HTML (Lowercase) tag : 3c 68 74 6d</li>
<li>HTML (Uppercase) tag : 3c 48 54 4d</li>
<li>PLIST (Lowercase) tag : 70 6c 69 73 74</li>
</ul>

<h2>Volatility 3 - 101</h2>
<h4>Memory Image Informations</h4>
<p>vol.py -f "image.file" windows.info</p>
<h3>Process Infos (Windows)</h3>
<b>Process Information</b>
<p>vol.py -f "image.file" windows.pslist</p>
<p>vol.py -f "image.file" windows.psscan</p>
<p>vol.py -f "image.file" windows.pstree</p>
<p>vol.py -f "image.file" windows.psxview</p>
<b>Process Dump</b>
<p>vol.py -f "image.file" windows.dumpfiles --pid PID</p>
<b>Memory Dump</b>
<p>vol.py -f "/path/to/file" windows.memmap ‑‑dump ‑‑pid PID</p>

<h3>Command Line and NetScan (Windows)</h3>
<b>CmdLine</b>
<p>vol.py -f "/path/to/file" windows.cmdline</p>
<b>NetScan - NetStat</b>
<p>vol.py -f "/path/to/file" windows.netscan</p>
<p>vol.py -f "/path/to/file" windows.netstat</p>

<h4>Registry (Windows)</h4>
<b>HiveList</b>
<p>vol.py -f "/path/to/file" windows.registry.hivescan</p>
<p>vol.py -f "/path/to/file" windows.registry.hivelist</p>
<b>PrintKey</b>
<p>vol.py -f "/path/to/file" windows.registry.printkey</p>
<p>vol.py -f "/path/to/file" windows.registry.printkey ‑‑key "Software\Microsoft\Windows\CurrentVersion"</p>

<h4>Files (Windows)</h4>
<b>File Scan</b>
<p>vol.py -f "/path/to/file" windows.filescan</p>
<b>Dump Files</b>
<p>vol.py -f "/path/to/file" windows.dumpfiles</p>
<p>vol.py -f "/path/to/file" windows.dumpfiles ‑‑virtaddr OFFSET</p>
<p>vol.py -f "/path/to/file" windows.dumpfiles ‑‑physaddr OFFSET</p>

<h4>Others (Windows)</h4>
<b>Malfind</b>
<p>vol.py -f "/path/to/file" windows.malfind</p>
<b>YARA Scan</b>
<p>vol.py -f "/path/to/file" windows.vadyarascan ‑‑yara-rules STRING</p>
<p>vol.py -f "/path/to/file" windows.vadyarascan ‑‑yara-file "/path/to/file.yar"</p>
<p>vol.py -f "/path/to/file" windows.vadyarascan ‑‑yara-file "/path/to/file.yar"</p>
<b>Handles</b>
<p>vol.py -f "/path/to/file" windows.handles ‑‑pid PID</p>
<b>DLLS</b>
<p>vol.py -f "/path/to/file" windows.dlllist ‑‑pid PID</p>
