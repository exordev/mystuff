COMMENT=		dynamic menu for X11

V=				5.1
DISTNAME=		dmenu-${V}
REVISION=		0

CATEGORIES=		x11

HOMEPAGE=		https://tools.suckless.org/dmenu

MAINTAINER=		Jose G Perez Taveras <josegpt27@gmail.com>

# MIT/X
PERMIT_PACKAGE=	Yes

# uses pledge()
WANTLIB=		X11 Xft Xinerama c fontconfig

MASTER_SITES=		https://dl.suckless.org/tools/

RUN_DEPENDS=		fonts/spleen

MAKE_ENV=		LDFLAGS="${LDFLAGS}" \
				X11INC=${X11BASE}/include \
				X11LIB=${X11BASE}/lib

NO_TEST=		Yes

do-install:
	${INSTALL_PROGRAM} ${WRKBUILD}/{dmenu,stest} ${PREFIX}/bin/
	${INSTALL_SCRIPT} ${WRKBUILD}/dmenu_{run,path} ${PREFIX}/bin/
	${INSTALL_MAN} ${WRKSRC}/{dmenu,stest}.1 ${PREFIX}/man/man1/
	sed -i s/VERSION/${V}/g ${PREFIX}/man/man1/{dmenu,stest}.1

.include <bsd.port.mk>
