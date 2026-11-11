OSQP v0.6.3 build compatibility patch

Base: https://github.com/osqp/osqp.git, tag v0.6.3.
Keep its original recursive QDLDL revision; no custom submodule commit is needed.

osqp-00.patch raises the minimum CMake version to 3.5 in OSQP and QDLDL,
and generates/installs osqp-config-version.cmake for versioned downstream
find_package calls. The recipe supplies OSQP_VERSION=0.6.3 explicitly.
Generated headers are not part of the patch, and solver code is unchanged.

The custom recipe steps apply the patch before configuring, as Xenomai does.
Forest's CMake pre_build hook runs after configure and is too late here.
A reverse check skips the patch
when already applied, including after CMake has generated source headers.
This follows the Xenomai patch directory convention while supporting rebuilds.

The CMake changes work with Noble's CMake 3.28 as well as CMake 4, so the
CMake-4-only CMAKE_POLICY_VERSION_MINIMUM flag is no longer necessary.
