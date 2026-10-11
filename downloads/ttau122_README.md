# Tτ AFM: source and calculation notes

Source: Supplemental Material, Table S4, pp. 34–63.
Coverage: 122 T-tau AFM groups; 738 direction branches; no coupled branches.

All branches have chi_xyy = chi_yxx = 0 separately in each physical layer. Every group retains an in-plane antitranslation {T|tau}; tau_z = 0 preserves each layer while time reversal changes the sign of the intrinsic Hall response. This statement concerns physical-layer projections averaged over the complete in-plane magnetic cell, not projections onto sublattices exchanged by tau.

Identifiers and reference symbols follow the source OG setting. A displayed T is the point projection of an antitranslation, not necessarily bare time reversal. Do not reduce an OG antitranslation modulo the family primitive cell before identifying the unitary magnetic translation lattice.

Unitary magnetic translation bases:
- p_2a: (2a,b), antitranslation a.
- p_2b: (a,2b), antitranslation b.
- p_c: (a+b,-a+b), antitranslation b.
- p_p: (a+b,-a+b), antitranslation a.
- c_p: (a,b), antitranslation (a+b)/2.

Recorded corrections:
- 50.4.361, p. 56, operation 06: translation (1/2,0,0) is treated as (1,0,0), from operation 05 times operation 02.
- 61.11.432, p. 61, operation 25: translation (0,0,0) is treated as (1,0,0), from operation 17 times operation 09.

The original records are retained. These corrections affect full affine closure, not the uniform zero-response conclusion. The single GEN branches of 1.3.3 and 2.4.7 cover every direction.

Conventions
-----------
Fixed structure and collinear magnetic order; two physical layers on opposite sides of z = 0. AX_[uvw] denotes a special axis. PL_(hkl) excludes all listed special axes in that plane; GEN excludes every listed special axis and plane. A single GEN branch covers all directions.

Cartesian tensor indices use z normal to the layer. Rectangular settings have x parallel to a and y parallel to b. Hexagonal/trigonal settings use a=(1,0,0), b=(-1/2,sqrt(3)/2,0); crystallographic [010] is not Cartesian y.

The time-reversal-odd Hall convention is chi_abc = -chi_bac. A^l = chi_xyy^l and B^l = chi_yxx^l, with chi_xyx^l = -B^l and chi_yxy^l = -A^l. The rows of each basis matrix are (A^t,B^t,A^b,B^b); columns are independent basis vectors. The same real parameters multiply these columns in all four equations.

Marks: + means equal allowed layer contributions; - means opposite allowed layer contributions (hidden); 0 means forbidden in each layer; v means no fixed same-component interlayer ratio. An asterisk identifies additional cross-component constraints. Allowed values may vanish microscopically.

Displayed operations omit translations. The original archives retain source operations, calculations, affine identification witnesses, and validation records. Coordinates satisfy x_source = C x_reference + origin; operation displays and tensor indices remain in source coordinates.

The source paper supplies the spin layer groups and operations. The direction branches, SOC group assignments, and response constraints are derived calculations. Recorded corrections are computational consistency treatments, not an author-issued erratum. The original archives, including their original documentation language, are preserved byte-for-byte for provenance.

Source: J.-X. Du, S. Zeng and Y.-J. Zhao, Stacking theory for bilayer two-dimensional magnets, Phys. Rev. B 113, 214455 (2026), DOI: 10.1103/g471-xrkl.
