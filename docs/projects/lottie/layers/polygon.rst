Polygon Layer
=============

+-----------------+------------------------------------------------------------------------+
|     Property    |                         Path to Property in lottie                     |
+=================+========================================================================+
|     Z depth     |             Depends on ordering of layers in lottie format             |
+-----------------+------------------------------------------------------------------------+
|      Amount     | layers/solid.json -> "ef" -> effects/fill.json -> effects/opacity.json |
+-----------------+------------------------------------------------------------------------+
|   Blend_method  |           layers/solid.json -> "bm" -> helpers/blendMode.json          |
+-----------------+------------------------------------------------------------------------+
|      Color      |  layers/solid.json -> "ef" -> effects/fill.json -> effects/color.json  |
+-----------------+------------------------------------------------------------------------+
|      Origin     |                   Added to vertex list of the polygon                  |
+-----------------+------------------------------------------------------------------------+
|      Invert     |             layers/solid.json -> helpers/mask.json -> "inv"            |
+-----------------+------------------------------------------------------------------------+
|   Antialiasing  |            This property is always present(true) in lottie.            |
+-----------------+------------------------------------------------------------------------+
|     Feather     |                              Not Supported                             |
+-----------------+------------------------------------------------------------------------+
| Type of Feather |                              Not supported                             |
+-----------------+------------------------------------------------------------------------+
|  Winding Style  |                              Not supported                             |
+-----------------+------------------------------------------------------------------------+
|  Vertices List  |             layers/solid.json -> helpers/mask.json -> "pt"             |
+-----------------+------------------------------------------------------------------------+

Important points
----------------

- Instead of directly using the shapes layer from Lottie, a solid color layer is used and is masked(using masks) to draw a polygon. This is done to support the invert parameter from Synfig.
