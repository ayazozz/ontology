# ontology-Project
Ontology of trees growing in a special region


## SUMMARY

This proje is the ontology of trees that grow in a special area.It includes classes of tree, soil, climate and region.This ontology keeps the soil type, climate information of the cities in the region.At the same time, keeps climate and soil types information that trees grow.
Finally, the ontology makes the inference that "which tree will grow more efficiently in which city" according to rules.

## 
You can look at rules as follows:

![ekran goruntusu 3](https://user-images.githubusercontent.com/38051809/38275386-61dae176-379a-11e8-8ae3-85231faea1e4.png)

## EXAMPLE SPARQL QUERY

Firstly, you have to import your ontology link on query page.For example; myOntology
1-Trees growing on laterite soil

SELECT ?Tree
WHERE { ?Tree myOntology:planting myOntology:Lateritte_Soil .}

![image1](https://user-images.githubusercontent.com/38051809/38276641-4d5a4576-379e-11e8-812f-325c183d427f.png)

2-Trees over 30 meters in height

SELECT ?Tree ?Height
WHERE { ?Tree  myOntology:Height?Height .
      FILTER(?Height > "29.57"^^<http://www.w3.org/2001/XMLSchema#double>) .}

![image2](https://user-images.githubusercontent.com/38051809/38276869-19b37160-379f-11e8-8cd9-8b28796b200a.png)
