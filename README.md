# SingleCell_tools

Enrichment

| First Header  | Second Header |
| ------------- | ------------- |
| ClusterProfiler  | enrichGO, enrichKEGG |
| PPI network | STRING, Cytoscape, CytoHubba, MCODE |
| Content Cell  | mammalian NcRNA-disease repository (MNDR)  |
| Content Cell  | human microRNA disease database (HMDD)  |
| Content Cell  | miR2disease database  |
| Content Cell  | chIPBase e starBase  |
| SNP analysis of DEGs | SCAN database (scandb.org) |
| Content Cell  | Content Cell  |
| Content Cell  | Content Cell  |
| Content Cell  | Content Cell  |
| Content Cell  | Content Cell  |
| Content Cell  | Content Cell  |
| Content Cell  | Content Cell  |
| Content Cell  | Content Cell  |


1. trovo i degs
2. costruisco il network di interazione con STRING e tengo solo le interazioni con uno score combinato maggiore di 0.4
3. costruisco il network di interazione con Cytoscape
4. misuro i nodi tramite le i loro score delle network features per inferire la loro importanza nel network e identifico gli elementi centrali del network. ottengo i nodi significativi e i geni hub nel network PPI usando CytoHubba il quale ranka i nodi tramite le loro features. i nodi con grado maggiore sono considerati come significativi.
5. uso MCODE (molecular complez detection) per fare uno screen dei moduli del network.
6. per esplorare le relzioni regolatorie e identificare i fattori di rischio costruisco il network reglatorio TF-miRNA-mRNA dei geni hub e dei miRNAs.
7. colleziono i miRNA faccio text mining  in pubmed usando il mammalian NcRNA-disease repository (MNDR) con uno score maggiore di 0.7, lo human microRNA disease database (HMDD) e il miR2disease database.
8. per ottenere la relazione regolatoria tra TF e miRNA, TF con geni e miRNA con mRNA, trovo le informazioni da chIPBase e starBase. mantengo come significativi le relazioni supportate da almeno 5 esperimenti.
9. SNPs associati ad MS ottenuti tramite il database SCAN (SNP and copy number annotation database). vengono scelti solo quelli con frequenza maggiore di 0.10.
10. per identificare solo gli SNPs biologicamente significativi, questi vengono lanciati nel MirSNP database. questo aiuta a trovare gli SNPs presenti nel 3' UTR dei siti target dei miRNA. la mutione di questi SNPs può affliggere il binding dei miRNA ai tagrte genes affliggendo l'espressione dei geni corrispondenti. con la lista dei miRNAs legati ad MS, identifico gli SNPs più rilevanti che possono essere usati per screening successivi.
