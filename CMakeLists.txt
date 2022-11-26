cmake_minimum_required(VERSION 3.5)
project(gaia-doc
        VERSION 0.1.0
        LANGUAGES NONE 
       )

execute_process ( COMMAND bash -c "cp -r ${CMAKE_CURRENT_SOURCE_DIR}/user-manual/ ." )
execute_process ( COMMAND bash -c "CMDROOT=`pwd`;cd $CMDROOT/user-manual/EN/; pdflatex -output-directory=$CMDROOT/ en_user_manual.tex" )


