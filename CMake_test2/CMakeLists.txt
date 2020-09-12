cmake_minimum_required (VERSION 2.8)
project (test)	
include_directories(./ ./menu ./student)	#添加頭文件
aux_source_directory(. ALL_SRCS)		# 添加当前目录下所有的源文件
add_subdirectory(menu)				#添加子目錄
add_subdirectory(student)			
add_executable(test ${ALL_SRCS})	        # 指定生成目标
target_link_libraries(test menu student)	# 添加链接库

