# Created by: Anton Berezin <tobez@FreeBSD.org>
# $FreeBSD$

PORTNAME=	IPC-Run
PORTVERSION=	0.98
CATEGORIES=	devel perl5
MASTER_SITES=	CPAN
PKGNAMEPREFIX=	p5-

MAINTAINER=	perl@FreeBSD.org
COMMENT=	IPC::Run - Run subprocesses with piping and redirection

LICENSE=	ART10 GPLv1+
LICENSE_COMB=	dual
LICENSE_FILE_ART10=	${WRKSRC}/LICENSE

BUILD_DEPENDS=	p5-IO-Tty>=1.08:devel/p5-IO-Tty
RUN_DEPENDS:=	${BUILD_DEPENDS}
TEST_DEPENDS=	p5-Readonly>=0:devel/p5-Readonly

NO_ARCH=	yes
USES=		perl5
USE_PERL5=	configure

.include <bsd.port.mk>
