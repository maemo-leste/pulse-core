AC_INIT([pulse-core], [0.0.1], [merlijn@wizzup.org])
#AC_INIT([pulse-core], [m4_esyscmd(./git-version-gen .tarball-version)], [merlijn@wizzup.org])

AM_INIT_AUTOMAKE

AC_CONFIG_MACRO_DIR([m4])



PKG_CHECK_MODULES([PULSEAUDIO], [libpulse > 2.1])
PKG_CHECK_MODULES([PULSEAUDIO], [libpulse > 2.1])


m4_define(pa_majorminor, `pkg-config libpulse --modversion`)
AC_SUBST(PA_MAJORMINOR, pa_majorminor)

AC_SUBST(pulseconfdir, ["${sysconfdir}/pulse"])

# Hacks, XXX FIXME TODO
AC_SUBST(PA_DEFAULT_CONFIG_DIR, ["${sysconfdir}/pulse"])

AX_PTHREAD()
#AC_SUBST(PTHREAD_LIBS, [""])

AC_CONFIG_FILES([
Makefile
pulsecore.pc
])

AC_OUTPUT
