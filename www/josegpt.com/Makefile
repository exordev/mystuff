COMMENT =		my personal site.

V =			1.21.6
MODGO_MODNAME =		git.sr.ht/~josegpt/josegpt.com
MODGO_VERSION =		v${V}
DISTNAME =		josegpt.com-${V}
REVISION =		0

CATEGORIES =		www
HOMEPAGE =		https://josegpt.com
MAINTAINER =		Jose G Perez Taveras <josegpt27@gmail.com>

# AGPL-3.0-or-later
PERMIT_PACKAGE =	Yes

# uses pledge()
WANTLIB =		c pthread

MODULES =		lang/go
MODGO_MODULES =		git.sr.ht/~josegpt/sanitize		v1.0.1		\
			git.sr.ht/~josegpt/template		v1.0.1		\
			github.com/google/uuid			v1.3.0		\
			github.com/mattn/go-sqlite3		v1.14.17	\
			golang.org/x/sync			v0.3.0

.include <bsd.port.mk>
