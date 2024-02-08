# Mesh Generator (Assignment #2 Walkthrough)

  - Author: Sébastien Mosser

## How to install?

```
mosser@azrael A2 % mvn install
```

It creates two jars:

  1. `generator/generator.jar` to generate meshes
  2. `visualizer/visualizer.jar` to visualize such meshes as SVG files

## Examples of execution

### Generating a mesh, grid or irregular

```
mosser@azrael A2 % java -jar generator/generator.jar -k grid -h 1080 -w 1920 -p 1000 -s 20 -o img/grid.mesh
mosser@azrael A2 % java -jar generator/generator.jar -k irregular -h 1080 -w 1920 -p 1000 -s 20 -o img/irregular.mesh
```

One can run the generator with `-help` as option to see the different command line arguments that are available

### Visualizing a mesh, (regular or debug mode)

```
mosser@azrael A2 % java -jar visualizer/visualizer.jar -i img/grid.mesh -o img/grid.svg          
mosser@azrael A2 % java -jar visualizer/visualizer.jar -i img/grid.mesh -o img/grid_debug.svg -x
mosser@azrael A2 % java -jar visualizer/visualizer.jar -i img/irregular.mesh -o img/irregular.svg   
mosser@azrael A2 % java -jar visualizer/visualizer.jar -i img/irregular.mesh -o img/irregular_debug.svg -x
```

Note: PDF versions of the SVG files were created with `rsvg-convert`.

### Running Our Code
To run the MVP sandbox, type ./run.sh into the command line. This creates a circular island with a lagoon and beach tiles. 

To change the shape of the island, go to line 29 in island/src/main and change the shape from "circle" to "oval". For examole, by running "Mesh cloned = cloneMesh.circle(aMesh, outerRadius, innerRadius);" we change the shape of the island to be a circle.
### Product Backlog

| Id | Feature title | Who? | Start | End | Status |
|:--:|---------------|------|-------|-----|--------|
|  F01  | Create configuration commands | Sylvia  | 21/25/2023 | 22/03/2023 | D |
|  F02  | Distance methods from canvas to centroids | Chengze | 22/03/2023 | 23/03/2023 | D |
|  F03  | Set polygon colours in island generator | Rosa | 23/03/2023 | 24/03/2023 | D |
|  F04  | Add beach tiles | Chengze | 24/03/2023 | 25/03/2023 | D |
|  F05  | Created another map shape (oval) | Sylvia | 25/03/2023 | 25/03/2023 | D |