CFLAGS=-Wall -g
OUTDIR=$(shell pwd)/out/
NAME=$(notdir $(shell pwd))
MACRO=
.SILENT: r  	# silence the output for the 'make run'. The echo statements are not silenced

a: cl cpl

cl: 					# make clean
	@echo "... cleaning $(OUTDIR) directory ..."
	rm -rf $(OUTDIR)

cpl:					# make compile
	@echo "... creating the output directory ..."
	mkdir $(OUTDIR)
	
	@echo "... compiling $(NAME) ..."
	cc $(CFLAGS) $(MACRO) -o $(addprefix $(OUTDIR), $(NAME)) $(NAME).c

r:						# make run
	@echo "... running $(NAME) -- program output after the dots ..."
	@echo "...................................................."
	$(OUTDIR)$(NAME)
	
tm: 					# make testmake. This one tests / prints out the variables that are set or constructed. Used for quick debugging
	@echo NAME == $(NAME)
	@echo OUTDIR == $(OUTDIR)
	@echo CC CMD == cc $(CFLAGS) $(MACRO) -o $(addprefix $(OUTDIR), $(NAME))

grnd: 				# for valgrind invocation
	@echo "... running with Valgrind ..."
	valgrind $(RUNCMD) $(PARAM) 
