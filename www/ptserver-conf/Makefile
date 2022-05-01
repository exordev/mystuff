COMMENT =			PTServer configuration

V =				0.0.1
DISTNAME =			v${V}
PKGNAME =			ptserver-conf-${V}
REVISION =			0

CATEGORIES =		www

HOMEPAGE =			https://josegpt.com

MAINTAINER =		Jose G Perez Taveras <josegpt27@gmail.com>

# 0BSD
PERMIT_PACKAGE =	Yes

MASTER_SITES =		https://git.sr.ht/~josegpt/ptserver-conf/archive/

NO_BUILD =			Yes
NO_TEST =			Yes

WRKSRC =			${WRKDIR}/ptserver-conf-v${V}

do-install:
	${INSTALL_DATA_DIR} ${PREFIX}/share/examples/ptserver-conf
	${INSTALL_DATA}	${WRKSRC}/{httpd,relayd,acme-client}.conf ${PREFIX}/share/examples/ptserver-conf/

.include <bsd.port.mk>
