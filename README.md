Hello I am Damodar Dhakad from SATI Vidisha, India. I will be preparing 
for Google Summer of Code under R organization. The project entitled as 

# marshal: Saving and Loading Objects that Otherwise Cannot be Saved or 
Exported to Parallel Workers
 
Following are the tests that I need to complete to become a good candidate for 
the above mentioned project. 

## 1. Easy: Git and R package testing

Fork the marshal repository and build the package and check it with both devtools::check() and R CMD check --as-cran.

## 2. Easy: Prototyping in R

Write XML_serialize_refhook() and XML_unserialize_refhook() functions that are simple wrappers that calls XML::xmlSerializeHook() and XML::xmlDeserializeHook() internally such that they can be used in place of the latter two functions

Write a package help page with an example illustrating how to use your new functions for saving and reading XML objects to file

Try to make the package passes R CMD check will all OKs

## 3. Medium: Package tests

Add package tests that validates your new pair of functions. The help example is often a good start

Write test cases where you call your functions in non-expected ways, e.g. with objects that your functions don't expect

Try to update your functions to handle such unexpected input, e.g. by producing an error, a warning, or silently returning NULL, or what you think makes the most sense

## 4. Medium/Hard: Use marshal functions for parallelization

With the help of XML_serialize_refhook() and XML_unserialize_refhook(), try to pass an XML object doc to a parallel worker, which should call y <- as(doc, "character") on it and then return y. You may use the parallel package or the future package for this example

## 5. Hard: Begin to work on the project.
