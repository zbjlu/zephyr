# SPDX-License-Identifier: Apache-2.0

zephyr_library()

zephyr_library_sources_ifdef(CONFIG_IPM_MCUX   ipm_mcux.c)
zephyr_library_sources_ifdef(CONFIG_IPM_IMX ipm_imx.c)
zephyr_library_sources_ifdef(CONFIG_IPM_QUARK_SE ipm_quark_se.c)

zephyr_library_sources_ifdef(CONFIG_USERSPACE   ipm_handlers.c)
