# SingleCell_tools

Enrichment

| First Header  | Second Header |
| ------------- | ------------- |
| ClusterProfiler  | enrichGO, enrichKEGG |
| PPI network | STRING, Cytoscape, CytoHubba, MCODE |
| Content Cell  | Content Cell  |
| Content Cell  | Content Cell  |
| Content Cell  | Content Cell  |
| Content Cell  | Content Cell  |
| Content Cell  | Content Cell  |
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
7. colleiono i miRNA faccio text mining  in pubmed usando il mammalian NcRNA-disease repository (MNDR) con uno score maggiore di 0.7, lo human microRNA disease database (HMDD) e il miR2disease database.
8. per ottenere la relazione regolatoria tra TF e miRNA, TF con geni e miRNA con mRNA, trovo le informazioni da chIPBase e starBase. mantengo come significativi le relazioni supportate da almeno 5 esperimenti.
