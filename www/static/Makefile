COMMENT = 		static files for all my services.

V =			1.5.1
DISTNAME =		static-${V}
REVISION =		0

CATEGORIES =		www

HOMEPAGE =		https://git.sr.ht/~josegpt/static

MAINTAINER =		Jose G Perez Taveras <josegpt27@gmail.com>

# GPL-3.0-or-later
PERMIT_PACKAGE =	Yes
MASTER_SITES =		https://git.sr.ht/~josegpt/
DISTFILES =		static-{static/archive/v}${V}${EXTRACT_SUFX}

PREFIX =		${VARBASE}/www
FAKE_FLAGS =		DESTDIR=""

NO_BUILD = 		Yes
NO_TEST =		Yes

WRKSRC =		${WRKDIR}/static-v${V}

.include <bsd.port.mk>
