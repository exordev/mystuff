COMMENT= 	httpd config.

GH_PROJECT=	httpd.conf
GH_ACCOUNT=	josegpt
GH_TAGNAME=	0.5
REVISION=	0

CATEGORIES=	www
HOMEPAGE=	https://redhex.dev
MAINTAINER=	Jose G Perez Taveras <josegpt27@gmail.com>

# ISC
PERMIT_PACKAGE=	Yes

RUN_DEPENDS=	www/design	\
		www/publicaddr	\
		www/josegpt	\
		www/mtaveras

NO_BUILD=	Yes
NO_TEST=	Yes

PREFIX=		${SYSCONFDIR}

.include <bsd.port.mk>
