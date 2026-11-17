# CSC405MOD6

**CSC405 Computer Graphics, CSU Global (Winter 2026, Session A). Module 6: Lighting and Shading**

Recursive sphere with ADS shading.

## Enabling Objectives

By the end of this module, you will be able to:

1. Examine light and matter.
2. Examine computation of vectors.
3. Describe polygonal shading.
4. Describe normal vectors.
5. Characterize light source.

## Readings

**Required**

- Gordon, V. S., & Clevenger, J. (2021). Computer graphics programming in OpenGL with Java (3rd ed.). Mercury Learning.
  - Chapter 6
    - Section 6.1: Procedural Models - Building a Sphere
  - Chapter 7: Lighting

**Recommended**

- Akenine-Möller, T., Haines, E., Hoffman, N., Pesce, A., Iwanicki, M., & Hillaire, S. (2022). Real-time rendering (4th ed.). A K Peters / CRC Press.
  - Chapter 5: Shading Basics — https://learning-oreilly-com.csuglobal.idm.oclc.org/library/view/real-time-rendering-fourth/9781351816144/xhtml/ch05.xhtml
- Hill, S. (2026). SIGGRAPH 2025 course: Physically based shading in theory and practice. Self Shadow. https://blog.selfshadow.com/publications/s2025-shading-course/

## Assignment: Module 6: Critical Thinking

Approximating a Sphere Recursively (100 Points)

Read Chapter 6, Section 6.1 (“Procedural Models—Building a Sphere”) and Chapter 7 (“Lighting”) of Gordon & Clevenger (2021). Note in particular the recursive subdivision approach and the ADS lighting model (ambient, diffuse, specular).

In one paragraph, briefly discuss how the sphere is used as an example curved surface to illustrate shading calculations. Then, using Java with JOGL, design an interactive program that:

Builds a sphere by recursive subdivision of an icosahedron or octahedron, as shown in Section 6.1 (start with subdivision depth 0 and let the user increase/decrease it interactively).

Implements either Gouraud or Phong shading using the ADS lighting model from Chapter 7, with at least one positional light source.

Allows the user to toggle between Gouraud and Phong shading and observe the visual difference.


### Submission Guidelines

Your Java source files and GLSL shaders.

Screenshots at three subdivision levels and screenshots comparing Gouraud vs. Phong shading.

A Word document with your one-paragraph sphere discussion and a two-paragraph reflection on what you observed when toggling shading modes (approximately 3 paragraphs total).

Your paper must be formatted according to APA guidelines in the CSU Global Writing Center (available in the left-hand navigation panel).

Refer to the rubric below for more details about how you will be graded for this assignment.

