add_definitions(-DUIDLL)
add_library(ui SHARED
	ui_atoms.c
	ui_gameinfo.c
	ui_loadpanel.c
	ui_main.c
	ui_players.c
	ui_shared.c
	ui_syscalls.c
	ui_util.c
	../game/bg_campaign.c
	../game/bg_classes.c
	../game/bg_misc.c
	../game/q_math.c
	../game/q_shared.c
)
target_link_libraries(ui m)
set_target_properties(ui PROPERTIES OUTPUT_NAME "ui.mp.${ARCH}" PREFIX "")
