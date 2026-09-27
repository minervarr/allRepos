# allRepos

Registry of the projects and first-party libraries. This repo holds no source of its own. Each path is a submodule pinned to the commit checked out on 2026-09-27.

Apps pin those libraries again inside themselves. The library entries here are the `main` tips, except `Vk_Canvas_Lb_LAW`, which is the standalone `hdr-output` checkout. Camera keeps its own `raw-isp-fp16` pins inside `camera_without_blood`.

## Restore

```bash
git clone --recurse-submodules https://github.com/minervarr/allRepos.git
```

The clone is detached on each pin. To keep working on the recorded branch:

```bash
git submodule foreach 'b=$(git config -f $toplevel/.gitmodules submodule.$sm_path.branch); git switch "$b"'
```

## Registry

| Path | Branch | Commit | What it is |
|---|---|---|---|

| `AndroidOneAudioServer_AOAS` | `main` | `8d3d00caca1b` | USB audio server |

| `Economycs` | `main` | `648abb80fef1` | Economycs (GitHub name Econo_miss) |

| `ImagesLogosCreator` | `main` | `b557c0067b65` | glyph and logo tool |

| `Matrix_Player` | `main` | `46a78e007581` | music player |

| `PKGBUILD` | `main` | `ca03522bec73` | workspace restore script and packaging notes |

| `Print_BooksAndSo` | `main` | `9779eaa56ad5` | print and LaTeX books |

| `UI_demo_LAW` | `main` | `c9260562753f` | UI demo |

| `VideoPlayer` | `main` | `b33bab1eda6d` | video player |

| `ViewMage` | `main` | `b3057033ffc2` | image viewer |

| `Vk_Canvas_Lb_LAW` | `hdr-output` | `146bb4a245b0` | Vulkan canvas, standalone checkout |

| `archive_engine` | `main` | `0dc0d959bc9f` | archive and media-index library |

| `audio_recorder` | `main` | `9320bb857b35` | USB recorder |

| `camera_without_blood` | `raw-isp-30fps` | `4b15c032eb69` | camera app |

| `git_wrapper` | `main` | `3cb0a4bacc41` | commit and push wrapper |

| `navaLauncher` | `main` | `f88349ca5c8f` | Android launcher |

| `streamer` | `main` | `cb0c84472e3c` | streamer |

| `whisper_ui_cpp` | `main` | `ef4791dc3742` | whisper UI |

| `App_shell` | `main` | `01f5d2436f2f` | window and lifecycle shell |

| `audio_engine` | `main` | `6934cdc287f5` | audio I/O library |

| `vulkan_font_engine` | `main` | `937988b05919` | font engine used by vk_canvas |

| `fonts` | `main` | `0bb1f804edfa` | shared typefaces |

| `regen_atlas` | `main` | `17a6c0160886` | atlas library used by the camera |

| `KawusapiCC` | `main` | `ad29df1e5e15` | streamer library |

| `reference/media_player` | `master` | `93d9d7f19079` | earlier media player |


## Kept out of the clone

- `reference/AutoEq` is the upstream [jaakkopasanen/AutoEq](https://github.com/jaakkopasanen/AutoEq) checkout at `7ae0f56d5307` on `master`. It is a measurement database of several gigabytes, so it is registered here and not vendored.

- `LaTeX_Everywhere` has a GitHub remote and no commits.

- `LiveTheLife`, `AudioTrans`, and `MusicCreation` are folders on this machine without a git repository.

- Build directories, generated assets, `~/.git-credentials`, and the Android keystores are not part of any of these pins. The keystore that is already inside Matrix_Player stays there.
