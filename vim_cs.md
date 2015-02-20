set nonu nolist foldcolumn=0	#in order to copy a list
set folding

#installation hints
##terminal settings
TERM=xterm-256colors   #in .bashrc
set term=xterm-256colors	#in .vimrc
this is in order to avoid ESC strange characters 001B
##powerline fonts
take the ones with 'for powrline' sufix, there is a plenty of them on misc sites

#reload currently opened script
:so %

#buffers
:ls					#list buffers
:b <buffer number>	#switch to buffer
:b#, C-^			#previous buffer
:bp, :bn			#pervious, next buffer

