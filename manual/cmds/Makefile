FILES=comp.tex top.tex runtime.tex native.tex lexyacc.tex intf-c.tex \
  depend.tex profil.tex debugger.tex browser.tex ocamldoc.tex warnings.tex \
  ocamlbuild.tex

TRANSF=../../tools/transf
TEXQUOTE=../../tools/texquote2
FORMAT=../../tools/format-intf

all: $(FILES)

clean:
	rm -f $(FILES)
	rm -f *~ #*#

.SUFFIXES:
.SUFFIXES: .tex .etex

.etex.tex:
	$(TEXQUOTE) < $*.etex > $*.tex

ocamldoc.tex: ocamldoc.etex $(TRANSF)
	$(TRANSF) < ocamldoc.etex | $(TEXQUOTE) > ocamldoc.tex

top.tex: top.etex $(TRANSF)
	$(TRANSF) < top.etex | $(TEXQUOTE) > top.tex

intf-c.tex: intf-c.etex $(TRANSF)
	$(TRANSF) < intf-c.etex | $(TEXQUOTE) > intf-c.tex

lexyacc.tex: lexyacc.etex $(TRANSF)
	$(TRANSF) < lexyacc.etex | $(TEXQUOTE) > lexyacc.tex

debugger.tex: debugger.etex $(TRANSF)
	$(TRANSF) < debugger.etex | $(TEXQUOTE) > debugger.tex

warnings.etex: ../warnings.etex
	cp ../warnings.etex .
