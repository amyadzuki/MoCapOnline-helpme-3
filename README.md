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








