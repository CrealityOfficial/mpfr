if(CC_INSTALL_MPFR)
	__install_directory_specif(${CMAKE_CURRENT_SOURCE_DIR}/include/ mpfr)
	
	set(LIBS)
	set(DLLS)
	
	if(CC_BC_WIN)
		set(LIBS ${CMAKE_CURRENT_SOURCE_DIR}/lib/libmpfr-4.lib
				)
		set(DLLS ${CMAKE_CURRENT_SOURCE_DIR}/lib/libmpfr-4.dll
				)
	elseif(CC_BC_LINUX)
	else()
	endif()
	
	INSTALL(FILES ${LIBS} DESTINATION lib)
	INSTALL(FILES ${DLLS} DESTINATION bin)
endif()