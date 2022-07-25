#ifeq ($(CONFIG_ARCH_LAHAINA), y)

include $(srctree)/techpack/oneplus/config/oneplus.conf
LINUXINCLUDE    += -include $(srctree)/techpack/oneplus/config/oneplus.h
LINUXINCLUDE    += \
                   -I$(srctree)/techpack/oneplus/include
USERINCLUDE     += -I$(srctree)/techpack/oneplus/include

ifeq ($(CONFIG_QGKI),y)
include $(srctree)/techpack/oneplus/config/coretech.conf
LINUXINCLUDE    += -include $(srctree)/techpack/oneplus/config/coretech.h
endif

obj-y += input/
obj-y += misc/
ifeq ($(CONFIG_QGKI),y)
obj-y += coretech/
endif
obj-y += fs/
obj-y += kernel/
obj-y += oneplus_healthinfo/
obj-y += mm/
obj-y += opslalib/
ifeq ($(CONFIG_DETECT_HUNG_TASK), y)
obj-$(CONFIG_HUNG_TASK_ENHANCE) += hung_task_enhance/
endif
#endif
ifeq ($(CONFIG_ARCH_HOLI), y)
#ifdef CONFIG_OPLUS_FEATURE_QCOM_PMICWD
obj-$(CONFIG_OPLUS_FEATURE_QCOM_PMICWD) += qcom_pmicwd/
#endif
endif

ifeq ($(CONFIG_ARCH_HOLI), y)
##include $(srctree)/techpack/oneplus/config/oneplus.conf
#LINUXINCLUDE    += -include $(srctree)/techpack/oneplus/config/oneplus.h
#LINUXINCLUDE    += \
#                   -I$(srctree)/techpack/oneplus/include
#USERINCLUDE     += -I$(srctree)/techpack/oneplus/include

##ifeq ($(CONFIG_QGKI),y)
##include $(srctree)/techpack/oneplus/config/coretech.conf
##LINUXINCLUDE    += -include $(srctree)/techpack/oneplus/config/coretech.h
##endif

#obj-y += input/
#obj-y += misc/project_info.o
#obj-y += misc/op_cmdline.o
#obj-y += input/
endif
$(warning "techpack USERINCLUDE  " $(USERINCLUDE))
$(warning "techpack LINUXINCLUDE " $(LINUXINCLUDE))
