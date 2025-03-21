cmake_minimum_required(VERSION 3.23)

project(advection_miniapp LANGUAGES CXX VERSION 0.1)

# Setting this to OLD, since deal.ii seems to mess with this policy
cmake_policy(SET CMP0074 OLD)

find_package(pdexa REQUIRED)

add_executable(advection_solver_implicit advection_solver_implicit.cc)
target_link_libraries(advection_solver_implicit PUBLIC pdexa::ext)
