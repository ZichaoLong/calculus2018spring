.PHONY : pages update clean
DOCS=index 20180228 20180307 20180314 20180321 20180328 20180404
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
