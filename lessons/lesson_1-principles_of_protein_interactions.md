# Chapter 1
## 1. Introduction to Protein-ligand interactions 

The interactions between proteins and other molecules, collectively referred to as ligands, are of fundamental importance for the many biological processes that take place into living cells. Ligands can be other proteins, but also peptides, nucleic acids, small molecules, or ions.

Protein interactions can be studied from different perspectives. 

**Reductionist biology**: involves an atomic and molecular level of analysis. The aim is to analyse small portions of larger systems and later on connecting everything together (Van Regenmortel 2004). We focus on specific macromolecules of interest that belong to a larger system, and study atoms or molecules participating in the interaction among these macromolecules, as well as how interactions occur. Experiments are carried out so as to identify interaction partners and to characterise the modes of interaction. The focus is on single interactions, rather than on the entire biological system. The analysis of specific interactions can be done through experimental and/or computational prediction strategies.

**Protein networks**: protein-protein interaction (PPIs) networks are mathmatical representations of the interactions among proteins in a cell (European Bioinformatics Institute n.d.). In a protein interaction network, proteins are represented as "nodes" and their interactions as "edges". Proteins can interact directly, indirectly, forming a complex and/or establishing transient interactions. Thanks to protein networks we can identify hubs (proteins that interact with many other proteins), non-hubs (proteins that interact with one or a few other proteins) and singletons (non-interacting proteins). This approach makes it possible to learn several aspects of PPIs. For example, we can identify functional modules, which are sets of proteins that are highly interconnected to each other and that could be indicative of sets of functionnally related proteins such us proteins participating in a complex or a pathway; we can study the centrality of certain nodes (or edges), such hubs, which take part in many interactions and are therefore essential for the information flow across the network. The analysis of a protein network can also give insights on how perturbating events may affect a network, as well as infer the function of not yet characterised proteins. Furthermore, it is possible to identify networks associated with pathological states and networks that are deregulated or perturbed.


**Systems biology**: if we look at a biological system as a whole, interconnected entity composed of many networks and pathways that share information among each other, we fall into the Systems biology approach. Here, we study the behaviour of an entire cell instead of single interactions or single PPI networks. It is possible to make computational predictions of the effect of perturbations on the system and test these predictions experimentally. In System biology, differential equations are the typical mathematical tools used for modeling biological systems.


Protein functions are based on the capability of proteins to bind a certain ligand (or more). Ligands can be atoms, small molecules, peptides, proteins, as well as other macromolecules (DNA, RNA). 

> ### A few definitions:
>
> 1. Binary interactions
> 	-	Interactions occurring between two molecules
> 2. Protein complex
> 	- A stable complex formed of two or more interacting proteins
> 3. Homo vs hetero
> 	- We use the prefix "homo" for a complex formed of only one type of subunit (homodimer, homooligomer, homomultimer, etc); we use the prefix hetero for protein complexes made up of different proteins (heterodimer, hetero-oligomer, heteromultimer, etc)
> 4. Stable vs transient
> 	- Stable or permanent interactions: Complexes that interact for long periods of times. They have binding affinities in the range of nM.
> 	- Transient interactions: reversible interactions that occur in a short period of time. They are characterized by binding affinities in the range of μM and lifetimes in seconds (Perkins et al., 2010)
> 5. Protein binding interface
> 	- A protein binding interface is defined as the set of atoms of a protein that are less than 5 Å apart from an atom of the partner protein.
> 6. PPI network
>  - protein-protein interaction networks (PPINs) are math- ematical representations of the physical contacts between proteins in the cell (European Bioinformatics Institute)
> 7. hubs, non-hubs, singletons
> 	- hubs are proteins that interact with many other proteins
> 	- non-hubs are proteins that interact with one or few other proteins
> 	- singletons are non-interacting proteins
> 8. Interactome
>  - An interactome is a PPI network that includes all the interactions in a biological system (could be a cell, a cell compartment, or an entire organism). 
> 


### 1.1 Protein-ligand interactions: principles of thermodinamics

Proteins can bind a plethora of different molecules with different modalities. All their interactions are guided by thermodynamics principles, whose in-depth discussion is beyond the scope of this chapter. Nevertheless, some basic concepts and principles are helpful in formalising the laws that guide protein interactions.

