# Terraform Debug provider

## Problem

Terraform being a descriptive tool is fairly difficult to debug. When there's a heavy use of Terraform modules, it's difficult to get the visibility on the values of variables passed between modules. Our team faces these difficulties especially when the modules use complex variable types with complex loop logic to iterate over them (e.g. map of arrays of maps). Moreover, the need for better debugging options rise with abstraction used on the project. When Terraform is executed through Terramate, Terragrunt or in the pipelines, there's no possibility for the user to fire up `terraform console` and test expressions and loop definitions over them.

## Solution

A debug provider would have just a single resource-type, which takes an input variable and prints its value on the STDERR (in YAML, JSON or HCL formats - controlled by a resource parameter). This way, the user will have a chance to see into the variables carrying values within the TF layers.
