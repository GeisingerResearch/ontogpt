# reaction Template

A template for reactions

URI: https://w3id.org/ontogpt/reaction
Name: reaction-template



## Schema Diagram

```mermaid
erDiagram
Reaction {
    string label  
    string description  
    stringList synonyms  
    string id  
}
GeneToReaction {

}
ReactionDocument {

}
GeneReactionPairing {

}
ReactionGrouping {
    string id  
    string label  
}
ChemicalEntity {
    string id  
    string label  
}
Evidence {
    string id  
    string label  
}
Gene {
    string id  
    string label  
}
Organism {
    string id  
    string label  
}
Any {

}
ExtractionResult {
    string input_id  
    string input_title  
    string input_text  
    string raw_completion_output  
    string prompt  
}
NamedEntity {
    string id  
    string label  
}
CompoundExpression {

}
Triple {
    string qualifier  
}
TextWithTriples {

}
RelationshipType {
    string id  
    string label  
}
Publication {
    string id  
    string title  
    string abstract  
    string combined_text  
    string full_text  
}
AnnotatorResult {
    string subject_text  
    string object_id  
    string object_text  
}

Reaction ||--|o ReactionGrouping : "subclass_of"
Reaction ||--}o ChemicalEntity : "left_side"
Reaction ||--}o ChemicalEntity : "right_side"
GeneToReaction ||--|o Gene : "gene"
GeneToReaction ||--}o Reaction : "reactions"
GeneToReaction ||--|o Organism : "organism"
ReactionDocument ||--}o Gene : "genes"
ReactionDocument ||--}o Reaction : "reactions"
ReactionDocument ||--}o GeneReactionPairing : "gene_reaction_pairings"
ReactionDocument ||--|o Organism : "organism"
ReactionDocument ||--}o Evidence : "has_evidence"
GeneReactionPairing ||--|o Gene : "gene"
GeneReactionPairing ||--|o Reaction : "reaction"
ExtractionResult ||--|o Any : "extracted_object"
ExtractionResult ||--}o Any : "named_entities"
Triple ||--|o NamedEntity : "subject"
Triple ||--|o RelationshipType : "predicate"
Triple ||--|o NamedEntity : "object"
Triple ||--|o NamedEntity : "subject_qualifier"
Triple ||--|o NamedEntity : "object_qualifier"
TextWithTriples ||--|o Publication : "publication"
TextWithTriples ||--}o Triple : "triples"

```


## Classes

| Class | Description |
| --- | --- |
| [AnnotatorResult](AnnotatorResult.md) |  |
| [Any](Any.md) |  |
| [ChemicalEntity](ChemicalEntity.md) |  |
| [CompoundExpression](CompoundExpression.md) |  |
| [Evidence](Evidence.md) |  |
| [ExtractionResult](ExtractionResult.md) | A result of extracting knowledge on text |
| [Gene](Gene.md) |  |
| [GeneReactionPairing](GeneReactionPairing.md) |  |
| [GeneToReaction](GeneToReaction.md) |  |
| [NamedEntity](NamedEntity.md) |  |
| [Organism](Organism.md) |  |
| [Publication](Publication.md) |  |
| [Reaction](Reaction.md) |  |
| [ReactionDocument](ReactionDocument.md) |  |
| [ReactionGrouping](ReactionGrouping.md) |  |
| [RelationshipType](RelationshipType.md) |  |
| [TextWithTriples](TextWithTriples.md) |  |
| [Triple](Triple.md) | Abstract parent for Relation Extraction tasks |


## Slots

| Slot | Description |
| --- | --- |
| [abstract](abstract.md) | The abstract of the publication |
| [combined_text](combined_text.md) |  |
| [description](description.md) | a textual description of the reaction |
| [extracted_object](extracted_object.md) | The complex objects extracted from the text |
| [full_text](full_text.md) | The full text of the publication |
| [gene](gene.md) | name of the gene that catalyzes the reaction |
| [gene_reaction_pairings](gene_reaction_pairings.md) | semicolon separated list of gene to reaction pairings |
| [genes](genes.md) | semicolon separated list of genes that catalyzes the mentioned reactions |
| [has_evidence](has_evidence.md) | evidence for the reaction |
| [id](id.md) | A unique identifier for the named entity |
| [input_id](input_id.md) |  |
| [input_text](input_text.md) |  |
| [input_title](input_title.md) |  |
| [label](label.md) | the name of the reaction |
| [left_side](left_side.md) | semicolon separated list of chemical entities on the left side |
| [named_entities](named_entities.md) | Named entities extracted from the text |
| [object](object.md) |  |
| [object_id](object_id.md) |  |
| [object_qualifier](object_qualifier.md) | An optional qualifier or modifier for the object of the statement, e |
| [object_text](object_text.md) |  |
| [organism](organism.md) |  |
| [predicate](predicate.md) |  |
| [prompt](prompt.md) |  |
| [publication](publication.md) |  |
| [qualifier](qualifier.md) | A qualifier for the statements, e |
| [raw_completion_output](raw_completion_output.md) |  |
| [reaction](reaction.md) | equation describing the reaction (e |
| [reactions](reactions.md) | semicolon separated list of reaction equations (e |
| [right_side](right_side.md) | semicolon separated list of chemical entities on the right side |
| [subclass_of](subclass_of.md) | the category to which this biological process belongs |
| [subject](subject.md) |  |
| [subject_qualifier](subject_qualifier.md) | An optional qualifier or modifier for the subject of the statement, e |
| [subject_text](subject_text.md) |  |
| [synonyms](synonyms.md) | alternative names of the reaction |
| [title](title.md) | The title of the publication |
| [triples](triples.md) |  |


## Enumerations

| Enumeration | Description |
| --- | --- |


## Types

| Type | Description |
| --- | --- |
| [Boolean](Boolean.md) | A binary (true or false) value |
| [Date](Date.md) | a date (year, month and day) in an idealized calendar |
| [DateOrDatetime](DateOrDatetime.md) | Either a date or a datetime |
| [Datetime](Datetime.md) | The combination of a date and time |
| [Decimal](Decimal.md) | A real number with arbitrary precision that conforms to the xsd:decimal speci... |
| [Double](Double.md) | A real number that conforms to the xsd:double specification |
| [Float](Float.md) | A real number that conforms to the xsd:float specification |
| [Integer](Integer.md) | An integer |
| [Ncname](Ncname.md) | Prefix part of CURIE |
| [Nodeidentifier](Nodeidentifier.md) | A URI, CURIE or BNODE that represents a node in a model |
| [Objectidentifier](Objectidentifier.md) | A URI or CURIE that represents an object in the model |
| [String](String.md) | A character string |
| [Time](Time.md) | A time object represents a (local) time of day, independent of any particular... |
| [Uri](Uri.md) | a complete URI |
| [Uriorcurie](Uriorcurie.md) | a URI or a CURIE |


## Subsets

| Subset | Description |
| --- | --- |
