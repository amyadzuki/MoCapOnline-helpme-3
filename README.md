# Software Versions:
  - Unreal Engine v4.20.3 (the latest version with all updates applied)
  - MakeHuman v1.1.1-win32 (the latest version; [download link](http://download.tuxfamily.org/makehuman/releases/1.1.1/makehuman-1.1.1-win32.zip))

# Animation Pack:
  - Product: `[UE4] Mobility Basic: MoCap Animation Pack`
  - Order ID: `SPYMCP8213162`
  - Filename: `UE4_Mobility127_Basic.zip`

# Reproduction Steps:

  - Extract `UE4_Mobility127_Basic.zip` to `C:\Users\UE4\Assets\UE4_Mobility127_Basic`
    + `Mobility127_Basic.uproject` is `C:\Users\UE4\Assets\UE4_Mobility127_Basic\Mobility127_Basic.uproject`
  - Launch Unreal Engine 4.20.3
  - New Project
    + Blueprint
    + Blank
    + Desktop / Console
    + **Scalable 2D or 3D**
    + No Starter Content
    + Folder: `C:\Users\UE4\Projects`
    + Name: `AmyMoCapOnlineHelp3`
  - I get a pop-up notification "New plugins are available" and choose "Dismiss" because I don't want plugins interfering.
  - At this point, `Content` is completely empty.
  - Using the File Explorer app, I copy `C:\Users\UE4\Assets\UE4_Mobility127_Basic\Content\Mobility_01\Animation` into `C:\Users\UE4\Projects\AmyMoCapOnlineHelp3\Content`
    + `Aim_Offsets` is `C:\Users\UE4\Projects\AmyMoCapOnlineHelp3\Content\Animation\Aim_Offsets`
  - Using the UE4 Content Browser, I create a new folder in `Content` called `Textures`.
  - I browse to the new `Textures` folder in the UE4 Content Browser and drag in the entire contents of `textures` (included in this repo as /Models/exports/textures).
    + I get a notification popup, "Texture female_casualsuit01_normal was imported as a normal map"
  - Using the UE4 Content Browser, I go back up a directory to `Content` and create a new folder called `Characters`.
  - I browse to the new `Characters` folder in the UE4 Content Browser and drag in the entire contents of `exports` (included in this repo as /Models/exports), **excluding `textures`** since I already imported them.
    + Mesh:
      * [x] Skeletal Mesh
      * [x] Import Mesh
      * Skeleton: None
    + Animation:
      * [ ] Import Animations
    + Transform:
      * Import Translation: 0.0, 0.0, 0.0
      * Import Rotation: 0.0, 0.0, 0.0
      * Import Uniform Scale: 1.0
    + Miscellaneous:
      * [x] Convert Scene
      * [ ] Force Front XAxis
      * [ ] Convert Scene Unit
    + Material:
      * Base Material Name: None
      * [ ] Import Materials
      * [ ] Import Textures
    + Import All
  - I ignore the one warning I get:
    + `No smoothing group information was found in this FBX scene.  Please make sure to enable the 'Export Smoothing Groups' option in the FBX Exporter plug-in before exporting the file.  Even for tools that don't support smoothing groups, the FBX Exporter will generate appropriate smoothing data at export-time so that correct vertex normals can be inferred while importing.`
    + [Docs](https://docs.unrealengine.com/en-us/Shared/Editor/FbxErrors?utm_source=editor&utm_medium=docs&utm_campaign=msg_log)
  - **Save All**
  - **Edit -> Editor Preferences -> General -> Loading & Saving -> Auto Save:**
    + [ ] **Enable AutoSave**
    + **I disable AutoSave so I can revert to this point in time as I try things!**
  - **Save Current**
    + Path: `/Game`
    + Filename: `NewMap`

---

  - I open `/Content/Characters/Male25-cm-generic_Skeleton` in the UE4 Content Browser
  - Retarget Manager
    + Select Rig: Select Humanoid Rig
    + Save
  
  - I open `/Content/Animation/IPC/MOB1_Stand_Relaxed_Idle_v2_IPC` in the UE4 Content Browser and get this message:
    + `Could not find the skeleton for Anim 'MOB1_Stand_Relaxed_Idle_v2_IPC'  Would you like to choose a new one?`
    + I answer `Yes`
  - The Select Skeleton dialog pops up, and I click `Male25-cm-generic_Skeleton` in the left pane.
    + Both `[Source]` and `[Target]` previews appear blank.
  - I leave the Retarget Options on their default settings:
    + [x] Remap referenced assets
    + [ ] Allow remapping to existing assets
  - I click the `Retarget` button.
  - The result looks severly deformed, see the screenshot, `(placeholder for screenshot path)`.
