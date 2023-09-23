COMMENT = 		static files for all my services.

V =			1.3.0
DISTNAME =		static-${V}
REVISION =		0

CATEGORIES =		www

HOMEPAGE =		https://git.sr.ht/~josegpt/static

MAINTAINER =		Jose G Perez Taveras <josegpt27@gmail.com>

# GPL-3.0-or-later
PERMIT_PACKAGE =	Yes
MASTER_SITES =		https://git.sr.ht/~josegpt/
DISTFILES =		static-{static/archive/v}${V}${EXTRACT_SUFX}

NO_BUILD =		Yes
NO_TEST =		Yes

WRKSRC =		${WRKDIR}/static-v${V}

do-install:
	${INSTALL_DATA_DIR} ${PREFIX}/share/static/{img,css}
	${INSTALL_DATA} ${WRKSRC}/*.html ${PREFIX}/share/static
	${INSTALL_DATA} ${WRKSRC}/css/*.css ${PREFIX}/share/static/css
	${INSTALL_DATA} ${WRKSRC}/img/*.{png,ico} ${PREFIX}/share/static/img

.include <bsd.port.mk>
