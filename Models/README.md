There are 2 models included here for testing.  They were created in (makehuman-1.1.1-win32)[http://download.tuxfamily.org/makehuman/releases/1.1.1/makehuman-1.1.1-win32.zip].

Each model is saved as `{{Name}}.mhm` and exported 8 times as `{{Name}}-{{Units}}-{{Rig}}.fbx` with the following export options:

Common export options:
  - [x] Feet on ground
  - [x] Binary FBX
  - [ ] Helper geometry*

*Note that (to the best of my knowledge) "helper geometry" is untextured vertices of a skirt and male genitalia.  I do not use this option.

The protagonist in my game is a 14-year-old girl, but the Unreal Mannequin is a large man, so I have chosen the following two models for testing:

Name=`Male25`:
  - The gender slider was set to "100% male"
  - The age slider was left on the default age of exactly 25.
  - Clothes: "Female casualsuit01" (default is naked and this one is public domain; I'm using a different one in-game but it isn't public domain)
  - Eyes: "high-poly eyes", "Brown" (the defaults; I'm using these settings in-game)
  - Skin: "Young asian female" (I'm using this skin in-game; the default is untextured)

Name=`Female14`:
  - The gender slider was set to "100% female"
  - The age slider was programmatically set to exactly age 14.
  - Clothes: "Female casualsuit01" (default is naked and this one is public domain; I'm using a different one in-game but it isn't public domain)
  - Eyes: "high-poly eyes", "Brown" (the defaults; I'm using these settings in-game)
  - Skin: "Young asian female" (I'm using this skin in-game; the default is untextured)

Units=`cm`:
  - Scale units: centimeter

Units=`dm`:
  - Scale units: decimeter

Rig=`generic`:
  - Skeleton: "Game engine" (recommended for use with Unreal Engine 4)

Rig=`unreal`:
  - Skeleton: "uengine" (designed specifically for Unreal Engine 4; via plugin)

Anything not mentioned specifically was left on the default.
