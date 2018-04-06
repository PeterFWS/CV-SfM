# CV-SfM
lecture note for Computer Vision, mainly about Structure from Motion (SfM) and 3D reconstruction
## Content OverView

## Computer Vision for Automatic Photogrammetric 3D Data Collection
  • Structure-from-Motion: The big picture


## Automatic Tie-point Generation
### Introduction to Image Matching
		○ Recap: Correlation and Feature Matching
	• SIFT Feature Extraction and Matching 
	• Elimination of outliers by geometric validation
		○ RANSAC for robust parameter estimation
		○ Application example: Automatic image alignment by Projective Transformation Estimation (homography) 
		x'=Hx -> A2x9h9x1=0, 4 points, SVD
		
	

## Projective Geometry for efficient solution of photogrammetric tasks
### Efficient modelling of camera parameters: Perspective Projection Matrix
		○ Application and Assignment: Spatial Resection by DLT
		x=P3x4X 
		Over determined spatial intersection
		A3x4X4x1=0
		P_DLT -> A2x12p12x1=0, 6 points, SVD
		 ->Extracting camera parameters


## Structure-from-Motion
### Connectivity Matrix 
	• Essential and Fundamental matrix for Relative Orientation 
	A1x9f9x1=0, 8 points, SVD
	Epipolar Lines
	I'=Fx
	• Bundle Block Adjustment
	


## Dense Multi-View-Stereo Image Matching for 3D Surface Reconstruction
### Epipolar image generation
		○ Prerequisite for parallax or disparity images
		○ Simplified matching using epipolar lines and epipolar images
		○ Generation of epipolar images
			§ using homographies
	• Dense Pixel Matching
		○ Window based algorithms
		○ Pixel based matching: Global Matching
			§ Census
			§ Stereo Correspondence by Dynamic Programing
			§ Optimization of global Matching Costs
		○ Semi-Global Matching
			§ Cost Cube
				□ Cost aggregation along path through cost cube
				□ Cost Accumulation along multiple paths
			§ Forward-backward matching to detect potential matching errors
	• Triangulation
		○ Multi-View Stereo
			§ Multi Stereo Matching
			§ Multi-Stereo-Triangulation
		○ Depth Maps and Point-clouds
		○ Filtering and Fusion of 3D point clouds
	• Gridding
	

## MVS-Surface Reconstruction
###  DSM and Meshes for 3D Visualization
		○ Hierarchical representations of triangle meshes
		○ Modification of meshed triangles
		○ Adapt triangle size at building facades
		○ DSM Mesh
			§ Processing of 2D meshes: Texture mapping
### Stereo vision: General Tasks
		○ Depth Maps and Point-clouds
		○ Range images for 2D representation of per-pixel distances
### Multi-view stereo pipeline
		○ Compute depth-maps from each view using neighbouring views
		○ Merge depth-maps into single volume
		○ Extract 3d surface from this volume
### Markov Random Field for MVS-optimization
### Volumetric Graph-Cuts on a Voxel Grids
		○ Volumetric Representation
### Space Carving
		○ Voxel & Signed distance fields
### Graph-cut to solve 3D binary labelling problem
###  From volume to mesh: Marching Cubes
###  Surface Extraction from Point Clouds
		○ Visibility consistent mesh extraction
		○ Delaunay Tetrahedrization



## Real-time Applications: SLAM
