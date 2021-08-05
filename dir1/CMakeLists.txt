
cmake_minimum_required (VERSION 3.20)

function (child_fn msg_)
    message (STATUS "${CMAKE_CURRENT_FUNCTION_LIST_DIR}: ${CMAKE_CURRENT_FUNCTION}: ${msg_}")
endfunction ()

function (call1 msg_)
    child_fn (${msg_})
endfunction ()
