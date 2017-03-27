# Humanities Data Curation
## Network Graphs & Network Analysis
### The Basics

Network data come in a wide range of formats, all with their own affordances, contingencies, and visual and descriptive information.  Network graphs can be produced in a number of different formats, ranging from static .jpg and .svg to the more complex GraphML format. Because network analysis is highly dependent upon software packages for both visualization and analysis, file format interoperability is essential to reuse.

### Documentation

When developing a model in the humanities, sources that are subjective, continuous, and “fuzzy,” must be made discrete. Decisions and the methodology that informs them must be documented in order to make the dataset reviewable and widely usable. This documentation is especially important for network analysis because network graphs are models that are necessarily limited. Documentation is key to evaluating their integrity.

Network measurements may vary between different software packages, and each makes different assumptions about your data. Many tools also run random measurements over the data, and, by nature of the algorithm, will return slightly different metrics each time they are run. Understanding the purpose, strengths, and weaknesses of these measurements is key to  data produced by them.

### Data Types
*Note: These recommendations are based on the use of Cytoscape, Gephi, NodeXL, Sci2, D3.js, igraph (R and Python).*

Network data are often represented in matrices, adjacency lists, and/or node/edge lists. Data annotation of matrices is limited. Matrices are becoming less popular, and fewer software platforms may support their use in the future. Adjacency lists are slightly more common and are widely readable by graphing platforms, but offer data annotation for edges only.

For the purposes of data curation of scalability, ease of data entry, and long term access, node/edge lists are strongly recommended. The node/edge list format is widely used, readable by every major network analysis software platform used by humanists, and allows for edge and node annotation.

**Preferred data format:**

- two or more files of tabular data - lists of nodes and edges
- lists should have column descriptors with clear semantic meaning, with further details illustrated in either the tabular data or in a codebook

### File Formats

It may be a good idea to make network data available in a few different formats. Research products will likely include the underlying network dataset in addition to graphs that illustrate different measurements and subsets.

#### Native data

**Delimited text (CSV, TSV, etc.)** files support the underlying data of a network, but will not support many of the aesthetics of a graph. However, because the CSV is a foundational data format, it is highly likely that your data will be recognized by all software platforms now and in the future. CSV format also brings the benefit of further data visualization and manipulation by other software packages. The native dataset should include the node and edge list, as well as measurements (centrality, Eigenvector, etc.) and any documentation that is available. 

*It is strongly recommended that the underlying data is saved in CSV, in addition to other formats that may better represent the graph structures and visualizations obtained from the data.*

#### Graphs

**GraphML** is an open, XML-based format that defines a graph, including the connections between the nodes and coloring, if applicable. There is also space for an application to add data that may only be usable for that particular application.

Further reading: [http://graphml.graphdrawing.org/index.html](http://graphml.graphdrawing.org/index.html)

**GML** (Graph Modelling Language) is an ASCII-based format that describes graph data in hierarchical key-value lists. GML was created to serve as an interchange between various graphing software systems, so it is flexible and extensible, and allows for arbitrary annotation of the graph data. GML supports specific aesthetic features, such as node location, as well as other data annotation, although there is no guarantee that all annotations will be recognized or utilized by all applications.

Further reading: [*http://www.fim.uni-passau.de/fileadmin/files/lehrstuhl/brandenburg/projekte/gml/gml-technical-report.pdf*](http://www.fim.uni-passau.de/fileadmin/files/lehrstuhl/brandenburg/projekte/gml/gml-technical-report.pdf)

**PNG** is a raster image format that’s often used for the capture of information visualization. It represents a frozen snapshot of the graph that is not easily manipulated or customized after it has been produced.

**SVG** is an XML-based image format for capturing (relatively) static images of all or part of a graph. SVG is probably the best option for this type of capture, because its XML foundation makes it trustworthy in the long run, and also allows for some simple aesthetic modifications to be made using Javascript.

---
*Humanities Data Curation Record*  
Brandon Locke  
CC-BY 4.0
