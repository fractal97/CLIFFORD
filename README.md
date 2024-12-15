Installation Instructions for CLIFFORD under Maple 2020.2 running in Windows 10

by

Rafal Ablamowicz
rablamowicz@gmail.com

December 14, 2024
******************************************************************************

Here are the installation instructions for CLIFFORD in Maple 2020.2 running on Windows 10. All necessary files are included in Cliffordlib_distr.zip file.

The following assumes that user has access with administrative privileges to the C:\ drive on his/her own computer. If not, see Comment 2 below.

Instructions:
*************

1. Create a directory Maple2020 on C:\ drive.
2. Create a subdirectory Cliffordlib in the directory C:/Maple2020 .
3. Unzip the file Cliffordlib_distr.zip in the directory C:/Maple2020/Cliffordlib. You should see the following files:

(a) define.m
(b) definemore.m
(c) maple.help
(d) maple.ind
(e) maple.ini
(f) maple.lib
(g) README.txt 
(h) Sample_computations_with_eClifford_ver._3_M2020.mw (A Maple 2020.2 worksheet)
(i) Sample_computations_with_eClifford_ver._3_M2020.pdf (A pdf version of (h))
(j) Walshpackage.m

4. Copy and paste maple.ini file to the directory C:/Program Files/Maple 2020/Users assuming that Maple 2020 has been installed in the directory C:/ProgramFiles/Maple 2020 which is the default installation directory for Maple. If Maple got installed in a different directory, copy and paste maple.ini file into the /Users subdirectory.

Comment 1: Open maple.ini in Notepad. It contains the following lines:

savelibname:="C:\\Maple2020/Cliffordlib":
libname:=savelibname,libname:

where "C:\\Maple2020/Cliffordlib" matches the name of the subdirectory Cliffordlib from point 3. above. Note that
the syntax "C:\\Maple2020/Cliffordlib" is the Maple syntax for the directory C:/Maple2020/Cliffordlib in Windows.

Comment 2: The directory Cliffordlib can be created on any partition, for example, on the D: partition. In that case, user needs to modify the maple.ini file using Notepad and replace the string 

"C:\\Maple2020/Cliffordlib"

with the string

"D:\\Maple2020/Cliffordlib"

Then, save the modified maple.ini by overwriting the original maple.ini in the directory /Users.

5. To test if CLIFFORD works in Maple 2020, do the following:

(a) Start Maple 2020.
(b) At the Maple prompt, type

[> libname; 

and Maple should return this string

"C:Maple2020/Cliffordlib", "C:Program FilesMaple 2020lib"

If so, the installation was done correctly.

Then, type

[> with(Clifford); 

and Maple should return a list of procedures that are evailable in the package Clifford, namely,

[`&m`, Bsignature, CLIFFORD_ENV, Kfield, LC, LCQ, RC, RCQ, RHnumber, adfmatrix, all_sigs, beta_minus, beta_plus, buildm, bygrade, c_conjug, cbasis, cdfmatrix, cexp, cexpQ, cinv, clibilinear, clicollect, clidata, clilinear, climinpoly, cliparse, cliremove, clisolve, clisort, cliterms, cmul, cmulNUM, cmulQ, cmulRS, cmulgen, cocycle, commutingelements, conjugation, ddfmatrix, diagonalize, displayid, extract, factoridempotent, find1str, findbasis, gradeinv, hsplit, init, isVahlenmatrix, isproduct, makealiases, makeclibasmon, matKrepr, maxgrade, maxindex, mdfmatrix, minimalideal, ord, permsign, pseudodet, q_conjug, qdisplay, qinv, qmul, qnorm, rd_clibasmon, rd_climon, rd_clipolynom, reorder, reversion, rmulm, rot3d, scalarpart, sexp, specify_constants, spinorKbasis, spinorKrepr, squaremodf, subs_clipolynom, tp, useproduct, vectorpart, version, wedge, wexp]

To see if Clifford help pages work correctly, type at the Maple prompt

[> ?cmul

and you should see info about the command "cmul".

Hopefully, all will work properly. If not, email me.

Rafal Ablamowicz
rablamowicz@gmail.com

Sarasota, Florida, December 14, 2024

