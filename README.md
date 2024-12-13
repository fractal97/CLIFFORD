# CLIFFORD
A Maple Package for Clifford Algebras by R. Ablamowicz and B. Fauser
(**) Universitat Konstanz, Fachbereich Physik, Fach M678
78457 Konstanz, Germany
Bertfried.Fauser@uni-konstanz.de
bertfried.fauser@googlemail.com

Version 2017.1 of CLIFFORD for Clifford algebra computations in Maple 17 contains the following packages:

CLIFFORD - the main package for computations in Clifford algebras Cl(V,B) of an arbitrary bilinear form B
eClifford - a new small and fast package for computations in Clifford algebras Cl(p,q,r) over vector space V of arbitrary dimension dim V = n = p+q+r which uses a new way to represent basis monomials as indexed names. The quadratic form Q in V may be degenerate and it has signature (p,q,r) with a possible degeneracy in r dimensions or none. A modified code to multiply two basis monomials uses Walsh functions. For more information see:
Sample_computations_with_eClifford_M2017.mw
Sample_computations_with_eClifford_M2017.pdf
Bigebra - for computations with Hopf gebras and bi-gebras
Cliplus - extends CLIFFORD to other bases such as the Clifford basis or the dotted wedge basis
Octonion - for computations with octonions and octonionic matrices
GfG - experimental package for Groebner bases in Grassmann algebras
GTP - extends CLIFFORD to graded tensor products of Clifford algebras
RJgrobner - small package (with Jane Liu) for commutative Groebner bases. It does not need CLIFFORD/Bigebra.
SchurFkt - package for the Hopf Algebra of Symmetric Function
SymGroupAlgebra - an experimental package for computations in the group algebra of the symmetric group S_n
SP - small package for symmetric functions. It does not need CLIFFORD/Bigebra.
Walsh package - this package is included as a Maple worksheet, type [>?cmulWalsh3; at the Maple prompt.
code_support - a package to modify, copy, and insert help worksheets into Maple database. It does not need CLIFFORD/Bigebra.
The above packages are included in one common library file library_M17.zip shown below. Permission is given to download this file and any supporting help files shown below as long as they are for individual use and not for distribution of any kind including posting these files on any other server but this one. It is expected that appropriate acknowledgment will be given to their authors, Rafal Ablamowicz, Bertfried Fauser, and Jane Liu, as appropriate, when results are derived with a help from any of these packages. All packages and their extensive help pages are copyrighted by Rafal Ablamowicz, Bertfried Fauser, and Jane Liu, as indicated.
AVAILABLE FILES:

Download library_M2017.zip - A .zip file with all library files containing compiled code for CLIFFORD ver. 2017.1 including all help pages. [updated 09/04/2017]
For new installation instructions see README.txt. [updated 09/04/2017]
Download Code_of_all_packages_for_Clifford_M17.zip - A .zip file with Maple code of all packages included in CLIFFORD ver. 2017.1. [updated 09/04/2017]
A Maple tutorial for CLIFFORD ver. 16.1 from AGACSE 2012 (one .mws and one .mw worksheet): Tutorial_AGACSE2012.zip
A Maple tutorial for CLIFFORD ver. 17.1 for Alterman Summer School, Brasov, Romania, August 1-9, 2016 (one .mw worksheet): Tutorial_Brasov_2016_M17.zip
A Maple tutorial for CLIFFORD ver. 2017.1 for Alterman Summer School, Sofia, Bulgaria, July 31-August 4, 2017 (one .mw worksheet): Tutorial_Sofia_2017_M2017.zip
You can find out how I use CLIFFORD by going to my recent publications page.

HIGHLIGHTS OF NEW FEATURES IN VERSION 2017.1:
maple.ini file has been modified due to a different way Maple 2017 reads and saves files, that is, an explicit complete path to a directory where an .m file is located must be included in the 'read' statement. Thus, it is convenient to store such files in the same directory as the one saved in 'savelibname'. For example, there is a file Groups_in_Clifford.m stored in \Cliffordlib directory. It can be read into Maple 2017 as follows:

[>read(cat(savelibname,"/","Groups_in_Clifford.m"));

where 'savelibname' stores a path as a string to the \Cliffordlib directory, for example, savelibname = "D:\Maple2017/Cliffordlib". The value of savelibname is assigned in this new maple.ini file. Load and execute a worksheet "G03_as_central_product.mw" as an example.

WARNING: The above modification of maple.ini file is necessary as Maple 2017 cannot read files it saves unless both the "save" and the "read" commands contain the same complete path and a file name.

cmulWalsh3 procedure to multiply Grassmann monomials in Cl(p,q) using Walsh functions is now fully functional. This means that via the command

[> useproduct(cmulWalsh3);

cmul can use internally cmulWalsh3 in Clifford algebras Cl(Q) of a non-degenerate quadratic form Q of signature (p,q). This procedure is part of Walshpackage. This package must be read in via the command

[> read(cat(savelibname,"/","Walshpackage.m"));

A new help page on the entire Walshpackage is now included in Maple help system. Issue command

[> ?cmulWalsh3

to see Maple worksheet with the code of Walshpackage.
Please direct all questions, comments, and bug reports to:
