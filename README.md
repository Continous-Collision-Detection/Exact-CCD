# Exact CCD: Efficient Geometrically Exact Continuous Collision Detection

Released into the public domain by Tyson Brochu and Robert Bridson, 2012.

To make the library, edit the Makefile if needed and then run make; a static library file will be created.  This together with header file "rootparitycollisiontest.h" provides C++ access to the CCD routines.  

To use, create a RootParityCollisionTest object by specifying the vertex positions at the time step beginning and end times, and whether the test should be edge-vs-edge or vertex-vs-triangle, then call run_test() on the object.

IMPORTANT NOTE: Compiler optimizations may cause incorrect behaviour by assuming properties of floating-point arithmetic which do not actually hold, or by using 80-bit extended-precision registers. It has been tested with GCC 4.2.1 on Mac OS X with the -O2 flag set.

# Fast and Exact Continuous Collision Detection with Bernstein Sign Classification

1. Usage:
The entry points for VF/EE tests are:
```cpp
bool Intersect_VF_robust(
	const Vec3d &a0, const Vec3d &b0, const Vec3d &c0, const Vec3d &d0,
	const Vec3d &a1, const Vec3d &b1, const Vec3d &c1, const Vec3d &d1)
```
and
```cpp
bool Intersect_EE_robust(
	const Vec3d &a0, const Vec3d &b0, const Vec3d &c0, const Vec3d &d0,
	const Vec3d &a1, const Vec3d &b1, const Vec3d &c1, const Vec3d &d1)
```
We are using the IntervalType/expansion classes of El Topo.
It can be downloaded from http://www.cs.ubc.ca/labs/imager/tr/2012/ExactContinuousCollisionDetection/exactccd.tar.gz

2. Reference:<br>
Min Tang, Ruofeng Tong, Zhendong Wang, Dinesh Manocha, Fast and Exact Continuous Collision Detection with Bernstein Sign Classification, ACM Transactions on Graphics, 33(6), Article 186 (November 2014), 8 pages (Proc. of ACM SIGGRAPH Asia), 2014.

3. Bug Report: We would be interested in knowing more about your application as well as any bugs you may encounter when using the codes. You can report them by sending e-mail to geom@cs.unc.edu or tangm@cs.unc.edu
