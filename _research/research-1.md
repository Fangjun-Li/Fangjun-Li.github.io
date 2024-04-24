---
title: "Reframing Spatial Reasoning Evaluation in Language Models"
excerpt: "This work builds a real-world simulation benchmark for evaluating spatial reasoning abilities of language models.<br/><img src='/images/IJCAI-00.gif'>"
collection: research
---

## Introduction

Spatial reasoning plays a vital role in both human cognition and machine intelligence, prompting new research into language models' (LMs) capabilities in this regard. However, existing benchmarks reveal shortcomings in evaluating qualitative spatial reasoning (QSR). These benchmarks typically present oversimplified scenarios or unclear natural language descriptions, hindering effective evaluation. 

This work presents a novel benchmark for assessing QSR in LMs, which is grounded in realistic 3D simulation data, offering a series of diverse room layouts with various objects and their spatial relationships. This approach provides a more detailed and context-rich narrative for spatial reasoning evaluation, diverging from traditional, toy-task-oriented scenarios.

Our benchmark encompasses a broad spectrum of qualitative spatial relationships, including topological, directional, and distance relations. These are presented with different viewing points, varied granularities, and density of relation constraints to mimic real-world complexities. A key contribution is our logic-based consistency-checking tool, which enables the assessment of multiple plausible solutions, aligning with real-world scenarios where spatial relationships are often open to interpretation.

Our benchmark evaluation of advanced LM reveals their strengths and limitations in spatial reasoning. They struggle with complex spatial contexts, especially in topological and distance constraints and in interpreting north-facing view descriptions, pointing to areas for future improvement.

![Editing a markdown file for a talk](/images/IJCAI24-01.png)
*One test instance in our RoomSpace benchmark, consisting only of text for evaluating LMs. The accompanying images are for visualization and can be used for multi-modality modal tests.*



![Editing a markdown file for a talk](/images/IJCAI24-02.png)
*Example scenes in our dataset with top-down view.*



## Problem Definition

We focus on constraint satisfaction problems (CSP), defined by a set of variables defined over a domain and a collection of constraints. The goal is to find a specific instantiation where all constraints are simultaneously satisfied.
We particularly emphasize binary constraints, which simultaneously restrict the domain of two variables. An example of this is the constraint *The desk is placed in front of the window.*


## Data Generation Process
All constructed constraint networks are transformed into textual format, specifically for the purpose of evaluating LMs.

Our test sets are available in varying sizes:
- **RoomSpace-100** includes a sample of 100 rooms.
- **RoomSpace-1K** consists of 1,000 rooms.
- **RoomSpace-10K** comprises 10,000 rooms.

The initial 100 rooms in **RoomSpace-1K** (ID 0-99) are identical to those in **RoomSpace-100**. Similarly, the first 1,000 rooms in **RoomSpace-10K** (ID 0-999) match those in **RoomSpace-1K**.

### Specify Spatial Relationships
For spatial relationship constraints, we focus on three categories: topological relations, directional relations, and distance relations. These are employed to articulate the positioning of objects within rooms and the inter-object relationships.

![Editing a markdown file for a talk](/images/IJCAI24-03.png)
*Illustration showcasing two topological spatial relations: TPP (in red, denoting objects touching the room's walls) and NTPP (in green, representing objects positioned inside the room's boundaries without touching the walls).*

![Editing a markdown file for a talk](/images/IJCAI24-04.png)
*An overview of directional and distance spatial relationships: The left image displays the room's spatial divisions. The middle image displays both directional and distance-based relationships among objects from a top-down view.  The right image illustrates directional relations as seen from a north-facing perspective.*

### Creating Reasoning Story, Questions and Answers
Our benchmark offers a variety of stories with varying levels of complexity, accomplished by adjusting two key parameters: `$n$` for object selection and `$p_1$` for constraint determination.

![Editing a markdown file for a talk](/images/IJCAI24-05.png)


### Conclusion

Our study identifies gaps in current QSR datasets and presents a new benchmark to better evaluate LM capabilities in spatial reasoning. We enhance QSR dataset creation with a benchmark that addresses multiple complexities, including topological, directional, and distance relationships. Our benchmark uniquely incorporates different viewing perspectives in spatial reasoning, moving towards more accurate LM evaluations.

Future directions include incorporating object size and shape, as our current focus is on object centers for spatial relationships. Additionally, exploring more topological relations beyond TPP and NTPP can deepen the benchmark's scope. We also aim to include more complex perspectives, such as an agent's viewpoint within a room, introducing natural front-facing scenarios for more challenging reasoning tasks.

Our findings highlight the need for improvements in LMs, particularly in handling north-facing perspectives, opening new avenues for enhancing spatial reasoning in AI models.

