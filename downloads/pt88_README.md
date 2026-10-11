# PT AFM: source and calculation notes

Source: Supplemental Material, Table S5.
Coverage: 88 PT AFM groups; 625 direction branches; 104 coupled branches.

PT remains present for all Neel-axis directions and exchanges the two physical layers. For this time-reversal-odd polar Hall tensor it enforces equal contributions in the two layers. Therefore only + and 0 occur in the component marks. Other operations can forbid components or couple chi_xyy and chi_yxx.

Recorded corrections: the Mx translation in operation 08 of 39.3.258, 39.6.261, and 39.7.262 is treated as (0,1/2,0), consistent with multiplication and affine closure. See the original reports for the audit trail.

Conventions
-----------
Fixed structure and collinear magnetic order; two physical layers on opposite sides of z = 0. AX_[uvw] denotes a special axis. PL_(hkl) excludes all listed special axes in that plane; GEN excludes every listed special axis and plane. A single GEN branch covers all directions.

Cartesian tensor indices use z normal to the layer. Rectangular settings have x parallel to a and y parallel to b. Hexagonal/trigonal settings use a=(1,0,0), b=(-1/2,sqrt(3)/2,0); crystallographic [010] is not Cartesian y.

The time-reversal-odd Hall convention is chi_abc = -chi_bac. A^l = chi_xyy^l and B^l = chi_yxx^l, with chi_xyx^l = -B^l and chi_yxy^l = -A^l. The rows of each basis matrix are (A^t,B^t,A^b,B^b); columns are independent basis vectors. The same real parameters multiply these columns in all four equations.

Marks: + means equal allowed layer contributions; - means opposite allowed layer contributions (hidden); 0 means forbidden in each layer; v means no fixed same-component interlayer ratio. An asterisk identifies additional cross-component constraints. Allowed values may vanish microscopically.

Displayed operations omit translations. The original archives retain source operations, calculations, affine identification witnesses, and validation records. Coordinates satisfy x_source = C x_reference + origin; operation displays and tensor indices remain in source coordinates.

The source paper supplies the spin layer groups and operations. The direction branches, SOC group assignments, and response constraints are derived calculations. Recorded corrections are computational consistency treatments, not an author-issued erratum. The original archives, including their original documentation language, are preserved byte-for-byte for provenance.

Source: J.-X. Du, S. Zeng and Y.-J. Zhao, Stacking theory for bilayer two-dimensional magnets, Phys. Rev. B 113, 214455 (2026), DOI: 10.1103/g471-xrkl.
