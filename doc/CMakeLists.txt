ADD_CUSTOM_TARGET(rklogger_man ALL)
ADD_CUSTOM_COMMAND(TARGET rklogger_man
  COMMAND mkdir -p ${CMAKE_BINARY_DIR}/doc/man
  COMMAND gzip -c ${CMAKE_SOURCE_DIR}/doc/man/rklogger.1 > ${CMAKE_BINARY_DIR}/doc/man/rklogger.1.gz
  DEPENDS ${CMAKE_SOURCE_DIR}/doc/man/rklogger.1)

#SET(manpages rklogger.1)
#FOREACH(manpage ${manpages})
#    ADD_CUSTOM_COMMAND(TARGET man
#       OUTPUT ${manpage}.gz
#       COMMAND gzip ${manpage}
#       SOURCE ${manpage}
#       DEPENDS ${manpage})
#ENDFOREACH(manpage)
