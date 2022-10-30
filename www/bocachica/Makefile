COMMENT =			BocaChica server configuration

V =					0.0.6
DISTNAME=			bocachica-${V}
REVISION=			0

CATEGORIES=			www

HOMEPAGE=			https://ptserver.org

MAINTAINER=			Jose G Perez Taveras <josegpt27@gmail.com>

# ISC
PERMIT_PACKAGE=		Yes

MASTER_SITES=		https://git.sr.ht/~josegpt/
DISTFILES=			bocahica-{bocachica/archive/v}${V}${EXTRACT_SUFX}

NO_BUILD=			Yes
NO_TEST=			Yes

WRKSRC =			${WRKDIR}/bocachica-v${V}

do-install:
	${INSTALL_DATA_DIR} ${PREFIX}/share/examples/bocachica
	${INSTALL_DATA}	${WRKSRC}/{httpd,relayd,acme-client,mk}.conf ${PREFIX}/share/examples/bocachica

.include <bsd.port.mk>
