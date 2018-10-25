# Copyright 2018 Mike Dev
# Distributed under the Boost Software License, Version 1.0.
# See accompanying file LICENSE_1_0.txt or copy at http://www.boost.org/LICENSE_1_0.txt

cmake_minimum_required(VERSION 3.5)
project(boost-asio LANGUAGES CXX)

add_library(boost_asio INTERFACE)
add_library(Boost::asio ALIAS boost_asio)

target_include_directories(boost_asio INTERFACE include)

target_link_libraries(boost_asio
    INTERFACE
        Boost::array
        Boost::assert
        Boost::bind
        Boost::chrono
        Boost::config
        Boost::core
        Boost::coroutine
        Boost::date_time
        Boost::function
        Boost::regex
        Boost::smart_ptr
        Boost::system
        Boost::throw_exception
        Boost::type_traits
        Boost::utility
)
