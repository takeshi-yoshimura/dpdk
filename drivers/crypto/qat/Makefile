# SPDX-License-Identifier: BSD-3-Clause
# Copyright(c) 2015-2018 Intel Corporation

include $(RTE_SDK)/mk/rte.vars.mk

# library name
LIB = librte_pmd_qat.a

# library version
LIBABIVER := 1

# build flags
CFLAGS += $(WERROR_FLAGS)
CFLAGS += -O3

# external library include paths
CFLAGS += -I$(SRCDIR)/qat_adf
LDLIBS += -lcrypto
LDLIBS += -lrte_eal -lrte_mbuf -lrte_mempool -lrte_ring
LDLIBS += -lrte_cryptodev
LDLIBS += -lrte_pci -lrte_bus_pci

# library source files
SRCS-$(CONFIG_RTE_LIBRTE_PMD_QAT) += qat_sym.c
SRCS-$(CONFIG_RTE_LIBRTE_PMD_QAT) += qat_device.c
SRCS-$(CONFIG_RTE_LIBRTE_PMD_QAT) += qat_qp.c
SRCS-$(CONFIG_RTE_LIBRTE_PMD_QAT) += qat_sym_session.c
SRCS-$(CONFIG_RTE_LIBRTE_PMD_QAT) += qat_common.c
SRCS-$(CONFIG_RTE_LIBRTE_PMD_QAT) += qat_logs.c
SRCS-$(CONFIG_RTE_LIBRTE_PMD_QAT) += qat_sym_pmd.c
SRCS-$(CONFIG_RTE_LIBRTE_PMD_QAT) += qat_asym_pmd.c
SRCS-$(CONFIG_RTE_LIBRTE_PMD_QAT) += qat_comp_pmd.c

# export include files
SYMLINK-y-include +=

# versioning export map
EXPORT_MAP := rte_pmd_qat_version.map

include $(RTE_SDK)/mk/rte.lib.mk
