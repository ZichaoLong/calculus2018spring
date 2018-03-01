.PHONY : pages update clean
DOCS=index 20180228
UTILS=../utils/
PREFIX=../

HDOCS=$(addsuffix .html, $(DOCS))
PHDOCS=$(addprefix $(PREFIX), $(HDOCS))

pages : $(PHDOCS)

update : $(PHDOCS)
	@echo -n 'Copying to server...'
	# insert code for copying to server here.
	@echo ' done.'

$(PREFIX)%.html : %.jemdoc MENU
	$(UTILS)jemdoc.py -o $@ $<

clean :
	-rm -f $(PREFIX)*.html
