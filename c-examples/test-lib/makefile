# c-examples/test-lib/makefile
#
# $Header: /usr/app/odstb/CVS/snacc/c-examples/test-lib/makefile,v 1.4 1995/07/24 20:50:11 rj Exp $
# $Log: makefile,v $
# Revision 1.4  1995/07/24 20:50:11  rj
# changed `_' to `-' in file names.
#
# Revision 1.3  1995/02/13  15:05:59  rj
# augment CPPFLAGS, not overwrite.
#
# Revision 1.2  1994/08/31  21:43:20  rj
# rebuild the executables when the c-lib is newer.
#
# Revision 1.1  1994/08/31  08:46:37  rj
# first check-in. for a list of changes to the snacc-1.1 distribution please refer to the ChangeLog.
#

#include ../../makehead

TOP		= /usr

ASN1_C_LIB_DIR	= $(TOP)/lib
ASN1_C_INC_DIR	= $(TOP)/include/snacc/c
ASN1_C_LIB	= $(ASN1_C_LIB_DIR)/libasn1csbuf.a

CPPFLAGS	+= -g -I$(TOP) -I$(ASN1_C_INC_DIR) -DUSE_SBUF
LIBS		+= -lm

LDLIBS		= $(ASN1_C_LIB) $(LIBS)

CFILES = \
	test-lib.c

DISTFILES = \
	README		\
	makefile	\
	$(CFILES)

#-------------------------------------------------------------------------------

default::	check

check::		test-lib
		./test-lib

test-lib:	$(ASN1_C_LIB)

clean::
		$(RM) *.o *~ .emacs* test-lib core

#include ../../maketail
