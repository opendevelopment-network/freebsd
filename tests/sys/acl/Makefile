# $FreeBSD$

TESTSDIR=	${TESTSBASE}/sys/acl

BINDIR=		${TESTSDIR}

FILES+=		tools-crossfs.test
FILES+=		tools-nfs4.test
FILES+=		tools-nfs4-psarc.test
FILES+=		tools-nfs4-trivial.test
FILES+=		tools-posix.test

SCRIPTS+=	run

TAP_TESTS_SH+=	00
TAP_TESTS_SH+=	01
TAP_TESTS_SH+=	02
TAP_TESTS_SH+=	03
TAP_TESTS_SH+=	04

.for t in ${TAP_TESTS_SH}
TEST_METADATA.$t+=	required_user="root"
.endfor

.for t in 01 03 04
TEST_METADATA.$t+=	required_programs="/sbin/zpool"
.endfor

.include <bsd.test.mk>
