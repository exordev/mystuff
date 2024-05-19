COMMENT=	ultralightweight JSON parser in ANSI C

GH_ACCOUNT=	DaveGamble
GH_PROJECT=	cJSON
GH_TAGNAME=	v1.7.17

PKGNAME=	${DISTNAME:L}

SHARED_LIBS+=	cjson	0.0	# 0.0

CATEGORIES=	devel

# MIT
PERMIT_PACKAGE=	Yes

COMPILER=	base-clang ports-gcc
COMPILER_LANGS= c

WANTLIB+=	m

MODULES=	devel/cmake

CONFIGURE_ARGS=	-DENABLE_CJSON_UTIRLS=On \
		-DENABLE_CJSON_TEST=Off \
		-DBUILD_SHARED_AND_STATIC_LIBS=On

# build whatever is left (ca. 43 C test files)
pre-test:
	@${MODCMAKE_BUILD_TARGET}

.include <bsd.port.mk>
