# DataModel

This is the data model being built for the BIM4Ren project. This work is being used to
* list the data that are required to run the different services
* structure this data, linking concepts
* categorize concepts according to their domain of expertise
* identify concepts that are not present in current standards, in particular IFC4. This tasks is performed by aligning the concepts in the present data model with concepts in identified standards.

**Beware the model focuses only on residential buildings!**

The data model is made of the following different RDF files:

## buildings.rdf

Contains generic elements related to a basic description of a building. This work is inspired by the BOT ontology.
Typically, a building gets associated with a site, floors and spaces. Functionalities of some of the elements are produced through subclasses.
this the core ontology of the BIM4Ren ontology.


## buildingcomponents.rdf

*Dependency: buildings.rdf*

Contains elements of components of the building that as walls, windows...

## buildingsystems.rdf

Contains concepts related to HVAC, Domestic Hot Water, Lighting and domestic appliances.

## occupancy.rdf

*Dependency: buildings.rdf*

Contains concepts related to occupants, and their activities within the building. Activities are only modeled by schedules of occupancies in the building.

## energy.rdf

*Dependency: buildings.rdf, buildingcomponents.rdf, buildingsystems.rdf*

Models concepts relevant to build up an energy modeling of the building.
