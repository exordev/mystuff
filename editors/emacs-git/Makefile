COMMENT=		GNU editor: extensible, customizable, self-documenting

VERSION=		29.0.50
DISTNAME=		emacs-${VERSION}
PKGNAME=		emacs-git-${VERSION}
REVISION=		0

CATEGORIES=		editors

HOMEPAGE=		https://www.gnu.org/software/emacs/

MAINTAINER=		Jose G Perez Taveras <josegpt27@gmail.com>

# GPLv3+
PERMIT_PACKAGE=		Yes

WANTLIB =		c curses execinfo jansson gmp gnutls m pthread xml2 z \
				ICE SM X11 X11-xcb Xaw3d Xext Xfixes Xinerama Xmu \
				Xpm Xrandr Xrender Xt cairo dbus-1 fontconfig freetype \
				gdk_pixbuf-2.0 gif gio-2.0 glib-2.0 gobject-2.0 harfbuzz \
				jpeg lcms2 otf png rsvg-2 tiff xcb webp webpdemux \
				Xcomposite Xi intl sqlite3 xcb-render xcb-shape xcb-util

GH_ACCOUNT =	emacs-mirror
GH_PROJECT =	emacs
GH_COMMIT =	3939a72fcb5230e86cbe2fb9bcfe00be1dc7bfe0

DEBUG_PACKAGES =	${BUILD_PACKAGES}

GCCARCH=		${MACHINE_ARCH}-unknown-openbsd

CONFIGURE_STYLE=	gnu
MODGNU_CONFIG_GUESS_DIRS=${WRKSRC}/build-aux
CONFIGURE_ARGS=	--build="${GCCARCH}" \
					--without-sound \
					--without-compress-install \
					--with-x-toolkit=athena

CONFIGURE_ENV=		CPPFLAGS="-I${LOCALBASE}/include" \
			LDFLAGS="-L${LOCALBASE}/lib ${LDFLAGS}"

MAKE_ENV=		INSTALL_EMACS="${INSTALL_SCRIPT}" \
			LOGNAME="${SHAREOWN}"

SUBST_VARS=		GCCARCH VERSION

USE_GMAKE=		Yes
BUILD_DEPENDS =	print/texinfo
LIB_DEPENDS=	devel/jansson \
			devel/gmp \
			security/gnutls \
			textproc/libxml \
			devel/harfbuzz \
			devel/libotf \
			graphics/jpeg \
			graphics/png \
			graphics/tiff \
			graphics/giflib \
			graphics/lcms2 \
			graphics/libwebp \
			x11/dbus \
			x11/gnome/librsvg \
			x11/Xaw3d

post-install:
	chmod -t ${PREFIX}/bin/emacs-${VERSION}
	rm -rf ${PREFIX}/lib/systemd
	rm -rf ${PREFIX}/share/{icons,applications}

.include <bsd.port.mk>
