message("-------------------------------")
message("Building Programs")

file(GLOB directs "./*")
foreach(direct ${directs})
    get_filename_component(bext ${direct} EXT)
    if (${bext} MATCHES "txt")
    else()
        get_filename_component(bdirect ${direct} NAME_WE)
        add_subdirectory(${PROJECT_SOURCE_DIR}/programs/${bdirect})
    endif()
endforeach()

