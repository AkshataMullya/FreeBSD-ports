# Created by: mi@aldan.algebra.com
# $FreeBSD$

PORTNAME=	incron
DISTVERSION=	2017-11-13
PORTREVISION=	1
CATEGORIES=	sysutils

MAINTAINER=	joh.hendriks@gmail.com
COMMENT=	Handle filesystem-events the way cron handles time ones

LICENSE=	GPLv2 LGPL21 MIT
LICENSE_COMB=	dual
LICENSE_FILE_GPLv2=	${WRKSRC}/LICENSE-GPL
LICENSE_FILE_LGPL21=	${WRKSRC}/LICENSE-LGPL
LICENSE_FILE_MIT=	${WRKSRC}/LICENSE-X11

LIB_DEPENDS=	libinotify.so:devel/libinotify

USE_GITHUB=	indeed
GH_ACCOUNT=	ar-
GH_TAGNAME=	81421d3a8bde0989d7e167d8a814d5232896c930
CPPFLAGS+=	-I${LOCALBASE}/include -D__NR_inotify_init
LDFLAGS+=	-L${LOCALBASE}/lib -linotify
MAKE_ARGS=	PREFIX="${PREFIX}" USER=${UID}	\
		DOCDIR="${PREFIX}/etc"	\
		MANPATH=${MANPREFIX}/man
USE_RC_SUBR=	${PORTNAME}

post-patch:
	${REINPLACE_CMD} -e 's,/etc/incron,${PREFIX}/etc/incron,'	\
		${WRKSRC}/*conf* ${WRKSRC}/Makefile ${WRKSRC}/*.[158h]	\
		${WRKSRC}/*.cpp
	${REINPLACE_CMD} -e '/INITDIR/d' ${WRKSRC}/Makefile

.include <bsd.port.mk>
