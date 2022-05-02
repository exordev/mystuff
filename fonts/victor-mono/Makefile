COMMENT =		a free programming font with cursive italics and ligature
V =			1.5.2
DISTNAME =		VictorMonoAll
PKGNAME =		victor-mono-${V}

CATEGORIES =	fonts

HOMEPAGE =	https://rubjo.github.io/victor-mono

MAINTAINER =	Jose G Perez Taveras <josegpt27@gmail.com>

# OFL-1.1
PERMIT_PACKAGE = Yes

MASTER_SITES =	https://github.com/rubjo/victor-mono/raw/v${V}/public/

EXTRACT_SUFX =	.zip

PKG_ARCH =	*

FONTDIR =	${PREFIX}/share/fonts/victor-mono

NO_BUILD = YES
NO_TEST = YES

do-install:
	${INSTALL_DATA_DIR} ${FONTDIR}
	${INSTALL_DATA} ${WRKDIR}/TTF/*.ttf ${FONTDIR}
	${INSTALL_DATA_DIR} ${PREFIX}/share/doc/victor-mono
	${INSTALL_DATA} ${WRKDIR}/LICENSE.txt ${PREFIX}/share/doc/victor-mono

.include <bsd.port.mk>
