# ExportSceneToObj

A plug-in for exporting Unity scenes (including GameObjects and Terrain) as `.fbx` model or `.obj` files.

This plugin was developed by [monitor1394](https://github.com/monitor1394/ExportSceneToObj) and all rights belong to them.
There was a problem when the export process would stop running if one mesh failed to export, this is fixed now.
README is translated mostly using Google Translate.
It is missing the part about `fbx` export since it didn't translate well.

Feel free to create issues if you find any mistakes or PRs if you want to contribute.
Please also contribute to the original repo.

Also please star the original repo even if you're using this one.

## Features

* Supports exporting objects and terrain
* Supports custom crop area
* Supports auto crop function
* Supports single selection export
* Supports export as an `.fbx` model


## Screenshots

<img src="Documentation/screenshot/scene.jpg" width="1024" height="auto"/>
<img src="Documentation/screenshot/export.jpg" width="1024" height="auto"/>
<img src="Documentation/screenshot/part.jpg" width="1024" height="auto"/>
<img src="Documentation/screenshot/select.jpg" width="1024" height="auto"/>

## Installation

### Unitypackage

* Download latest `.unitypackage` from Releases.
* Import to Unity via `Assets` -> `Import Package` -> `Custom Package...`

### Direct

* Download source folder.
* Unpack it and paste to your `Assets` folder.

## Usage

Use `ExportScene` menu in the top menu bar in Unity.

If you want to customize the cropping area, add an empty space `GameObject` in the scene to represent the cropping area (you need to have empty space in the lower left corner and the upper right corner GameObject), and change `CUT_LB_OBJ_PATH` and `CUT_RT_OBJ_PATH` to corresponding path.

## Misc

* Only objects which contain a `MeshFilter`, `SkinnedMeshRenderer`, or `Terrain` will be exported.
* Currently, whether the object is in the clipping area is only judged by whether the coordinates of the object are in the area. Boundary clipping of the object is not handled.
* For correct import into 3ds Max, check `Import as single mesh` option in the import settings.

## References

1. [ExportOBJ](http://wiki.unity3d.com/index.php?title=ExportOBJ)
2. [TerrainObjExporter](http://wiki.unity3d.com/index.php?title=TerrainObjExporter)
