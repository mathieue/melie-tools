Melie Tools
======================
Trivial bash tools make linux user life easyer and happyer

Just simple bash scripts wrapper to find, grep and rgrep. Helping to find files and code quickly and open them in editor
in a lazy way.


melie-find
----------------------
	melie-find [iname] [pattern...] [-e]

Find paths. The first parameter mustbe a part of the file or last directory of the path.
The following patterns are parts of the directory to match.

-e open resulting files in editor.

ex:
	find iname . | grep pattern1 | grep pattern2 | grep pattern3    

melie-rgrep
----------------------
	melie-rgrep pattern [pattern...] [-e]

Rgrep a pattern in current path.
The following patterns are parts of the directory to match.

-e open resulting files in editor.

ex:
	rgrep pattern1 | grep pattern2 | grep pattern3

melie-grep
----------------------
	melie-grep pattern [pattern..]

Grep a pattern.
The following patterns are parts of the directory to match.

ex:
	grep pattern1 | grep pattern2 | grep pattern3
