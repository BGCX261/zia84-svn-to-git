##
## Makefile.am for zia in /home/elthariel/code/httpd/src
##
## Made by Nahlwe
## Login   <elthariel@lse.epita.fr>
##

noinst_HEADERS = foncteurs.hpp help.hpp \
	thread.hpp worker.hpp main.hpp conf.hpp http_request.hpp socket.hpp dired.hpp \
	parsing.hpp modrequestadapter.hpp modresponseadapter.hpp modrawadapter.hpp

#######################
# Build an executable #
#######################

#INCLUDES = -I $(top_builddir)/src

bin_PROGRAMS = zia modapitest cgi_test
zia_SOURCES = foncteurs.cpp help.cpp thread.cpp \
	worker.cpp main.cpp conf.cpp http_request.cpp socket.cpp dired.cpp \
	parsing.cpp modrequestadapter.cpp modresponseadapter.cpp \
	modrawadapter.cpp my_uuid.cpp mod_manager.cpp mod_q_out.cpp \
	module_loader.cpp

# Don't forget that the order of the libraries _does_ matter
zia_CPPFLAGS = -g -Wall $(LIBXML_CFLAGS) $(ARCH_CFLAGS) -I../modapi
zia_LDADD = -lpthread $(LIBXML_LIBS) $(ARCH_LDADD)

modapitest_SOURCES = mod_manager.cpp mod_q_out.cpp \
	module_loader.cpp modapitest.cpp
modapitest_CPPFLAGS = -g -Wall $(LIBXML_CFLAGS) $(ARCH_CFLAGS) -I../modapi
modapitest_LDADD = -lpthread $(LIBXML_LIBS) $(ARCh_LDADD)

cgi_test_SOURCES = cgi_test.cpp


##########
# Checks #
##########

# --> make check
#TESTS = test-1.sh test-
#TESTS = zia_test.sh
#check_PROGRAMS = test-2
#test_2_SOURCES = main_for_tests.cc


####################
# Additional Rules #
####################

re : clean all

c : clean

a : clean
