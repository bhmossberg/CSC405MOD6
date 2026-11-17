# CSC405 Module 6 — Textbook Example Programs

Example code from Gordon, V. S., & Clevenger, J. (2021). Computer graphics programming in OpenGL with Java (3rd ed.). Mercury Learning and Information. Used for coursework study.

Official companion files were downloaded from the author’s page,
[Computer Graphics Programming in OpenGL with Java, 3rd Edition](https://athena.ecs.csus.edu/~gordonvs/textJ3E.html)
(`J3E_CompanionFiles.zip`). Each program folder is self-contained:
its `.java` sources, `.glsl` shaders, utility classes (`Utils.java`,
`Sphere.java`, `Torus.java`, `ImportedModel.java` as needed), and any
textures or models that program loads are copied into that folder.

**Assigned reading:** Chapter 6, Section 6.1; Chapter 7 (entire).

## Programs in this module

### Program6_1 — Procedurally Generated Sphere

- **Section:** 6.1 Procedural Models — Building a Sphere
- **Official folder:** `Chapter_06_models/Prog6_1_sphere`
- **Assets included:** `earth.jpg`

### Program7_1 — Torus with Positional Light and Gouraud Shading

- **Section:** 7.5.1 Gouraud Shading
- **Official folder:** `Chapter_07_lighting/Prog7_1_gouraud`

### Program7_2 — Torus with Phong Shading

- **Section:** 7.5.2 Phong Shading
- **Official folder:** `Chapter_07_lighting/Prog7_2_phong`

### Program7_3 — Torus with Blinn-Phong Shading

- **Section:** 7.5.2 Phong Shading (Blinn-Phong variant)
- **Official folder:** `Chapter_07_lighting/Prog7_3_blinnPhong`

## Assigned sections without a numbered program

- Sections 7.1–7.4 develop the ADS lighting model and are implemented in Programs 7.1–7.3.
- Section 7.6 (Combining Lighting and Textures) has no separate numbered program in the companion (later texture+lighting examples appear in unassigned chapters, such as Program 10.3).

## Compile and run

These programs use the official companion layout: Java sources and shaders live in a `code/` package (`package code;`), and textures or `.obj` models sit in the program folder (the working directory when you run). Shaders are loaded with paths such as `code/vertShader.glsl`.

You need **JDK 11**, **JOGL 2.4** (`jogl-all.jar`, `gluegen-rt.jar`, plus the native jars for your OS), and **JOML 1.10** (`joml-1.10.0.jar`) on the classpath. The textbook’s Appendix A (Windows) and Appendix B (macOS) cover installation. On Linux, put the jars in a `lib` directory (or any folder you prefer) and run the following from a program folder, for example `Program2_5`:

```bash
# Adjust these paths to where you keep the jars
CP="lib/jogl-all.jar:lib/jogl-all-natives-linux-amd64.jar:lib/gluegen-rt.jar:lib/gluegen-rt-natives-linux-amd64.jar:lib/joml-1.10.0.jar"

# Compile (from the program folder that contains the code/ directory)
javac -cp "$CP" code/*.java

# Run (also from that program folder, so shader and texture paths resolve)
java -cp "$CP:." \
  --add-exports java.base/java.lang=ALL-UNNAMED \
  --add-exports java.desktop/sun.awt=ALL-UNNAMED \
  --add-exports java.desktop/sun.java2d=ALL-UNNAMED \
  -Dsun.java2d.d3d=false -Dsun.java2d.uiScale=1 \
  code.Code
```

On Windows, use `;` instead of `:` in the classpath, and the official `compile.bat` / `run.bat` in each folder assume the JOGL and JOML jars are already on your global `CLASSPATH` (as the book’s setup appendix describes):

```bat
javac code/Code.java
java --add-exports java.base/java.lang=ALL-UNNAMED --add-exports java.desktop/sun.awt=ALL-UNNAMED --add-exports java.desktop/sun.java2d=ALL-UNNAMED -Dsun.java2d.d3d=false -Dsun.java2d.uiScale=1 code.Code
```

Programs that open a window need a display; compiling does not.


This `textbook-examples` folder contains **30** files.
