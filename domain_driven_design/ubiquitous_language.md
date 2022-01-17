# Ubiquitous Language
Domain experts have limited understanding of the technical jargon of software development, but instead use the jargon of their chosen field.

On the other hand, developers may discuss and understand a system in descriptive, functional terms which lack the meaning of the experts' language.

Across this linguistic divide, domain experts vaguely describe what they want while developers struggle to understand a domain new to them. 

**Ubiquitous Language** bridges this divide and allows experts and developers to communicate clearly and without misunderstanding:
- The **vocabulary** comprises of **classes** and prominent **operations** 
- The **language** comprises terms to discuss **rules** that have been made explicit in the model. It is supplemented with terms from high-level organizing principles imposed on the model (such as **context maps** and **large-scale structures**)

Persistent use of the **ubiquitous language** exposes weaknesses in the domain model. The team will identify alternatives to awkward terms or combinations. As these gaps are plugged, the changes to the language will also be changes to the domain model. This means updating **class names**, **methods**, and changing **behaviour**.

Naturally, domain experts will speak outside the scope of the **ubiquitous language**, to explain broader contexts. But within the scope of the model, they should use the **language**. If they find it to be awkward or incomplete, then there are oppurtunities for refactoring. 

- Use the model as the backbone of a language
- Commit to exercising the language relentlessly in all communication and code
- Iron out difficulties by experimenting with alternative expressions/models
- Refactor the code, renaming classes, methods, and modules to conform to the new model
- Resolve confusion over terms in conversation, just like with normal language
- Domain experts should object to terms or structures they find awkward or inadequate
- Developers should watch for ambiquity or inconsistency that will trip up design
- #### Recognize that a change in the Ubiquitous Language is a change in the Model