### 1.1.1 Gibbs free energy (G)

Any physico-chemical process is spontaneous when it entails a reduction in the free energy of the systems it belongs to. This is true also for protein interactions. The free energy that we are considering here is the Gibbs free energy, normally referred to as G. 
This quantity is a thermodynamic state function, meaning that its value depends only on the current equilibrium state of the system, not on the path followed to reach the current state. The Gibbs free energy is a measure of the amount of energy of the system which is available (free) for carrying out work. It is related to other thermodynamic state functions, enthalpy (H), entropy (S) and temperature (T) by the following equation:

**G = H − TS**  &nbsp; [1]    

What matters in determining the spontaneity of reactions is not the absolute value of free energy, but its variations. A process that causes a decrease in free energy of the system (∆G < 0) is defined as exergonic and it is spontaneous. A process that causes an increase in free energy of the system (∆G > 0) is defined as endergonic and it is not spontaneous. To be possible, an endergonic process must be coupled with an exergonic process such that the total variation in the free energy of the system is negative. Biological systems do not exist in isolation, but in an environment with an approximately constant temperature. Because of this, we can treat temperature as a constant and focus on how the variations in entropy and enthalpy relate to the variations in free energy.
∆G = ∆H − T ∆S (2) Entalpy The internal heat content of a system is described by its enthalpy. It is composed of the
internal energy of the system (E) plus the product of its pressure (P) and volume (V).
H=E+PV (3)
In biological systems, we typically are in a state of constant pressure and temperature. Because of this, it is possible to approximate the variations in the enthalpy of the system with variations in its internal energy.
∆H ≈ ∆E (4) The internal energy is itself composed of a potential energy term (U) and a kinetic term (K).
E=U+K (5) In a biological context, the potential energy is due to the set of covalent and non-covalent interactions
that take place in the system. The kinetic energy is the result of the thermal motion of molecules.
In a biological system variations in enthalpy can ultimately be ascribed to the formation or breakage of covalent bonds and the alteration of weak interactions (Van der Waals, electrostatic interactions). Since biological systems are not isolated but exist in a constant volume, pressure and temperature environment variations in internal energy correspond to heat transfer (Q) between the biological system and its surroundings.
Q = ∆H ≈ ∆E (6)
Since the heat transfer from the system to the environment can be easily measured, this allows us to indirectly determine the variations in the internal energy of the system during a process. A release of heat corresponds to a decrease in internal energy, while adsorption of heat relates to an increase in internal energy.
Entropy The number of possible elementary configurations (microstates) that correspond to the observable state of a system (macrostate) is related to its entropy. The number of microstates
2

corresponding to the current macrostate (ω) is related to the entropy of the system by the following equation, where kB is the Boltzmann constant:
S = kB ln ω (7) At constant temperature the variation in entropy of the system can be related to its variation in
enthalpy and therefore to the heat exchanged with the environment:
∆S = ∆H = Q (8)
TT
From simple statistical considerations, it is evident how the entropy of any isolated system can only increase. This principle is described by the second law of thermodynamics.
Molecular features of biological interactions During protein folding the entropy of the protein itself decreases, since the conformational space that it can explore is reduced compared to the unfolded state. However, folding is still a spontaneous process thanks to the increase in entropy of the surrounding water molecules. The entropy of the solvent increases during folding since the exposed surface of the protein decreases and many water molecules are freed from forming an ordered cage-like solvation layer. Moreover, the formation of favorable Van der Waals and electrostatic interactions contributes to making also the enthalpy change associated with protein folding negative.
This example is explicative of a major motif in biological processes: the driving force of many biological events is the increase in entropy of water molecules of the solvent. During the binding of a ligand to a protein, the entropy of the protein-ligand system decreases, since the relative position of the two molecules becomes constrained. However, the entropy of the solvent increases since the water molecules that before the binding were solvating the interaction surfaces are expelled and can move freely in the solvent. 

### 1.2 Principles of protein interactions and binding site properties

In order to understand how proteins interact and form complexes with other molecules, we first need to stress that the ability of proteins to form biologically active complexes depends on their binding surfaces, and that at the same time these surfaces rely on few residues that make these interactions occur. 




