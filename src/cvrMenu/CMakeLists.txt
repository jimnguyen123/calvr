IF(WIN32)
	IF(CALVR_WIN_DYNAMIC)
		ADD_DEFINITIONS(-DCVRMENU_LIBRARY)
	ELSE(CALVR_WIN_DYNAMIC)
		ADD_DEFINITIONS(-DCVRMENU_LIBRARY_STATIC)
	ENDIF(CALVR_WIN_DYNAMIC)
ENDIF(WIN32)

SET(LIB_NAME cvrMenu)
SET(HEADER_PATH ${CalVR_SOURCE_DIR}/include/${LIB_NAME})
SET(LIB_PUBLIC_HEADERS
    ${HEADER_PATH}/MenuItem.h
    ${HEADER_PATH}/MenuCollection.h
    ${HEADER_PATH}/SubMenu.h
    ${HEADER_PATH}/SubMenuClosable.h
    ${HEADER_PATH}/MenuItemGroup.h
    ${HEADER_PATH}/MenuButton.h
    ${HEADER_PATH}/MenuCheckbox.h
    ${HEADER_PATH}/MenuList.h
    ${HEADER_PATH}/MenuRangeValue.h
    ${HEADER_PATH}/MenuRangeValueCompact.h
    ${HEADER_PATH}/MenuText.h
    ${HEADER_PATH}/MenuTextButtonSet.h
    ${HEADER_PATH}/MenuScrollText.h
    ${HEADER_PATH}/MenuImage.h
    ${HEADER_PATH}/MenuBar.h
    ${HEADER_PATH}/MenuFloatEntryItem.h
    ${HEADER_PATH}/MenuIntEntryItem.h
    ${HEADER_PATH}/MenuTextEntryItem.h
    ${HEADER_PATH}/MenuBase.h
    ${HEADER_PATH}/PopupMenuBase.h
    ${HEADER_PATH}/BoardMenu.h
    ${HEADER_PATH}/MenuSystem.h
    ${HEADER_PATH}/MenuManager.h
    ${HEADER_PATH}/PopupMenu.h
    ${HEADER_PATH}/DialogPanel.h
    ${HEADER_PATH}/TabbedDialogPanel.h
    ${HEADER_PATH}/ScrollingDialogPanel.h
    ${HEADER_PATH}/TextInputPanel.h
    ${HEADER_PATH}/BoardPopupMenu.h
    ${HEADER_PATH}/BoardMenu/BoardMenuGeometry.h
    ${HEADER_PATH}/BoardMenu/BoardMenuButtonGeometry.h
    ${HEADER_PATH}/BoardMenu/BoardMenuCheckboxGeometry.h
    ${HEADER_PATH}/BoardMenu/BoardMenuListGeometry.h
    ${HEADER_PATH}/BoardMenu/BoardMenuRangeValueGeometry.h
    ${HEADER_PATH}/BoardMenu/BoardMenuRangeValueCompactGeometry.h
    ${HEADER_PATH}/BoardMenu/BoardMenuTextGeometry.h
    ${HEADER_PATH}/BoardMenu/BoardMenuTextButtonSetGeometry.h
    ${HEADER_PATH}/BoardMenu/BoardMenuScrollTextGeometry.h
    ${HEADER_PATH}/BoardMenu/BoardMenuSubMenuGeometry.h
    ${HEADER_PATH}/BoardMenu/BoardMenuSubMenuClosableGeometry.h
    ${HEADER_PATH}/BoardMenu/BoardMenuItemGroupGeometry.h
    ${HEADER_PATH}/BoardMenu/BoardMenuImageGeometry.h
    ${HEADER_PATH}/BoardMenu/BoardMenuBarGeometry.h
    ${HEADER_PATH}/Export.h
    ${HEADER_PATH}/BubbleMenu.h
    ${HEADER_PATH}/BubbleMenu/BubbleMenuGeometry.h
    ${HEADER_PATH}/BubbleMenu/BubbleMenuGeometry.h
    ${HEADER_PATH}/BubbleMenu/BubbleMenuCheckboxGeometry.h
    ${HEADER_PATH}/BubbleMenu/BubbleMenuListGeometry.h
    ${HEADER_PATH}/BubbleMenu/BubbleMenuRangeValueGeometry.h
    ${HEADER_PATH}/BubbleMenu/BubbleMenuRangeValueCompactGeometry.h
    ${HEADER_PATH}/BubbleMenu/BubbleMenuTextGeometry.h
    ${HEADER_PATH}/BubbleMenu/BubbleMenuTextButtonSetGeometry.h
    ${HEADER_PATH}/BubbleMenu/BubbleMenuSubMenuGeometry.h
    ${HEADER_PATH}/BubbleMenu/BubbleMenuSubMenuClosableGeometry.h
    ${HEADER_PATH}/BubbleMenu/BubbleMenuImageGeometry.h
    ${HEADER_PATH}/BubbleMenu/Lerp.h
)

