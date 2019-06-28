# gmock_generator
mock generator of C and C++ functions (based on official googletest mock generator)

To use the Google Mock class generator, you need to call it
on the command line passing the header file and class for which you want
to generate a Google Mock class.

Make sure to install the scripts somewhere in your path.  Then you can
run the program.

  gmock_gen.py header-file.h [ClassName]...

If no ClassNames are specified, all classes in the file are emitted.

To change the indentation from the default of 2, set INDENT in
the environment.  For example to use an indent of 4 spaces:

INDENT=4 gmock_gen.py header-file.h ClassName

Known Limitations
-----------------
Not all code will be generated properly.  For example, when mocking templated
classes, the template information is lost.  You will need to add the template
information manually.

Not all permutations of using multiple pointers/references will be rendered
properly.  These will also have to be fixed manually.
