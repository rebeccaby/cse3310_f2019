# cse3310 project sample makefile



CXX=g++
# note the below asio package may be in a 
# different place
CPPFLAGS=-I../asio-1.13.0/include
CXXFLAGS=-Wall -g -std=c++11 

TARGETS=chat_client chat_server

all:${TARGETS}


# these compile and link in the same command.
# no intermediate object code files

chat_client: chat_client.cpp chat_message.hpp
	${CXX} ${CXXFLAGS} ${CPPFLAGS} -o $@ $< -lpthread -lncurses

chat_server: chat_server.cpp chat_message.hpp
	${CXX} ${CXXFLAGS} ${CPPFLAGS} -o $@ $< -lpthread

clean:
	-rm -f ${TARGETS}
