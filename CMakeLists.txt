#
# Copyright (c) 2018 [n/a] info@embeddora.com All rights reserved
#
# Redistribution and use in source and binary forms, with or without
# modification, are permitted provided that the following conditions are met:
#        * Redistributions of source code must retain the above copyright
#          notice, this list of conditions and the following disclaimer.
#        * Redistributions in binary form must reproduce the above copyright
#          notice, this list of conditions and the following disclaimer in the
#          documentation and/or other materials provided with the distribution.
#        * Neither the name of The Linux Foundation nor
#          the names of its contributors may be used to endorse or promote
#          products derived from this software without specific prior written
#          permission.
#
# THIS SOFTWARE IS PROVIDED BY THE COPYRIGHT HOLDERS AND CONTRIBUTORS "AS IS"
# AND ANY EXPRESS OR IMPLIED WARRANTIES, INCLUDING, BUT NOT LIMITED TO, THE
# IMPLIED WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND
# NON-INFRINGEMENT ARE DISCLAIMED.    IN NO EVENT SHALL THE COPYRIGHT OWNER OR
# CONTRIBUTORS BE LIABLE FOR ANY DIRECT, INDIRECT, INCIDENTAL, SPECIAL,
# EXEMPLARY, OR CONSEQUENTIAL DAMAGES (INCLUDING, BUT NOT LIMITED TO,
# PROCUREMENT OF SUBSTITUTE GOODS OR SERVICES; LOSS OF USE, DATA, OR PROFITS;
# OR BUSINESS INTERRUPTION) HOWEVER CAUSED AND ON ANY THEORY OF LIABILITY,
# WHETHER IN CONTRACT, STRICT LIABILITY, OR TORT (INCLUDING NEGLIGENCE OR
# OTHERWISE) ARISING IN ANY WAY OUT OF THE USE OF THIS SOFTWARE, EVEN IF
# ADVISED OF THE POSSIBILITY OF SUCH DAMAGE.
#


cmake_minimum_required(VERSION 2.6)

PROJECT(hwapp)

FIND_PACKAGE(osg)
FIND_PACKAGE(osgViewer)
FIND_PACKAGE(osgDB)
FIND_PACKAGE(osgFX)
FIND_PACKAGE(osgGA)
FIND_PACKAGE(osgParticle)
FIND_PACKAGE(osgSim)
FIND_PACKAGE(osgText)
FIND_PACKAGE(osgUtil)
FIND_PACKAGE(osgTerrain)
FIND_PACKAGE(osgManipulator)
FIND_PACKAGE(osgViewer)
FIND_PACKAGE(osgWidget)
FIND_PACKAGE(osgShadow)
FIND_PACKAGE(osgAnimation)
FIND_PACKAGE(osgVolume)
FIND_PACKAGE(OpenThreads)


SET(SOURCES
osgoccluder.cpp
#osgcamera.cpp
)

INCLUDE_DIRECTORIES(${OPENTHREADS_INCLUDE_DIR} ${OSG_INCLUDE_DIR})

LINK_DIRECTORIES(${OSG_LIB_DIR})

ADD_EXECUTABLE(hwapp ${SOURCES})

TARGET_LINK_LIBRARIES(hwapp ${OSG_LIBRARY} ${OSGUTIL_LIBRARY}   ${OSGGA_LIBRARY}
${OSGDB_LIBRARY} ${OSGVIEWER_LIBRARY} ${OPENTHREADS_LIBRARY})


