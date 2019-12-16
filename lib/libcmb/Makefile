#	$OpenBSD$

LIB=	cmb

SHLIB_MAJOR=	0
SHLIB_MINOR=	0

CFLAGS+=-I${.CURDIR}
CFLAGS+=-DHAVE_LIBCRYPTO

LDADD+=	-lcrypto -lm
DPADD+=	${LIBCRYPTO} ${LIBM}

HDRS=	cmb.h
SRCS=	cmb.c

MAN=	cmb.3

LIBDIR=	/usr/local/lib
MANDIR=	/usr/local/man/man

includes:
	@cd ${.CURDIR}; for i in $(HDRS); do \
	    j="cmp -s $$i ${PREFIX}/include/$$i || \
		${INSTALL} ${INSTALL_COPY} -o ${BINOWN} -g ${BINGRP} \
		-m 444 $$i ${PREFIX}/include"; \
	    echo $$j; \
	    eval "$$j"; \
	done

.include <bsd.lib.mk>
