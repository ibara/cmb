#	$OpenBSD$

PROG=	cmb

CFLAGS+=-I${.CURDIR} -I${.CURDIR}/../../lib/libcmb
CFLAGS+=-DHAVE_LIBCRYPTO

LDFLAGS+=-L${.CURDIR}/../../lib/libcmb

LDADD+=	-lcrypto -lcmb
DPADD+=	${LIBCRYPTO}

MAN=	cmb.1

BINDIR=	/usr/local/bin
MANDIR=	/usr/local/man/man

.include <bsd.prog.mk>
