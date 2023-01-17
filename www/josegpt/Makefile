COMMENT =		My personal website

V =			1.16.2
MODGO_MODNAME =		git.sr.ht/~josegpt/josegpt
MODGO_VERSION =		v${V}

DISTNAME =		josegpt-${V}
REVISION =		0

CATEGORIES =		www

HOMEPAGE =		https://josegpt.com

MAINTAINER =		Jose G Perez Taveras <josegpt27@gmail.com>

# ISC
PERMIT_PACKAGE =	Yes

# uses pledge()
WANTLIB =		c pthread

MODULES =		lang/go

MODGO_MODULES =		git.sr.ht/~josegpt/core-go		v0.23.0 \
			github.com/!burnt!sushi/toml		v1.2.1 \
			golang.org/x/sys			v0.4.0 \
			google.golang.org/grpc			v1.52.0 \
			google.golang.org/protobuf		v1.28.1 \
			github.com/golang/protobuf		v1.5.2 \
			golang.org/x/net			v0.5.0 \
			golang.org/x/text			v0.6.0 \
			google.golang.org/genproto		v0.0.0-20230113154510-dbe35b8444a5

post-install:
	${INSTALL_DATA_DIR} ${PREFIX}/share/josegpt
	${INSTALL_DATA} ${WRKSRC}/josegpt.toml ${PREFIX}/share/josegpt
	cp -Rp ${WRKSRC}/http/static ${PREFIX}/share/josegpt

.include <bsd.port.mk>
