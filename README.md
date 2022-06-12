# Hybrid de novo genome assemblies of Kazakh individuals

![Assemblies_workflow](https://user-images.githubusercontent.com/56155720/173247760-0d7cd3d3-3946-4540-be84-f383c53bfa46.png)

This repository accompanies the manuscript "Hybrid de novo genome assemblies of Kazakh individuals" by Daniyar Karabayev, Asset Daniyarov, Saule Rakhimova, Diana Samatkyzy, Askhat Molkenov, Ainur Akilzhanova, and Ulykbek Kairov. The code used to generate the assemblies can be found in `scripts/`

## Quick start

For primary de-novo assembly of ONT long reads `Flye` and `Shasta` tools were used. The primary assemly then need to be polished either with short reads (sr) from NGS or with long reads (lr) that were used for the primary assembly. For the first round of polishing (sr polishing or lr polishing) `Racon` was used, while `Medaka` was used for the second round of lr polishing. Alternatively, we tested `Hypo` for the hybrid polishing (sr + lr polishing).

For Flye + Racon + Medaka assemblies, use `/scripts/assembly_flye`

For Shasta + Racon + Medaka assemblies, use  `/scripts/assembly_shasta`

If you want to use Hypo instead of Racon + Medaka, use `/scripts/assembly_flye_hypo` or `/scripts/assembly_shasta_hypo`.

Please, make sure that all required tools are installed in your conda environment and all paths used in the scripts are valid 