This surface can bind an interactor thanks to its geometric compatibility and chemical properties. The shape of the interface is such to promote the close interaction of residues from the two partners. Interacting residues tend to have chemical properties that make the interaction favorable. For instance, hydrophobic regions tend to interact with hydrophobic regions of the partner, while oppositely charged residues can form salt bridges. From this broad description, it is already evident how processes that alter the geometric and chemical characteristics of a protein surface can also alter its interaction capabilities. This is the case for post-translational modifications and conformational changes.






The binding of ligands to proteins is generally driven by the hydrophobic effect (entropy decrease in the solvent) and by Van der Waals interactions. This is also supported by the observation that most protein-protein interaction surfaces are more hydrophobic than protein surfaces not involved in such interactions.
On the contrary, the specificity of binding is typically guided by electrostatic interactions such as
hydrogen bonds and salt bridges. These kinds of interactions are short-range and are typically
needed to achieve tight binding of the interactors. To maximize these interactions, the geometry of
binding sites tends to be highly specific. Opposing interacting surfaces tend to have a shape that
favors tight contact among atoms and places specific residues next to each other. This enhances the
hydrophobic effect due to the expulsion of water molecules and favors Van der Waals interactions
and electrostatic interactions among charged and polar residues. Protein-protein interaction (PPI)
surfaces tend to have a comparatively large area, and this area is related to the strength and
half-life of the complex. Low stability complexes have interface areas ranging from 1150 to 1200 Å2, 2
while the interfaces of more stable complexes can reach 2000 Å . Protein surfaces that mediate the interaction with small molecules tend to be smaller but deeply buried in the protein. Typical
2
The specificity of interaction can be mediated by loops of the protein that are supported by a conserved scaffold, like in antibodies. Low-specificity interaction surfaces are typical of interaction hubs: proteins that can interact with many different partners. When a protein can interact with many partners, these different interactors can all bind the same hydrophobic surface, or each of them can interact with a different cluster of residues. The energies involved in protein interactions can range from -2.5 to -22 kcal/mol. A summary of the energies associated with different interactions is reported in table 1.
binding pockets have an area of 300 to 1000 Å . Compared to binding pockets for small molecules, PPI surfaces tend to be flatter and less polar. They are typically highly conserved, especially in the central portion of the interface. Interfaces that mediate transient interactions are usually smaller, less planar and more polar than interfaces involved in tight binding. In homomultimeric complexes, the interaction interfaces tend to resemble the protein core in terms of hydrophobicity. The presence of some highly specific polar residues in interaction surfaces is essential in avoiding aggregation and for conferring specificity.
3

Interaction
Cofactors binding by enzymes Antibody-antigen Receptor-hormone Enzyme-inhibitor Enzyme-transition state
Affinity (kcal/mol)
−7.5 ± 2 −8 ± 3 −12 ± 3 −12 ± 3 −22 ± 5
 Table 1: Typical affinities for different types of protein interactions
The binding surfaces involved in PPIs are heterogeneous. The strength of protein interactions seems to be mostly due to the presence of certain discrete hydrophobic spots, more than to contacts across the entire interaction surface. These residues that provide most of the stabilization for the interaction are called as hotspots. An interaction hotspot is defined as a residue that, when replaced by alanine, causes a change in the interaction affinity of at least 2 kcal/mol. These hotspots tend to account for less than 50% of the interaction surface and are evolutionarily conserved. They usually appear in clusters and are typically constituted by large hydrophobic residues such as phenylalanine, tyrosine or tryptophan. Around these residues we can usually observe a cluster of less conserved hydrophobic residues that shield the hotspot from the solvent, leaving it available for interactions.

> ## References
> - Perkins, J. R., Diboun, I., Dessailly, B. H., Lees, J. G., & Orengo, C. (2010). Transient protein-protein interactions: structural, functional, and network p roperties. Structure, 18(10), 1233-1243.
> - Van Regenmortel, M. H. (2004), ‘Reductionism and complexity in molecular biology. Scientists now have the tools to unravel biological complexity and overcome the limitations of reductionism’, EMBO Reports 5(11), 1016–1020.
> 