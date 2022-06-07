COMMENT =			My personal website

V =				1.3.0
MODGO_MODNAME =	git.sr.ht/~josegpt/josegptcom
MODGO_VERSION =	v${V}

DISTNAME =			josegptcom-${V}
REVISION =			0

CATEGORIES =		www

HOMEPAGE =			https://josegpt.com

MAINTAINER =		Jose G Perez Taveras <josegpt27@gmail.com>

# MIT
PERMIT_PACKAGE =	Yes

# uses pledge()
WANTLIB =			c pthread

MODULES =			lang/go

MODGO_MODULES =	git.sr.ht/~josegpt/go-utils			v0.18.1 \
					github.com/bradleyjkemp/cupaloy/v2		v2.7.0 \
					github.com/stretchr/testify			v1.7.1 \
					golang.org/x/sys						v0.0.0-20220520151302-bc2c85ada10a

post-install:
	${INSTALL_DATA_DIR} ${PREFIX}/share/josegptcom/static/{img,css}
	${INSTALL_DATA} ${WRKSRC}/static/css/*.css ${PREFIX}/share/josegptcom/static/css
	${INSTALL_DATA} ${WRKSRC}/static/img/*.{svg,png,ico} ${PREFIX}/share/josegptcom/static/img

.include <bsd.port.mk>
