COMMENT= 		my personal website.

GH_PROJECT=		josegpt
GH_ACCOUNT=		josegpt
GH_TAGNAME=		0.10
REVISION=		0

CATEGORIES=		www
HOMEPAGE=		https://josegpt.com
MAINTAINER=		Jose G Perez Taveras <josegpt27@gmail.com>

# ISC
PERMIT_PACKAGE=		Yes

# uses pledge()
BUILD_DEPENDS=		devel/json-c

NO_TEST=		Yes
PREFIX=			${VARBASE}/www
MAKE_ENV=		VERSION=${GH_TAGNAME}

.include <bsd.port.mk>
