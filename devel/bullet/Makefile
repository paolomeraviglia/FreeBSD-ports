# Created by: Jose Alonso Cardenas Marquez <acm@FreeBSD.org>
# $FreeBSD$

PORTNAME=	bullet
PORTVERSION=	2.86.1
PORTREVISION=	3
CATEGORIES=	devel

MAINTAINER=	acm@FreeBSD.org
COMMENT=	3D collision detection and rigid body dynamics library

LICENSE=	ZLIB
LICENSE_FILE=	${WRKSRC}/LICENSE.txt

USE_GITHUB=	yes
GH_ACCOUNT=	bulletphysics
GH_PROJECT=	bullet3

USES=		cmake compiler:c++11-lang
USE_GL=		gl glu glut
USE_LDCONFIG=	yes
USE_XORG=	x11

CMAKE_ARGS=	-DBUILD_SHARED_LIBS:BOOL=ON \
		-DINSTALL_LIBS:BOOL=ON \
		-DINSTALL_EXTRA_LIBS:BOOL=ON \
		-DBUILD_BULLET2_DEMOS:BOOL=OFF \
		-DBUILD_BULLET3_DEMOS:BOOL=OFF \
		-DBUILD_UNIT_TESTS:BOOL=OFF

PORTDOCS=	*

OPTIONS_DEFINE=	DOCS

post-install-DOCS-on:
	@${MKDIR} ${STAGEDIR}/${DOCSDIR}
	${INSTALL_DATA} ${WRKSRC}/docs/*.pdf ${STAGEDIR}/${DOCSDIR}

.include <bsd.port.mk>
