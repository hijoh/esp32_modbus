# set(COMPONENT_SRCS "main.c" “modbus.c”)
# set(COMPONENT_ADD_INCLUDEDIRS "")

# add_library(main main.c)
# add_library(main main.c modbus.c)
# register_component()

file(GLOB_RECURSE SOURCES_C *.c components/*.c fonts/*.c screens/*.c  esp_now/*.c)
file(GLOB_RECURSE SOURCES_CPP *.cpp)

idf_component_register(SRCS ${SOURCES_C} ${SOURCES_CPP} 
                            "main.c"
                            "modbus.c"
                    INCLUDE_DIRS "." )
