# $FreeBSD$

_VALID_XEKMODS=battleimage lunarlake

XEKMODS?=	${_VALID_XEKMODS}

.for var in ${XEKMODS}
.if empty(_VALID_XEKMODS:M${var})
_INVALID_XE_KMODS+=	${var}
.endif
.endfor
.if !empty(_INVALID_XE_KMODS)
.error "${_INVALID_XE_KMODS} firmware doesn't exists"
.endif

.if ${XEKMODS:Mbattleimage}
SUBDIR+=	bmgguc_70 \
		bmg_huc
.endif

.if ${XEKMODS:Mlunarlake}
SUBDIR+=	lnlgsc_1 \
		lnlguc_70 \
		lnl_huc
.endif

SUBDIR_PARALLEL=

.include <bsd.subdir.mk>
