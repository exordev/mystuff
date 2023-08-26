COMMENT = 		configuration for my alphabet.

V =			0.0.32
DISTNAME =		alphabet-${V}
REVISION =		0

CATEGORIES =		www

HOMEPAGE =		https://git.sr.ht/~josegpt/alphabet

MAINTAINER =		Jose G Perez Taveras <josegpt27@gmail.com>

# ISC
PERMIT_PACKAGE =	Yes
MASTER_SITES =		https://git.sr.ht/~josegpt/
DISTFILES =		alphabet-{alphabet/archive/v}${V}${EXTRACT_SUFX}

NO_BUILD =		Yes
NO_TEST =		Yes

WRKSRC =		${WRKDIR}/alphabet-v${V}

do-install:
	${INSTALL_DATA_DIR} ${PREFIX}/share/examples/alphabet
	${INSTALL_DATA}	${WRKSRC}/{httpd,relayd,acme-client}.conf ${PREFIX}/share/examples/alphabet

.include <bsd.port.mk>
