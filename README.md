# ALCDog: defeasible OWL ontology generator for ALC

A simple, parameterised defeasible OWL ontology generator for ALC.

#### Usage

```
java -jar ALCDog-${version}-jar-with-dependencies.jar #ontologies #axioms #namedclasses #objectproperties #individuals %defeasibility
```

Parameters:

+ #ontologies - number of ontologies to generate e.g. 10
+ #axioms - number of axioms to generate in each ontology e.g. 100
+ #namedclasses - number of class names to use to generate each ontology e.g. 20
+ #objectproperties - number of object properties or roles to use to generate each ontology e.g. 10
+ #individuals - number of individuals to use in the generation of ABox assertions in each ontology e.g. 100
+ %defeasibility - percentage number of subsumptions in each ontology that would like to be defeasible. Integer between 0 and 100 e.g. 20

#### Fine-grained parameters

+ Finer-grained parameters of this generator such as the frequency distribution of different ALC features in the ontology, nesting depth of complex concepts, length of conjunctions and disjunctions etc. are fixed and and calculated by analysing the shape and structure of existing OWL ontologies in the [Manchester OWL repository](http://mowlrepo.cs.manchester.ac.uk/) in 2014-2015 when my PhD was written.
+ More details can be found in Chapter 6 of my [thesis](https://drive.google.com/file/d/0B35nGJosYOkGMGRJMGZhREJ5U0U/view).

#### Prepared test data

Pre-generated test data that I generated for my [PhD](https://drive.google.com/file/d/0B35nGJosYOkGMGRJMGZhREJ5U0U/view) evaluation:

+ Synthetic data generated using this tool is available [here](https://drive.google.com/open?id=0B35nGJosYOkGZlhvZURwV2pDZUE). 
+ Nonsynthetic defeasible ontologies are also available [here](https://drive.google.com/open?id=0B35nGJosYOkGcFNoRFptS3RScGM). These ontologies began as incoherent ontologies from the [Manchester OWL repository](http://mowlrepo.cs.manchester.ac.uk/) and the methodology used to introduce defeasible subsumptions into these ontologies is described in [this paper](http://iswc2015.semanticweb.org/sites/iswc2015.semanticweb.org/files/93670351.pdf) and in Chapter 6 of my [thesis](https://drive.google.com/file/d/0B35nGJosYOkGMGRJMGZhREJ5U0U/view).

#### Building source

Steps:

1. Get a copy of the code:

        git clone https://github.com/kodymoodley/defeasible-owl-ontologies.git
    
2. Change into the defeasible-owl-ontologies directory.

3. Type mvn clean package. On build completion, the "target" directory will contain a ALCDog-${version}-jar-with-dependencies.jar file.

#### License

[GNU General Public License](https://www.gnu.org/licenses/gpl-3.0.en.html)