SET(LIB_SRC_FILES
    MenuItem.cpp
    MenuCollection.cpp
    SubMenu.cpp
    MenuItemGroup.cpp
    MenuButton.cpp
    MenuCheckbox.cpp
    MenuList.cpp
    MenuRangeValue.cpp
    MenuRangeValueCompact.cpp
    MenuText.cpp
    MenuTextButtonSet.cpp
    MenuScrollText.cpp
    MenuImage.cpp
    MenuBar.cpp
    MenuFloatEntryItem.cpp
    MenuIntEntryItem.cpp
    MenuTextEntryItem.cpp
    MenuSystem.cpp
    BoardMenu.cpp
    MenuManager.cpp
    PopupMenu.cpp
    DialogPanel.cpp
    ScrollingDialogPanel.cpp
    TabbedDialogPanel.cpp
    TextInputPanel.cpp
    BoardPopupMenu.cpp
    BoardMenu/BoardMenuGeometry.cpp
    BoardMenu/BoardMenuButtonGeometry.cpp
    BoardMenu/BoardMenuCheckboxGeometry.cpp
    BoardMenu/BoardMenuListGeometry.cpp
    BoardMenu/BoardMenuRangeValueGeometry.cpp
    BoardMenu/BoardMenuRangeValueCompactGeometry.cpp
    BoardMenu/BoardMenuTextGeometry.cpp
    BoardMenu/BoardMenuTextButtonSetGeometry.cpp
    BoardMenu/BoardMenuScrollTextGeometry.cpp
    BoardMenu/BoardMenuImageGeometry.cpp
    BoardMenu/BoardMenuBarGeometry.cpp
    BoardMenu/BoardMenuSubMenuGeometry.cpp
    BoardMenu/BoardMenuSubMenuClosableGeometry.cpp
    BoardMenu/BoardMenuItemGroupGeometry.cpp
    BubbleMenu.cpp
    BubbleMenu/BubbleMenuGeometry.cpp
    BubbleMenu/BubbleMenuButtonGeometry.cpp
    BubbleMenu/BubbleMenuCheckboxGeometry.cpp
    BubbleMenu/BubbleMenuListGeometry.cpp
    BubbleMenu/BubbleMenuRangeValueGeometry.cpp
    BubbleMenu/BubbleMenuRangeValueCompactGeometry.cpp
    BubbleMenu/BubbleMenuTextGeometry.cpp
    BubbleMenu/BubbleMenuTextButtonSetGeometry.cpp
    BubbleMenu/BubbleMenuImageGeometry.cpp
    BubbleMenu/BubbleMenuSubMenuGeometry.cpp
    BubbleMenu/BubbleMenuSubMenuClosableGeometry.cpp
    BubbleMenu/Lerp.cpp
)

SET(LIB_EXTERNAL_INCLUDES
    ${OSG_INCLUDE_DIR}
)

SET(LIB_EXTERNAL_LIBRARIES
    ${OSG_LIBRARIES}
)

SET(LIB_INTERNAL_LIBRARIES
    config
    util
	input
)

SETUP_CORE_LIBRARY(${LIB_NAME})
