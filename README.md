[![License](https://img.shields.io/github/license/AcademySoftwareFoundation/Imath)](LICENSE.md)
[![CII Best Practices](https://bestpractices.coreinfrastructure.org/projects/2799/badge)](https://bestpractices.coreinfrastructure.org/projects/2799)
[![Build Status](https://dev.azure.com/academysoftwarefoundation/Academy%20Software%20Foundation/_apis/build/status/academysoftwarefoundation.Imath)](https://dev.azure.com/academysoftwarefoundation/Academy%20Software%20Foundation/_build?definitionId=4&_a=summary)
[![Quality Gate Status](https://sonarcloud.io/api/project_badges/measure?project=AcademySoftwareFoundation_Imath&metric=alert_status)](https://sonarcloud.io/dashboard?id=AcademySoftwareFoundation_Imath)

# Imath

Imath is a basic, light-weight, and efficient C++ representation of 2D
and 3D vectors and matrices and other simple but useful mathematical
objects, functions, and data types common in computer graphics
applications, including the “half” 16-bit floating-point type.

Imath also includes optional python bindings for all types and
functions, including optimized implementations of vector and matrix
arrays. 

### Project Mission

The goals of the Imath project are simplicity, ease of use,
correctness and verifiability, performance, and breadth of
adoption. Imath is not intended to be a comprehensive linear algebra
or numerical analysis package.

### Features

* half: 16-bit floating-point type
* Vector: V2s, V2i, V2i64, V2f, V2d, V3s, V3i, V4i64, V3f, V3d, V4s, V4i, V4i64, V4f, V4d 
* Matrix: M22f, M22d, M33f, M33d, M44f, M44d 
* Bounding box: Box2s, Box2i, Box2i64, Box2f, Box2d, Box3s, Box3i, Box3i64, Box3f, Box3d
* Color: C3h, C3f, C3c, C4f, C4h, C4c 
* Euler angles: Eulerf, Eulerd
* Quaternion: Quatf, Quatd
* Viewing frustum: Frustrumf, Frustumd
* Interval: Intervals, Intervali, Intervalf, Intervald
* Line: Line3f, Line3d
* Plane: Plane3f, Plane3d
* Sphere: Sphere3f, Sphere3d
* Shear: Shear3f, Shear3d, Shear6f, Shear6
* Miscellaneous math functions
  
### New Features in 3.1

The 3.1 release of Imath introduces optimized half-to-float and
float-to-half conversion, using Intel intrinsics if available, or
otherwise using an optimized bit-manipulation algorithm that does not
require lookup tables. Performance of both options is generally
significantly faster than the lookup-table based conversions that
Imath has traditionally used, although results may vary depending on
the nature of the data. The new optimized conversions generate the
same values as the tranditional methods.

For backwards compatibility and ensured stability in the 3.1 release,
the optimized conversion is off by default, but it can be enabled at
compile-time by disabling the ``IMATH_USE_HALF_LOOKUP_TABLES`` cmake
option.

### Supported Platforms

Imath builds on Linux, macOS, Microsoft Windows, and is
cross-compilable on other systems.

### About Imath

Imath was originally developed at Industrial Light & Magic in the
early 2000's and was originally distributed as open source as a part
of the [OpenEXR](https://github.com/AcademySoftwareFoundation/openexr)
project.

Imath continues to be maintained as a sub-project of OpenEXR, which is
now a project of the [Academy Software
Foundation](https://www.aswf.io).  See
the OpenEXR project's [GOVERNANCE.md](https://github.com/AcademySoftwareFoundation/openexr/blob/master/GOVERNANCE.md)
for more information about how the project operates.

The OpenEXR project is dedicated to promoting a harassment-free
community. Read our [code of conduct](CODE_OF_CONDUCT.md).

### Developer Quick Start

See [INSTALL.md](INSTALL.md) for instructions on downloading and building Imath
from source.

Documentation for the Imath classes and functions can be found at
[imath.readthedocs.io](https://imath.readthedocs.io).

If you encounter problems compiling code or building projects written
with an earlier release of Imath, the [porting
guide](https://github.com/AcademySoftwareFoundation/Imath/blob/master/docs/PortingGuide2-3.md)
explains some of the differences and how to address them.

### A Note about Versioning

Because Imath was originally distributed as a part of OpenEXR, it has
already had two major release versions, as a part of OpenEXR v1.* and
v2.*. To avoid confusion with these original releases, the first
version of Imath released independently of OpenEXR is Version v3.0. To
be clear, the versioning and release of Imath is no longer tied to
OpenEXR.

### Getting Help

There are two primary ways to connect with the project:

* The openexr-dev@lists.aswf.io mail list: This is a development
  focused mail list with a deep history of technical conversations and
  decisions that have shaped the project. Subscribe at
  [openexr-dev@lists.aswf.io](https://lists.aswf.io/g/openexr-dev).

* GitHub Issues: GitHub issues are used both to track bugs and to
  discuss feature requests. Submit an issue here:
  https://github.com/AcademySoftwareFoundation/imath/issues. 

### Getting Involved

The OpenEXR developer community welcomes contributions to the
project. See [CONTRIBUTING.md](CONTRIBUTING.md) for more information
about contributing to Imath and OpenEXR.

## License

Imath is released under OpenEXR's [BSD-3-Clause](LICENSE.md) license.

---

![aswf](https://github.com/AcademySoftwareFoundation/openexr/blob/master/ASWF/images/aswf.png)
