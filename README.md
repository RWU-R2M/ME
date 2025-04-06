# R2M Mechanical Design Guidelines

## Introduction

Welcome to the R2M Mechanical Design Guidelines. This document is a guide for the RWU Rover to Mars (R2M) team. This is to be used as a reference to design and build the mechanical parts of our rover. The goal is to be able to achieve a certain standard of quality and style across all the parts that we design, and manufacture.

## Software 

Fusion 360, can be had for free with a hobyist license, or a student license (student license has more features, highly recommended)

## Designing requirements

All the designed parts should have a requirements list, that is, a simple document with conditions for the given part to accepted as finished. The requirements MUST contain:

- Justification to why a certain part is needed
- In which assembly/ subassembly will the part be used
- Manufacturing constraints (eg. 3d, 3 axis CNC, laser, etc)
- Material constraints
- Deadline for having a finished part
- Technical Drawing standard to be used

It MAY also contain:
- Tolerated cost of the part
- Fastener standard to be used (or specific fasteners to be used)
- Tolerances to be used
- Form constraints based on other parts in subassembly (include technical drawings of other parts, including required fit types, tolerances, etc)
- Any other constraint that is relevant for the design of the part

## Modeling Parts of an Assembly (or Subassembly)

When designing parts that belong to an assembly, it is important to take into account the other elements of the assembly too. For that, the recommended workflow for developing such a part is as follows:

- make a copy of the assembly (or subassembly, or the other components that are relevant to the part t obe designed), and work on the part by selecting it as the active component.

- add ALL the joints and fasteners that would be required to support the part (Fusion has a vast library of fasteners, and there are joint types for any give geometric constraints)

- Simulate the movement of the part, check for collisions, check if all fasteners are reachable with the required tools

- Finally, add the part in the final assembly with ALL required fasteners and joints.

## Bodies vs Components when adding joints

All independent bodies should be components, not matter how small they are. Joints should be used when mating components. The rigid joint should only be used when necessary, for all other cases, there are specific joints for each geometry.

If two bodies are mated together, and they are always going to move together, keeping their relative position, they can be mated into a single body. The single body can then be mated into a component

## Naming parts

All parts should have descriptive names. That makes collaboration easier. Parts should have their names in small caps (eg. "banana"). Sub assemblies should have their names in capital letters ("eg. "BANANA_HOLDER"). 

All names should include no spaces or special characters, as they can break external plugins, such as the URDF exporter plugin, used for creating Gazebo models. Underscores should be used instead of spaces when separating words in part names.

# Technical drawings

Should follow the example that can be found in the Fusion team hub. 

A valid technical drawing MUST contain:

- Should be according to ISO 128 (American standard is not accepted)
- Name of the designer
- Correct drawing views according to German standard (DIN)(First Angle Projection)
- Name of the part
- Date of submission
- Material
- Tolerance class declaration
- Toleranced dimensions for the critical features
- Standardized fit type declarations according to DIN-ISO 286 when applicable
- All needed dimensions for the production of the part
- All necessary views for the production of the part

It MAY also contain:
- Extra views
- Any other information that is required for the production of the part


# Tips

The best design is the simplest design that complies with the requirements. If something is becoming too complicated, take a step back and ask yourself, "how could I make this simpler?". 

Organize your designs, that becomes crucial down the line once you have several parts that depend on one another.

Check for interferences 







