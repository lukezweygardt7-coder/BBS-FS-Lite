# BBS FS Lite (1.20.1)

A low-memory fork of [BBS FS](https://github.com/Wemppy4/bbs-fs) (itself a fork of McHorse's BBS mod), MIT licensed;
see LICENSE.md. Built for devices with very little RAM, such as a tablet with a 600 MB Java heap.

Changes from upstream (branch 1.20.1, commit 998c9d5):

- **Texture eviction** (`TextureManager`): upstream keeps every texture loaded until it is deleted by hand. This fork
  remembers when each texture was last used; when the Java heap is over 65% full it deletes textures that have not
  been used for 15 seconds (5 seconds when over 80%). They reload from disk on demand.

More changes will be listed here as they are made.
