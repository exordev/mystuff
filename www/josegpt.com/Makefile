COMMENT =			My personal website

V =					1.1.6
MODGO_MODNAME =		git.sr.ht/~josegpt/josegpt.com
MODGO_VERSION =		v${V}

DISTNAME =			josegpt.com-${V}
REVISION =			1

CATEGORIES =		www

HOMEPAGE =			https://josegpt.com

MAINTAINER =		Jose G Perez Taveras <josegpt27@gmail.com>

# MIT
PERMIT_PACKAGE =	Yes

WANTLIB =			c pthread

MODULES =			lang/go

MODGO_MODULES =		git.sr.ht/~josegpt/srth-core 		v0.9.0 \
					github.com/bradleyjkemp/cupaloy/v2 	v2.7.0 \
					github.com/stretchr/testify 		v1.7.1

# These are needed for dependency resolution. We don't actually need the
# coresponding code
#MODGO_MODFILES =	modulename version

post-install:
	${INSTALL_DATA_DIR} ${PREFIX}/share/josegpt.com/static/{img,css}
	${INSTALL_DATA} ${WRKSRC}/web/static/css/*.css ${PREFIX}/share/josegpt.com/static/css
	${INSTALL_DATA} ${WRKSRC}/web/static/img/*.{svg,png,ico} ${PREFIX}/share/josegpt.com/static/img

.include <bsd.port.mk>
