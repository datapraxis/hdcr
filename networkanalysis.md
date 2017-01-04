#Humanities Data Curation
##Network Graphs & Network Analysis
###The Basics

The primary issues for network analysis datasets are selecting a data format and filetype that’s widely accessible, and annotating and documenting the data. Because network analysis is highly dependent upon software packages for both visualization and analysis, file format interoperability is essential to the integrity of the dataset.

Network data can come in a wide range of formats, all with their own affordances, contingencies, and visual and descriptive information. Most of the time, the underlying data is held in two tabular data files, though some may use matrices or numerous tabular data files. Network graphs can be produced in a number of different formats, ranging from static .jpg and .png to dynamic .svg to more complex GraphML or GML formats that can carry a great amount of additional data for later manipulation.

It’s best to start with good curation practices in mind as you’re gathering and refining your data. If you’ve already started, don’t worry, it’s not too late to implement positive curation practices.

###Documentation

When developing a model in the humanities, sources that are objective, continuous, and “fuzzy,” must be made discrete. While doing this, it’s essential to document these decisions, or the methodology that informs them, in order to make the dataset widely usable the the present and in the future.

Data should include citations and an explanation of decisions about categorization, and any processing processing that occurs are essential for the trustworthy use and reuse of your data by others.These decisions must occur constantly with humanities data analysis, and these decisions have implications on the data and the results of the analysis, and cannot be ignored. This documentation is especially important for network analysis because network graphs are models that are necessarily limited. The documentation of these limitations is key to evaluation, verification, and reuse.

Network measurements may vary between different software packages, and each makes different assumptions about your data. Many tools also run random measurements over the data, and, by nature of the algorithm, will return slightly different metrics each time they are run. Understanding the purpose, strengths, and weaknesses of these measurements is key to your analysis, and the documentation of the algorithm is also key to the veracity of your dataset.

###Data Types
*Note: These recommendations are based on the use of Cytoscape, Gephi, NodeXL, Sci2, D3.js, igraph (R and Python).*

Network data is often represented in matrices, adjacency lists, and/or node/edge lists. Matrices may not be the best option for data curation, as data annotation is limited. Matrices are becoming less popular, and fewer software platforms may support their usage in the future. Adjacency lists are slightly more common and are widely readable by graphing platforms, but offers data annotation for edges only.

For the purposes of data curation (not to mention outside factors, such as scalability and ease of data entry), node/edge lists are strongly recommended. The node/edge list format is widely used, readable by every major network analysis software platform used by humanists, and allows for complete extensibility of data annotation, for both edges and nodes.

**Preferred data format:**

- two or more files of tabular data - lists of nodes and edges
- lists should have column descriptors with clear semantic meaning, with further details illustrated in either the tabular data or in a codebook

###File Formats

It may be a good idea to make network data available in a few different formats. Research products may include not only a network dataset, but also graphs that illustrate different measurements and subsets.

####Native data

**Delimited text (CSV, TSV, etc.)** files support the underlying data of a network, but will not support many of the aesthetics of a graph. However, because the CSV is a foundational data format, it is highly likely that your data will be recognized by nearly any software platform now or in the future. CSV format also brings the benefit of further data visualization and manipulation by other software packages. The native dataset should include the node and edge list, as well as measurements (centrality, Eigenvector, etc.) and any documentation that is available. It is strongly recommended that the underlying data is saved in CSV, in addition to other formats that may better represent the graph structures and visualizations obtained from the data.

####Graphs

**GraphML** is an open, XML-based format that defines a graph, including the connections between the nodes and coloring, if applicable. There is also space for an application to add data that may only be usable for that particular application.

Further reading: [http://graphml.graphdrawing.org/index.html](http://graphml.graphdrawing.org/index.html)

**GML** (Graph Modelling Language) is an ASCII-based format that describes graph data in hierarchical key-value lists. GML was created to serve as an interchange between various graphing software systems, so it is flexible and extensible, and allows for arbitrary annotation of the graph data. GML supports specific aesthetic features, such as node location, as well as other data annotation, although there is no guarantee that all annotations will be recognized or utilized by all applications.

Further reading: [*http://www.fim.uni-passau.de/fileadmin/files/lehrstuhl/brandenburg/projekte/gml/gml-technical-report.pdf*](http://www.fim.uni-passau.de/fileadmin/files/lehrstuhl/brandenburg/projekte/gml/gml-technical-report.pdf)

**PNG** is a raster image format that’s often used for the capture of information visualization. It represents a frozen snapshot of the graph that is not easily manipulated or customized after it has been produced.

**SVG** is an XML-based image format for capturing (relatively) static images of all or part of a graph. SVG is probably the best option for this type of capture, because its XML foundation makes it trustworthy in
the long run, and also allows for some simple aesthetic modifications to be made using Javascript.

---
*Humanities Data Curation Record*  
Brandon Locke  
CC-BY 4.0
