# Folder Size Window

A Unity Editor window that displays the runtime memory size of folders and selected assets in the Project window.

## Features

- Uses [`Profiler.GetRuntimeMemorySizeLong`](https://docs.unity3d.com/ScriptReference/Profiling.Profiler.GetRuntimeMemorySizeLong.html) to calculate size.
- Supports Project window and asset Selection sources.
- Sorts results alphabetically or by size.
- Calculates asynchronously with a per-item progress indicator.
- Displays the total size of the current results.

## Installation

In Unity, open **Window > Package Manager**, choose **+ > Add package from git URL**, and enter:

```text
https://github.com/mitay-walle/com.mitaywalle.folder-size-window.git
```

The package requires Unity 2021.3 or newer and depends on `com.unity.editorcoroutines`.

## Usage

Open **Window > Analysis > Folder Size**. Choose **Project Window** to inspect assets shown in the active Project window folder, or **Selection** to inspect the currently selected assets.

## Known Issues

- Uncollapsed subfolders may be shown from the left side of the Project window.
- Prefab size is approximate.
- Scene size is not calculated because `Profiler.GetRuntimeMemorySizeLong` throws for scenes.
- Vertex compression is a build-time setting and is not included in the calculation.
