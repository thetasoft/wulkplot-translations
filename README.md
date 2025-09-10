# wulkplot-translations
This repo serves as a submodule for the [wulkplot](https://github.com/thetasoft/wulkplot) repo. All translation metadata as well as compiled translations (see [releases](https://github.com/thetasoft/wulkplot-translations/releases)) are stored here to keep things nice and separated (avoiding a bunch of noise in the main repo).

## A note on versioning
The translation repository has its own versioning system that is fully independent of Wulkplot's versioning. This means that for any version of Wulkplot, several compiled translation versions may or may not be compatible. In practice, the versioning system for translations works as follows:

```bash
X.Y.Z[a-z]
```
- **[a-z] (Meta)**: Recompiled version with updated metadata, with no changes to the actual translations.
- **Z (Patch)**: Changes to existing UI elements such as correcting grammar mistakes or completely rewriting existing sentences result in a bump of the Z number.
- **Y (Minor)**: When newer Wulkplot versions add new UI elements that need translating, those new translations bump Y and reset Z to 0.
- **X (Major)**: Reserved for when locales are added or removed. When a language is added or removed, X is bumped and both Y and Z are reset to 0.

For example, a version might look like this:
```bash
2.7.3c
```
The 2 indicates that 2 new locales have been added (in addition to the base locales which were there from the start). The 7 indicates 7 revisions to accommodate new UI elements. The 3 indicates 3 patches to fix up grammar or change phrases. Finally the c indicates that this is the third recompiled version with updated metadata.

The `.translations-version` file keeps track of the current version.