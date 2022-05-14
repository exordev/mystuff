COMMENT =	sorthing.com account service

V =				0.1.0
MODGO_MODNAME =	git.sr.ht/~josegpt/srth-account
MODGO_VERSION =	v${V}

DISTNAME =	srth-account-${MODGO_VERSION}
REVISION =	0

CATEGORIES =	grpc

HOMEPAGE =	https://sr.ht/~josegpt/sorthing.com/

MAINTAINER =		Jose G Perez Taveras <josegpt27@gmail.com>

# GPLv3
PERMIT_PACKAGE =	Yes

WANTLIB =		c pthread

MODULES =		lang/go

MODGO_MODULES =	git.sr.ht/~josegpt/srth-proto	v0.2.0 \
					git.sr.ht/~josegpt/web-core	v0.17.0 \
					github.com/adlio/schema		v1.3.0 \
					github.com/go-sql-driver/mysql	v1.6.0 \
					google.golang.org/grpc			v1.46.0 \
					github.com/99designs/gqlgen	v0.17.5 \
					golang.org/x/crypto v0.0.0-20210921155107-089bfa567519 \
					github.com/golang/protobuf		v1.5.2 \
					github.com/vektah/gqlparser/v2	v2.4.2 \
					golang.org/x/net				v0.0.0-20211208012354-db4efeb81f4b \
					golang.org/x/sys				v0.0.0-20211216021012-1d35b9e2eb4e \
					golang.org/x/text				v0.3.7 \
					google.golang.org/genproto		v0.0.0-20200526211855-cb27e3aa2013 \
					google.golang.org/protobuf		v1.28.0 \
					gopkg.in/yaml.v3				v3.0.0-20210107192922-496545a6307b

RUN_DEPENDS =		databases/mariadb,-server

.include <bsd.port.mk>
