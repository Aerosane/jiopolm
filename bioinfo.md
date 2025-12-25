# Bioinformatics Databases, File Formats, and Web Portals

## Table of Contents
1. [Classification of Databases](#classification-of-databases)
2. [Primary and Secondary Databases](#primary-and-secondary-databases)
3. [Specialized Databases](#specialized-databases)
4. [File Formats](#file-formats)
5. [Bioinformatics Web Portals](#bioinformatics-web-portals)
6. [Search Engines and Software Packages](#search-engines-and-software-packages)

---

## Classification of Databases

Biological databases are organized collections of biological data stored electronically.  They can be classified based on: 

| Classification Criteria | Types |
|------------------------|-------|
| **By Data Type** | Nucleotide, Protein, Structure, Pathway |
| **By Curation Level** | Primary (archival), Secondary (curated), Tertiary (specialized) |
| **By Scope** | General-purpose, Organism-specific, Domain-specific |

---

## Primary and Secondary Databases

### Nucleotide Databases

| Database | Organization | Description |
|----------|--------------|-------------|
| **GenBank** | NCBI (USA) | Primary nucleotide sequence database |
| **ENA** | EBI (Europe) | European Nucleotide Archive |
| **DDBJ** | NIG (Japan) | DNA Data Bank of Japan |

> These three form the **International Nucleotide Sequence Database Collaboration (INSDC)** and exchange data daily.

### Protein Databases

| Database | Type | Description |
|----------|------|-------------|
| **UniProt** | Primary/Secondary | Universal Protein Resource - comprehensive protein database |
| **PDB** | Structure | Protein Data Bank - 3D structural data |
| **CATH** | Classification | Class, Architecture, Topology, Homology classification |
| **SCOP** | Classification | Structural Classification of Proteins |

### Metabolic Pathway Database

- **KEGG (Kyoto Encyclopedia of Genes and Genomes)**: Integrates genomic, chemical, and systemic functional information

### Genome Variation Database

- **dbSNP**: Database of single nucleotide polymorphisms and other genetic variations

---

## Specialized Databases

| Database | Purpose |
|----------|---------|
| **RAP-DB** | Rice Annotation Project Database |
| **PDB** | Protein structure exploration and download |
| **MMDB** | Molecular Modeling Database |
| **MGD** | Mouse Genome Database |

---

## File Formats

### A. Sequence File Formats

#### GenBank Format
```
LOCUS       SCU49845     5028 bp    DNA     PLN       21-JUN-1999
DEFINITION  Saccharomyces cerevisiae TCP1-beta gene. 
ACCESSION   U49845
VERSION     U49845.1  GI:1293613
KEYWORDS    .
SOURCE      Saccharomyces cerevisiae
FEATURES             Location/Qualifiers
     source          1..5028
                     /organism="Saccharomyces cerevisiae"
ORIGIN
        1 gatcctccat atacaacggt atctccacct caggtttaga tctcaacaac
//
```

#### FASTA Format
```
>sequence_identifier description
ATGCGATCGATCGATCGATCGATCGATCGATCG
ATCGATCGATCGATCGATCGATCGATCGATCGA
```
- Simple, widely used format
- Header line starts with `>`
- Sequence follows on subsequent lines

#### FASTQ Format
```
@SEQ_ID
GATTTGGGGTTCAAAGCAGTATCGATCAAATAGTAAATCCATTTGTTCAACTCACAGTTT
+
! ''*((((***+))%%%++)(%%%%).1***-+*''))**55CCF>>>>>>CCCCCCC65
```
- Contains sequence AND quality scores
- Used for high-throughput sequencing data
- Quality scores encoded as ASCII characters

#### SAM/BAM Format

| Format | Description |
|--------|-------------|
| **SAM** | Sequence Alignment/Map - text format for aligned sequences |
| **BAM** | Binary version of SAM - compressed, indexed |

SAM Format Structure:
```
@HD VN:1.0 SO: coordinate
@SQ SN:chr1 LN:248956422
read001 0 chr1 100 60 50M * 0 0 ATCGATCG...  IIIIIIII... 
```

### B. ENA & NBRF Formats

- **ENA Format**: Similar to GenBank, used by European Nucleotide Archive
- **NBRF/PIR Format**:  Protein Information Resource format
```
>P1;SEQUENCE_ID
Description line
SEQUENCE*
```

### C. PDB File Format

```
HEADER    OXIDOREDUCTASE                          17-OCT-07   2VIM
TITLE     CRYSTAL STRUCTURE OF HUMAN HEMOGLOBIN
ATOM      1  N   ALA A   1      27.340  24.430   2.614  1.00  0.00           N
ATOM      2  CA  ALA A   1      26.266  25.413   2.842  1.00  0.00           C
ATOM      3  C   ALA A   1      26.913  26.639   3.531  1.00  0.00           C
END
```

| Record Type | Description |
|-------------|-------------|
| HEADER | Classification, date, ID code |
| TITLE | Descriptive title |
| ATOM | Atomic coordinates |
| HETATM | Non-standard residues |
| END | End of file marker |

---

## Bioinformatics Web Portals

### Brief Overview

| Portal | Organization | Primary Focus |
|--------|--------------|---------------|
| **NCBI** | National Center for Biotechnology Information (USA) | Comprehensive biological databases and tools |
| **EBI** | European Bioinformatics Institute (UK) | European hub for biological data |
| **ExPASy** | Swiss Institute of Bioinformatics | Proteomics and protein analysis |

---

# NCBI:  National Center for Biotechnology Information

## Comprehensive Detailed Guide

---

## 1. Introduction to NCBI

### 1.1 What is NCBI? 

The **National Center for Biotechnology Information (NCBI)** is a division of the **National Library of Medicine (NLM)** at the **National Institutes of Health (NIH)**, located in Bethesda, Maryland, USA.  Established in **1988**, NCBI serves as a critical national resource for molecular biology information.

### 1.2 Mission Statement

NCBI's mission is to: 
- Develop new information technologies to aid in understanding molecular and genetic processes
- Create automated systems for storing and analyzing biological data
- Enable researchers to access biomedical and genomic information
- Perform research in computational biology

### 1.3 Historical Background

| Year | Milestone |
|------|-----------|
| 1988 | NCBI established as part of NLM |
| 1990 | GenBank database transferred to NCBI |
| 1991 | BLAST search algorithm introduced |
| 1993 | World Wide Web access enabled |
| 1997 | PubMed launched for public access |
| 2000 | Human genome draft sequence integration |
| 2005 | dbGaP established for genotype-phenotype studies |
| 2007 | NCBI redesign with Entrez system enhancement |
| 2020+ | COVID-19 resources and pandemic data integration |

---

## 2. NCBI Organizational Structure

### 2.1 Divisions and Branches

```
NCBI
├── Computational Biology Branch
├── Information Engineering Branch
├── National Center for Biotechnology Information
├── Database and Program Development
└── Research Programs
```

### 2.2 Key Personnel Categories

- Bioinformatics Scientists
- Software Engineers
- Database Administrators
- Research Scientists
- Computational Biologists

---

## 3. NCBI Databases:  Complete Catalog

### 3.1 Nucleotide Sequence Databases

#### 3.1.1 GenBank

**Overview**: Primary NIH genetic sequence database containing annotated nucleotide sequences. 

| Feature | Description |
|---------|-------------|
| **Data Source** | Direct submissions, genome projects |
| **Update Frequency** | Daily |
| **Access Methods** | Entrez, BLAST, FTP |
| **Record Count** | 200+ million sequences |

**GenBank Divisions**:
| Division Code | Name | Description |
|---------------|------|-------------|
| PRI | Primate | Primate sequences |
| ROD | Rodent | Rodent sequences |
| MAM | Other Mammalian | Other mammalian sequences |
| VRT | Other Vertebrate | Non-mammalian vertebrates |
| INV | Invertebrate | Invertebrate sequences |
| PLN | Plant | Plant, fungal, algal sequences |
| BCT | Bacterial | Bacterial sequences |
| VRL | Viral | Viral sequences |
| PHG | Phage | Bacteriophage sequences |
| SYN | Synthetic | Synthetic and chimeric |
| UNA | Unannotated | Unannotated sequences |
| EST | EST | Expressed Sequence Tags |
| PAT | Patent | Patent sequences |
| STS | STS | Sequence Tagged Sites |
| GSS | GSS | Genome Survey Sequences |
| HTG | HTGS | High Throughput Genomic |
| HTC | HTC | High Throughput cDNA |
| ENV | Environmental | Environmental sampling |
| CON | Constructed | Constructed sequences |
| TSA | TSA | Transcriptome Shotgun Assembly |

#### 3.1.2 RefSeq (Reference Sequence Database)

**Purpose**: Provides curated, non-redundant reference sequences. 

**RefSeq Accession Prefixes**:
| Prefix | Molecule Type | Description |
|--------|---------------|-------------|
| NC_ | DNA | Complete genomic molecule (chromosome) |
| NG_ | DNA | Incomplete genomic region |
| NM_ | mRNA | Protein-coding transcript |
| NR_ | RNA | Non-protein-coding transcript |
| NP_ | Protein | Protein |
| XM_ | mRNA | Predicted model transcript |
| XP_ | Protein | Predicted model protein |
| XR_ | RNA | Predicted model non-coding transcript |
| WP_ | Protein | Non-redundant protein |
| YP_ | Protein | Protein encoded by genome |

**RefSeq Categories**:
```
┌─────────────────────────────────────────────┐
│              RefSeq Categories              │
├─────────────────────────────────────────────┤
│ Known (N_) - Experimentally validated       │
│ Model (X_) - Computationally predicted      │
│ Inferred (Y_) - Genome annotation derived   │
│ WGS Protein (W_) - Whole genome shotgun     │
└─────────────────────────────────────────────┘
```

#### 3.1.3 Nucleotide Database

- Combined database searchable through Entrez
- Includes GenBank, RefSeq, Third Party Annotation (TPA)
- Cross-referenced with other NCBI databases

#### 3.1.4 EST Database

**Expressed Sequence Tags**:
- Short single-read sequences from cDNA
- Useful for gene discovery
- Contains millions of ESTs from various organisms

#### 3.1.5 GSS Database

**Genome Survey Sequences**:
- Random genomic sequences
- Includes exon-trapped sequences
- Alu-PCR sequences
- Transposon-tagged sequences

### 3.2 Protein Databases

#### 3.2.1 Protein Database

| Component | Description |
|-----------|-------------|
| **GenPept** | Translations from GenBank nucleotide |
| **RefSeq Proteins** | Curated protein sequences |
| **SwissProt** | High-quality curated proteins |
| **PIR** | Protein Information Resource |
| **PDB** | Protein Data Bank sequences |
| **PRF** | Protein Research Foundation |

#### 3.2.2 Conserved Domains Database (CDD)

**Purpose**: Collection of sequence alignments and profiles representing protein domains.

**Sources Integrated**:
- Pfam
- SMART
- COG
- PRK
- TIGRFAM
- NCBIfam

**CDD Search Output Components**:
```
Query Sequence
    │
    ├── Superfamily hits
    │   └── Specific domain hits
    │
    ├── Multi-domain models
    │
    └── Conserved features
        ├── Active sites
        ├── Binding sites
        └── Other features
```

#### 3.2.3 Identical Protein Groups (IPG)

- Groups identical proteins from different sources
- Reduces redundancy in searches
- Links to source annotations

### 3.3 Structure Databases

#### 3.3.1 Structure (MMDB)

**Molecular Modeling Database**:
| Feature | Description |
|---------|-------------|
| **Source** | Derived from PDB |
| **Added Value** | Domain annotations, structural neighbors |
| **Visualization** | Cn3D viewer integration |
| **Links** | Sequence-structure relationships |

**MMDB Record Components**:
- 3D coordinates
- Chemical components
- Structural domains
- Conserved domains
- Related structures

#### 3.3.2 iCn3D

**Interactive Web-based 3D Structure Viewer**:
- Browser-based visualization
- Synchronizes with sequence
- Supports multiple representations
- Allows annotations and selections

### 3.4 Genome Databases

#### 3.4.1 Genome Database

**Content Types**:
| Type | Description |
|------|-------------|
| Complete Genomes | Fully sequenced and assembled |
| Chromosomes | Individual chromosome sequences |
| Scaffolds | Assembled contigs with gaps |
| Contigs | Continuous sequences |
| WGS Projects | Whole Genome Shotgun projects |

#### 3.4.2 Assembly Database

**Genome Assembly Information**:
- Assembly statistics
- Scaffold/contig metrics
- N50 values
- Gap information
- Assembly methods

**Assembly Levels**:
```
Complete Genome
      ↑
Chromosome Level
      ↑
Scaffold Level
      ↑
Contig Level
```

#### 3.4.3 Gene Database

**Gene-centric Information**:
| Data Type | Content |
|-----------|---------|
| Gene Symbol | Official nomenclature |
| Aliases | Alternative names |
| Description | Functional summary |
| Genomic Location | Chromosome, coordinates |
| Exon Structure | Exon/intron organization |
| Transcripts | RefSeq transcripts |
| Proteins | Encoded proteins |
| Expression | Expression profiles |
| Pathways | Associated pathways |
| Interactions | Gene/protein interactions |
| Phenotypes | Associated phenotypes |
| Orthologs | Orthologous genes |
| Bibliography | Related publications |

#### 3.4.4 HomoloGene

**Homology Detection System**:
- Automated detection of homologs
- Multiple organisms
- Curated groups
- Evolutionary analysis support

#### 3.4.5 GEO (Gene Expression Omnibus)

**Functional Genomics Repository**:
| Component | Description |
|-----------|-------------|
| GEO Datasets (GDS) | Curated gene expression datasets |
| GEO Profiles | Gene-centric expression profiles |
| GEO Series (GSE) | User-submitted experiment sets |
| GEO Samples (GSM) | Individual sample records |
| GEO Platforms (GPL) | Array/platform descriptions |

**Data Types Accepted**:
- Microarray data
- RNA-seq data
- ChIP-seq data
- Methylation data
- SNP arrays
- Other high-throughput data

### 3.5 Variation Databases

#### 3.5.1 dbSNP

**Single Nucleotide Polymorphism Database**: 

| Field | Description |
|-------|-------------|
| rs Number | Reference SNP cluster ID |
| Position | Genomic coordinates |
| Alleles | Observed alleles |
| MAF | Minor Allele Frequency |
| Validation | Validation status |
| Clinical | ClinVar associations |
| Frequency | Population frequencies |

**Variation Classes**:
- SNV (Single Nucleotide Variant)
- DIV (Deletion/Insertion Variant)
- MNV (Multi-Nucleotide Variant)
- STR (Short Tandem Repeat)

#### 3.5.2 dbVar

**Structural Variation Database**: 
- Copy number variants (CNVs)
- Insertions/Deletions (Indels)
- Inversions
- Translocations
- Complex rearrangements

#### 3.5.3 ClinVar

**Clinical Significance Database**: 

| Classification | Meaning |
|----------------|---------|
| Pathogenic | Causes disease |
| Likely pathogenic | Probably causes disease |
| Uncertain significance | Unknown clinical impact |
| Likely benign | Probably does not cause disease |
| Benign | Does not cause disease |

**ClinVar Record Contents**:
```
Variant Record
├── Variant details
├── Clinical interpretations
│   └── Submitter assertions
├── Conditions
├── Evidence
├── Review status (stars)
└── Related publications
```

#### 3.5.4 dbGaP (Database of Genotypes and Phenotypes)

**Purpose**: Archive of genotype-phenotype association studies.

**Access Levels**:
| Level | Description |
|-------|-------------|
| Open Access | Summary data, study descriptions |
| Controlled Access | Individual-level data (requires authorization) |

### 3.6 Literature Databases

#### 3.6.1 PubMed

**Biomedical Literature Database**:
- Over 35 million citations
- MEDLINE indexed
- Global biomedical literature coverage

**PubMed Record Components**:
| Field | Description |
|-------|-------------|
| PMID | PubMed unique identifier |
| Title | Article title |
| Authors | Author list |
| Abstract | Article summary |
| MeSH Terms | Medical Subject Headings |
| Keywords | Author keywords |
| DOI | Digital Object Identifier |
| Journal | Publication venue |

**Search Features**:
- Boolean operators (AND, OR, NOT)
- Field tags ([Title], [Author], etc.)
- MeSH term searching
- Phrase searching with quotes
- Truncation with asterisk
- Date range filtering

#### 3.6.2 PubMed Central (PMC)

**Full-Text Archive**:
- Free full-text articles
- NIH Public Access requirement compliance
- Publisher-deposited content
- Author manuscripts

#### 3.6.3 Bookshelf

**Online Books and Documents**:
- Textbooks
- NCBI handbooks
- Database documentation
- Reference works
- Gene reviews

### 3.7 Taxonomy Database

#### Taxonomy

**Organism Classification System**: 

| Rank | Example (Human) |
|------|-----------------|
| Superkingdom | Eukaryota |
| Kingdom | Metazoa |
| Phylum | Chordata |
| Class | Mammalia |
| Order | Primates |
| Family | Hominidae |
| Genus | Homo |
| Species | Homo sapiens |

**Taxonomy Record Contents**:
- Scientific name
- Common names
- Synonyms
- Lineage
- Genetic codes
- Division
- Statistics (sequences, proteins, genomes)

### 3.8 Chemical Databases

#### 3.8.1 PubChem

**Chemical Information Resource**: 

| Database | Content |
|----------|---------|
| **Compound** | Unique chemical structures |
| **Substance** | Deposited chemical records |
| **BioAssay** | Biological screening data |

**PubChem Compound Information**:
- 2D/3D structures
- Chemical properties
- Identifiers (CAS, InChI, SMILES)
- Biological activities
- Patent information
- Literature references

### 3.9 Biosystems and Pathways

#### BioSystems Database

**Integrated Pathway Information**:
- KEGG pathways
- Reactome
- BioCyc
- Gene Ontology

---

## 4. NCBI Search and Retrieval Tools

### 4.1 Entrez System

**Integrated Search and Retrieval**: 

**Entrez Databases Accessible**:
```
┌─────────────────────────────────────────┐
│            ENTREZ DATABASES             │
├─────────────────────────────────────────┤
│ Nucleotide  │ Protein    │ Structure   │
│ Gene        │ Genome     │ Taxonomy    │
│ PubMed      │ PMC        │ GEO         │
│ dbSNP       │ ClinVar    │ dbVar       │
│ BioProject  │ BioSample  │ SRA         │
│ Conserved   │ HomoloGene │ PubChem     │
│ Domains     │            │             │
└─────────────────────────────────────────┘
```

**Entrez Operators**:
| Operator | Function | Example |
|----------|----------|---------|
| AND | Both terms required | cancer AND p53 |
| OR | Either term | tumor OR tumour |
| NOT | Exclude term | cancer NOT lung |
| "" | Exact phrase | "breast cancer" |
| [field] | Restrict to field | p53[Gene Name] |
| * | Wildcard | immun* |

### 4.2 BLAST (Basic Local Alignment Search Tool)

**Purpose**:  Finds regions of local similarity between sequences. 

#### BLAST Programs: 

| Program | Query | Database | Purpose |
|---------|-------|----------|---------|
| **blastn** | Nucleotide | Nucleotide | Nucleotide-nucleotide comparison |
| **blastp** | Protein | Protein | Protein-protein comparison |
| **blastx** | Nucleotide (translated) | Protein | Translated nucleotide vs protein |
| **tblastn** | Protein | Nucleotide (translated) | Protein vs translated nucleotide |
| **tblastx** | Nucleotide (translated) | Nucleotide (translated) | All reading frames comparison |

#### Specialized BLAST: 
| Tool | Purpose |
|------|---------|
| **Megablast** | Highly similar sequences (fast) |
| **Discontiguous megablast** | Cross-species comparisons |
| **PSI-BLAST** | Position-specific iterated BLAST |
| **PHI-BLAST** | Pattern Hit Initiated BLAST |
| **DELTA-BLAST** | Domain Enhanced Lookup Time Accelerated BLAST |
| **Primer-BLAST** | Primer design with specificity check |
| **VecScreen** | Vector contamination detection |
| **IgBLAST** | Immunoglobulin analysis |

#### BLAST Output Interpretation: 

```
Query:  Your input sequence
       │
       ▼
┌─────────────────────────────────────────┐
│            BLAST RESULTS                │
├─────────────────────────────────────────┤
│ Graphic Summary                         │
│   [Color-coded alignment scores]        │
├─────────────────────────────────────────┤
│ Descriptions                            │
│   Accession | Description | Score | E   │
├─────────────────────────────────────────┤
│ Alignments                              │
│   Query  1 ATGCGATCG...    50           │
│            |||||||||                    │
│   Sbjct  1 ATGCGATCG...   50           │
└─────────────────────────────────────────┘
```

**Key BLAST Statistics**:
| Statistic | Meaning |
|-----------|---------|
| **Score** | Bit score, alignment quality |
| **E-value** | Expected number of chance alignments |
| **Identity** | Percentage of identical matches |
| **Positives** | Similar amino acids (protein) |
| **Gaps** | Number of gaps introduced |
| **Query cover** | Percentage of query aligned |

### 4.3 Primer-BLAST

**Primer Design Tool**: 
- Designs primers using Primer3
- Checks specificity using BLAST
- Detects potential amplification targets
- Supports various PCR applications

### 4.4 ORFfinder

**Open Reading Frame Finder**:
- Identifies potential ORFs in nucleotide sequences
- Multiple genetic code support
- Variable minimum ORF length
- Links to BLAST for analysis

### 4.5 CD-Search

**Conserved Domain Search**: 
- Identifies conserved domains in proteins
- Uses RPS-BLAST algorithm
- Multiple database searching
- Domain architecture analysis

### 4.6 Cn3D / iCn3D

**3D Structure Viewers**:
| Feature | Cn3D | iCn3D |
|---------|------|-------|
| Platform | Desktop (download) | Web browser |
| Alignment view | Yes | Yes |
| Sequence sync | Yes | Yes |
| Annotations | Yes | Enhanced |
| Sharing | File export | URL sharing |

---

## 5. NCBI Data Submission

### 5.1 Submission Portals

| Portal | Data Type |
|--------|-----------|
| **BankIt** | GenBank sequences (web) |
| **tbl2asn** | GenBank (command-line) |
| **Sequin** | GenBank (desktop, discontinued) |
| **Submission Portal** | Unified submission system |
| **GEO** | Expression data |
| **SRA** | Sequence read data |

### 5.2 BioProject

**Project Registration**:
- Umbrella for related data
- Links samples, sequences, publications
- Required for many submissions

### 5.3 BioSample

**Sample Metadata**:
- Describes biological source
- Standardized attributes
- Links to sequence data

### 5.4 Sequence Read Archive (SRA)

**Raw Sequencing Data Repository**:
| Data Type | Accepted |
|-----------|----------|
| Illumina | Yes |
| PacBio | Yes |
| Oxford Nanopore | Yes |
| Ion Torrent | Yes |
| 454 | Yes |
| SOLiD | Yes |

---

## 6. NCBI Programmatic Access

### 6.1 E-utilities (Entrez Programming Utilities)

**API Access to NCBI Databases**:

| Utility | Function |
|---------|----------|
| **EInfo** | Database statistics and field info |
| **ESearch** | Text searches, returns UIDs |
| **EPost** | Upload UID list to server |
| **ESummary** | Document summaries |
| **EFetch** | Retrieve records in various formats |
| **ELink** | Related records in same/other databases |
| **EGQuery** | Global Query, counts across databases |
| **ESpell** | Spelling suggestions |

**E-utilities Base URL**:
```
https://eutils.ncbi.nlm.nih. gov/entrez/eutils/
```

**Example API Calls**:

ESearch for a gene:
```
https://eutils.ncbi.nlm. nih.gov/entrez/eutils/esearch.fcgi?db=gene&term=p53[Gene+Name]+AND+human[Organism]
```

EFetch to retrieve GenBank record:
```
https://eutils.ncbi.nlm. nih.gov/entrez/eutils/efetch.fcgi?db=nucleotide&id=NM_000546&rettype=gb&retmode=text
```

### 6.2 NCBI Datasets

**Command-line Tool for Genomic Data**:

Installation:
```bash
curl -o datasets 'https://ftp.ncbi.nlm.nih. gov/pub/datasets/command-line/LATEST/linux-amd64/datasets'
chmod +x datasets
```

Usage Examples:
```bash
# Download human genome
datasets download genome accession GCF_000001405.40

# Download gene data
datasets download gene gene-id 7157

# Get virus genomes
datasets download virus genome taxon SARS-CoV-2
```

### 6.3 EDirect

**Command-line E-utilities**: 

```bash
# Install
sh -c "$(curl -fsSL https://ftp.ncbi. nlm.nih.gov/entrez/entrezdirect/install-edirect.sh)"

# Example:  Search and fetch
esearch -db nucleotide -query "BRCA1 [Gene] AND human [Organism]" | efetch -format fasta

# Pipeline example
esearch -db pubmed -query "CRISPR" | elink -target gene | efetch -format docsum
```

### 6.4 FTP Access

**Direct Data Download**:
```
ftp://ftp.ncbi.nlm. nih.gov/
├── blast/         # BLAST databases
├── genbank/       # GenBank flat files
├── gene/          # Gene data
├── genomes/       # Genome assemblies
├── pub/           # Publications and tools
├── refseq/        # RefSeq data
├── snp/           # dbSNP data
├── sra/           # SRA data
└── taxonomy/      # Taxonomy database
```

---

## 7. NCBI Tools and Software

### 7.1 BLAST+ Suite

**Local BLAST Installation**: 

**Programs Included**:
| Program | Description |
|---------|-------------|
| blastn | Nucleotide-nucleotide BLAST |
| blastp | Protein-protein BLAST |
| blastx | Translated nucleotide-protein |
| tblastn | Protein-translated nucleotide |
| tblastx | Translated-translated |
| makeblastdb | Create BLAST databases |
| blastdbcmd | Query BLAST databases |

### 7.2 SRA Toolkit

**Commands**:
| Tool | Purpose |
|------|---------|
| fastq-dump | Convert SRA to FASTQ |
| fasterq-dump | Faster FASTQ conversion |
| prefetch | Download SRA files |
| vdb-validate | Validate SRA files |

### 7.3 Genome Workbench

**Desktop Application**:
- Integrated genome analysis
- Visualization tools
- Sequence editing
- Multiple alignment
- Tree building

### 7.4 Magic-BLAST

**RNA-seq Mapping**:
- Optimized for RNA-seq data
- Splice-aware alignment
- SRA integration

---

## 8. Using NCBI:  Practical Guide

### 8.1 Common Workflows

#### Finding a Gene

```
1. Go to NCBI homepage (ncbi.nlm.nih.gov)
2. Select "Gene" database
3. Enter gene name/symbol
4. Filter by organism if needed
5. Click on gene record
6. Explore: 
   - Summary
   - Genomic context
   - Transcripts
   - Expression
   - Bibliography
```

#### Sequence Similarity Search

```
1. Navigate to BLAST page
2. Select appropriate program
3. Enter query sequence or accession
4. Choose target database
5. Adjust parameters if needed
6. Submit and analyze results
```

#### Downloading Genome Data

```
1. Go to NCBI Datasets
   OR
2. Use Assembly database
3. Search for organism
4. Select assembly
5. Download via: 
   - Web interface
   - FTP
   - datasets CLI
```

### 8.2 Tips for Effective Searching

**Search Strategies**:
| Strategy | Example |
|----------|---------|
| Use field qualifiers | p53[Gene Name] |
| Combine terms | BRCA1 AND breast cancer |
| Use filters | 2023: 2024[Date - Publication] |
| Limit by organism | human[Organism] |
| Use MeSH terms | "Neoplasms"[MeSH] |

### 8.3 Linking Between Databases

**Cross-Database Navigation**:
- Use "Links" menu in records
- Related sequences
- Related structures
- Related publications
- Related genes
- Cited by articles

---

## 9. NCBI Learning Resources

### 9.1 Documentation

| Resource | URL |
|----------|-----|
| NCBI Handbook | ncbi.nlm. nih.gov/books/NBK143764/ |
| Help Documentation | ncbi.nlm. nih.gov/home/learn/ |
| YouTube Channel | youtube.com/ncaboregon |
| Twitter | @ABORNCBI |

### 9.2 Training Materials

- Online tutorials
- Webinars
- Workshop materials
- Video tutorials
- Quick start guides

---

## 10. NCBI Statistics and Facts

### Current Database Statistics (Approximate)

| Database | Size |
|----------|------|
| GenBank sequences | 200+ million |
| RefSeq genomes | 100,000+ |
| PubMed citations | 35+ million |
| Gene records | 20+ million |
| dbSNP variants | 700+ million |
| SRA experiments | 20+ million |
| GEO samples | 4+ million |

### Daily Usage

- Millions of web searches daily
- Billions of BLAST queries annually
- Petabytes of data served

---

## 11. Key NCBI URLs

| Resource | URL |
|----------|-----|
| Main Portal | https://www.ncbi.nlm. nih.gov |
| BLAST | https://blast.ncbi.nlm.nih. gov |
| PubMed | https://pubmed.ncbi.nlm. nih.gov |
| Gene | https://www.ncbi.nlm. nih.gov/gene |
| GenBank | https://www.ncbi.nlm.nih. gov/genbank |
| RefSeq | https://www.ncbi.nlm.nih.gov/refseq |
| GEO | https://www.ncbi.nlm.nih.gov/geo |
| SRA | https://www.ncbi.nlm. nih.gov/sra |
| dbSNP | https://www.ncbi.nlm. nih.gov/snp |
| ClinVar | https://www.ncbi.nlm.nih. gov/clinvar |
| Datasets | https://www.ncbi.nlm.nih. gov/datasets |
| E-utilities | https://www.ncbi.nlm.nih. gov/books/NBK25501/ |
| FTP | https://ftp.ncbi. nlm.nih.gov |

---

## Brief on Other Bioinformatics Web Portals

### B. EBI (European Bioinformatics Institute)

- Part of EMBL (European Molecular Biology Laboratory)
- Located in Hinxton, Cambridge, UK
- Major databases: ENA, UniProt, Ensembl, ArrayExpress, PDBe
- Key tools: BLAST, Clustal Omega, InterProScan

### C. ExPASy (Expert Protein Analysis System)

- Swiss Institute of Bioinformatics portal
- Focus on proteomics and protein analysis
- Key tools: ProtParam, PROSITE, SWISS-MODEL
- Hosts UniProt/Swiss-Prot

---

## Search Engines and Software Packages

### Bioinformatics Search Engines

| Tool | Purpose |
|------|---------|
| BLAST | Sequence similarity search |
| HMMER | Profile hidden Markov models |
| FASTA | Sequence database searching |
| BLAT | Genome BLAST-like tool |

### Common Software Packages

| Package | Purpose |
|---------|---------|
| Biopython | Python library for bioinformatics |
| Bioperl | Perl toolkit for biology |
| BioJava | Java framework for biology |
| R/Bioconductor | Statistical genomics |
| Galaxy | Web-based analysis platform |
| ClustalW/Omega | Multiple sequence alignment |
| MEGA | Molecular Evolutionary Genetics Analysis |
| Cytoscape | Network visualization |
| IGV | Integrative Genomics Viewer |
| SAMtools | SAM/BAM file manipulation |
| BWA | Burrows-Wheeler Aligner |
| GATK | Genome Analysis Toolkit |

---

## References and Further Reading

1.  NCBI Resource Coordinators. "Database resources of the National Center for Biotechnology Information." Nucleic Acids Research (Annual Database Issue)

2. Sayers EW, et al. "Database resources of the National Center for Biotechnology Information." Nucleic Acids Research.  2022. 

3. NCBI Handbook [Internet].  Bethesda (MD): National Center for Biotechnology Information (US).

4. Altschul SF, et al. "Basic local alignment search tool." J Mol Biol. 1990. 

5. Coordinators NR. "Database Resources of the National Center for Biotechnology Information." Nucleic Acids Research. 2023.

---

*Document prepared for educational purposes*
*Last updated: December 2025*
