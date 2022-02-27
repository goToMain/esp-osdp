
list(APPEND LIBOSDP_SOURCES
	libosdp/src/osdp_common.c
	libosdp/src/osdp_phy.c
	libosdp/src/osdp_pd.c
	libosdp/src/osdp_sc.c
	libosdp/src/osdp_cp.c
	libosdp/src/osdp_pd.c
	libosdp/utils/src/disjoint_set.c
	libosdp/utils/src/logger.c
	libosdp/utils/src/list.c
	libosdp/utils/src/queue.c
	libosdp/utils/src/slab.c
	libosdp/utils/src/utils.c
)

list(APPEND LIBOSDP_INCLUDES
	"."
	libosdp/include
	libosdp/utils/include
)

idf_component_register(SRCS ${LIBOSDP_SOURCES}
	INCLUDE_DIRS ${LIBOSDP_INCLUDES})
