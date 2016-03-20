cmake_minimum_required(VERSION 3.0)

include("cmake/HunterGate.cmake")
HunterGate(
    URL "https://github.com/ruslo/hunter/archive/v0.14.1.tar.gz"
    SHA1 "d073cc04d59a01782385799568afce78066a8cec"
)

project(FreeImage VERSION 3.17.0)
