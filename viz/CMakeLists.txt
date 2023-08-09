
rock_find_qt4(OPTIONAL Core)
rock_find_qt5(OPTIONAL Core)

if(ROCK_QT_VERSION_4)
    rock_vizkit_plugin(motion_planning_libraries-viz
        MOC
            PluginLoader.cpp
            MotionPlanningLibrariesStateVisualization.cpp
            MotionPlanningLibrariesSbplMprimsVisualization.cpp
            MotionPlanningLibrariesSbplSplineVisualization.cpp
        HEADERS
            MotionPlanningLibrariesStateVisualization.hpp
            MotionPlanningLibrariesSbplMprimsVisualization.hpp
            MotionPlanningLibrariesSbplSplineVisualization.hpp
        DEPS motion_planning_libraries
    )
endif(ROCK_QT_VERSION_4)

if(ROCK_QT_VERSION_5)
    rock_vizkit_plugin_qt5(motion_planning_libraries-viz-qt5
        MOC5
            PluginLoader.cpp
            MotionPlanningLibrariesStateVisualization.cpp
            MotionPlanningLibrariesSbplMprimsVisualization.cpp
            MotionPlanningLibrariesSbplSplineVisualization.cpp
        HEADERS
            MotionPlanningLibrariesStateVisualization.hpp
            MotionPlanningLibrariesSbplMprimsVisualization.hpp
            MotionPlanningLibrariesSbplSplineVisualization.hpp
        DEPS motion_planning_libraries
    )
endif(ROCK_QT_VERSION_5)
