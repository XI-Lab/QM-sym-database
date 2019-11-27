#Readme file of QM-sym-database, edit by Liang at 2019.9.12
#New Version of QM-sym with seperation on the space groups

Format of QM-sys xyz file

name: QM_sys_id.xyz

Line	                                 Content
1	                                 Number of atoms N*n_a (+1)
2	                                 Properties of molecule
3, ..., 2+n_a	                 Coordinate of atoms in the first subgroup
3+n_a, ..., 2+2*n_a	                 Coordinate of atoms in the second subgroup
......
3+(N-1)n_a, ..., 2+N*n_a             Coordinate of atoms in the last subgroup
(4+N*n_a)	                                (Coordinate of atom at the center)


example:
number of atoms
Symmetry Group | Band Gap (Ha) | LUMO (Ha) | HOMO (Ha) | Rotationl Constant (GHz) 1| 2 | 3 | Dipole Moment (D) x | y | z | total | Isotropic Polarizability (a0^3) | Electronic Spatial Extent (au) | Zero-point Vibrational energy (J/mol) | (Kcal/mol) | Sum of electronic and zero-point energies (Ha) | Sum of electronic and thermal energies (Ha) | Sum of electronic and thermal enthalpies (Ha) | Sum of electronic and thermal free energies (Ha) | Heat Capacity (J*K^-1) | Dengeneracy of orbitals -5 | -4 | -3 | -2 | -1 | HOMO | LUMO | +1 | +2 | +3 | +4 | +5 | Symmetry of orbitals -5 | -4 | -3 | -2 | -1 | HOMO | LUMO | +1 | +2 | +3 | +4 | +5 | Indication of subgroups and atoms
atom    x    y    z    mullikan_charge
......
......



# In degeneracy and symmetry, LUMO and HOMO are reak LUHO-HOMO, as for -5, ... , -1, +1, ... , +5, they are just symbols and depend on degeneracy. The number of orbitals is at least 12. If the degeneracy of HOMO is 3, then +1 is actually HOMO+3. 

# Indication of sub groups: example: 11 12 13 21 22 23 04
# The first number of '11', which is '1', means it is in subgroup 1. '11' and '21' are atoms of the same element at the same position in subgroup '1' and '2'.
# If the first number is '0', this atom is at the rotation axes, and '4' is used to differ it from other atoms in each subgroups.
