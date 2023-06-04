In this repository I'm learning differences which Caleb Maclennan made to update electron AUR package from 22 version to 24.

#### changes

1. bumped [electron](https://github.com/kup1o/electron_diff/blob/48a13b8f5c156281519a8ac83c84751c199d84ab/PKGBUILD#L9) & [chromium](https://github.com/kup1o/electron_diff/blob/48a13b8f5c156281519a8ac83c84751c199d84ab/PKGBUILD#L10) versions. used [suffix](https://github.com/kup1o/electron_diff/blob/48a13b8f5c156281519a8ac83c84751c199d84ab/PKGBUILD#L8) for electron version(24.4.**1**)
2. forced [use](https://github.com/kup1o/electron_diff/blob/48a13b8f5c156281519a8ac83c84751c199d84ab/PKGBUILD#L29) `libffi` from [system](https://github.com/kup1o/electron_diff/blob/48a13b8f5c156281519a8ac83c84751c199d84ab/PKGBUILD#L317) instead of repository because of [repetition count update](https://github.com/AOMediaCodec/libavif/commit/4d2776a)
3. changed electron source to [use tag](https://github.com/kup1o/electron_diff/blob/48a13b8f5c156281519a8ac83c84751c199d84ab/PKGBUILD#L51) instead of commit
4. changed chromium source to [official repository](https://github.com/kup1o/electron_diff/blob/48a13b8f5c156281519a8ac83c84751c199d84ab/PKGBUILD#L52)
5. changed [patches](https://github.com/kup1o/electron_diff/blob/48a13b8f5c156281519a8ac83c84751c199d84ab/PKGBUILD#L60-L77) that is used to compile chomium
6. [skipped](https://github.com/kup1o/electron_diff/blob/48a13b8f5c156281519a8ac83c84751c199d84ab/PKGBUILD#L82) sha256 sum for chromium
7. [added](https://github.com/kup1o/electron_diff/blob/48a13b8f5c156281519a8ac83c84751c199d84ab/PKGBUILD#L89-L106) sha256 sums for patches
8. [linked](https://github.com/kup1o/electron_diff/blob/48a13b8f5c156281519a8ac83c84751c199d84ab/PKGBUILD#L168) chromium source to economy disk space
9. [disabled](https://github.com/kup1o/electron_diff/blob/48a13b8f5c156281519a8ac83c84751c199d84ab/PKGBUILD#L307) Profile-Guided Optimization([wiki](https://en.wikipedia.org/wiki/Profile-guided_optimization)). See `chrome_pgo_phase` in [list of all gn arguments](https://gitlab.com/noencoding/OS-X-Chromium-with-proprietary-codecs/-/wikis/List-of-all-gn-arguments-for-Chromium-build#code-40) to understand flags
