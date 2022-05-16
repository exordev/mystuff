COMMENT =			My personal website

V =				1.2.3
MODGO_MODNAME =	git.sr.ht/~josegpt/josegpt.com
MODGO_VERSION =	v${V}

DISTNAME =			josegpt.com-${V}
REVISION =			0

CATEGORIES =		www

HOMEPAGE =			https://josegpt.com

MAINTAINER =		Jose G Perez Taveras <josegpt27@gmail.com>

# MIT
PERMIT_PACKAGE =	Yes

# uses pledge()
WANTLIB =			c pthread

MODULES =			lang/go

MODGO_MODULES =	git.sr.ht/~josegpt/web-core			v0.10.0 \
					github.com/bradleyjkemp/cupaloy/v2		v2.7.0 \
					github.com/stretchr/testify			v1.7.1 \
					golang.org/x/sys						v0.0.0-20220429233432-b5fbb4746d32

post-install:
	${INSTALL_DATA_DIR} ${PREFIX}/share/josegpt.com/static/{img,css}
	${INSTALL_DATA} ${WRKSRC}/web/static/css/*.css ${PREFIX}/share/josegpt.com/static/css
	${INSTALL_DATA} ${WRKSRC}/web/static/img/*.{svg,png,ico} ${PREFIX}/share/josegpt.com/static/img

.include <bsd.port.mk>
