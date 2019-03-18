cmake_minimum_required( VERSION 3.0 )

option( PLUGIN_IO_CORE "Check to install the CoreIO plugin" ON )

if ( PLUGIN_IO_CORE )
	project( qCoreIO )

	set( CC_IS_IO_PLUGIN 1 )
	
	include_directories( src )

	add_subdirectory( src )
	add_subdirectory( ui )
	
	include( ../../../CMakePluginTpl.cmake )
endif()
