.. _shapes:

Shapes
======

Shapes are objects that can be added to a slide. There are five types of shapes that can be used, i.e. [rich text](#rich-text), [line](#line), [chart](#chart), [drawing](#drawing), and [table](#table). Read the corresponding section of this manual for detail information of each shape.

Every shapes have common properties that you can set by using fluent interface.

- ``width`` in pixels
- ``height`` in pixels
- ``offsetX`` in pixels
- ``offsetY`` in pixels
- ``rotation`` in degrees
- ``fill`` see *[Fill](#fill)*
- ``border`` see *[Border](#border)*
- ``shadow`` see *[Shadow](#shadow)*
- ``hyperlink``

Example:

.. code-block:: php

	$richtext = $slide->createRichTextShape()
		->setHeight(300)
		->setWidth(600)
		->setOffsetX(170)
		->setOffsetY(180);

Generic Shape
-------------

Shapes are a core part of presentations, and we need a variety of shapes for presentations. Following are the options of the shapes that we can use with this generic function. These shapes can be adjusted according to the requirements of the presentation.

- ``accentBorderCallout1``
- ``accentBorderCallout2``
- ``accentBorderCallout3``
- ``accentCallout1``
- ``accentCallout2``
- ``accentCallout3``
- ``actionButtonBackPrevious``
- ``actionButtonBeginning``
- ``actionButtonBlank``
- ``actionButtonDocument``
- ``actionButtonEnd``
- ``actionButtonForwardNext``
- ``actionButtonHelp``
- ``actionButtonHome``
- ``actionButtonInformation``
- ``actionButtonMovie``
- ``actionButtonReturn``
- ``actionButtonSound``
- ``arc``
- ``bentArrow``
- ``bentConnector2``
- ``bentConnector3``
- ``bentConnector4``
- ``bentConnector5``
- ``bentUpArrow``
- ``bevel``
- ``blockArc``
- ``borderCallout1``
- ``borderCallout2``
- ``borderCallout3``
- ``bracePair``
- ``bracketPair``
- ``callout1``
- ``callout2``
- ``callout3``
- ``can``
- ``chartPlus``
- ``chartStar``
- ``chartX``
- ``chevron``
- ``chord``
- ``circularArrow``
- ``cloud``
- ``cloudCallout``
- ``corner``
- ``cornerTabs``
- ``cube``
- ``curvedConnector2``
- ``curvedConnector3``
- ``curvedConnector4``
- ``curvedConnector5``
- ``curvedDownArrow``
- ``curvedLeftArrow``
- ``curvedRightArrow``
- ``curvedUpArrow``
- ``decagon``
- ``diagStripe``
- ``diamond``
- ``dodecagon``
- ``donut``
- ``doubleWave``
- ``downArrow``
- ``downArrowCallout``
- ``ellipse``
- ``ellipseRibbon``
- ``ellipseRibbon2``
- ``flowChartAlternateProcess``
- ``flowChartCollate``
- ``flowChartConnector``
- ``flowChartDecision``
- ``flowChartDelay``
- ``flowChartDisplay``
- ``flowChartDocument``
- ``flowChartExtract``
- ``flowChartInputOutput``
- ``flowChartInternalStorage``
- ``flowChartMagneticDisk``
- ``flowChartMagneticDrum``
- ``flowChartMagneticTape``
- ``flowChartManualInput``
- ``flowChartManualOperation``
- ``flowChartMerge``
- ``flowChartMultidocument``
- ``flowChartOfflineStorage``
- ``flowChartOffpageConnector``
- ``flowChartOnlineStorage``
- ``flowChartOr``
- ``flowChartPredefinedProcess``
- ``flowChartPreparation``
- ``flowChartProcess``
- ``flowChartPunchedCard``
- ``flowChartPunchedTape``
- ``flowChartSort``
- ``flowChartSummingJunction``
- ``flowChartTerminator``
- ``folderCorner``
- ``frame``
- ``funnel``
- ``gear6``
- ``gear9``
- ``halfFrame``
- ``heart``
- ``heptagon``
- ``hexagon``
- ``homePlate``
- ``horizontalScroll``
- ``irregularSeal1``
- ``irregularSeal2``
- ``leftArrow``
- ``leftArrowCallout``
- ``leftBrace``
- ``leftBracket``
- ``leftCircularArrow``
- ``leftRightArrow``
- ``leftRightArrowCallout``
- ``leftRightCircularArrow``
- ``leftRightRibbon``
- ``irregularSeal1``
- ``leftRightUpArrow``
- ``leftUpArrow``
- ``lightningBolt``
- ``line``
- ``lineInv``
- ``mathDivide``
- ``mathEqual``
- ``mathMinus``
- ``mathMultiply``
- ``mathNotEqual``
- ``mathPlus``
- ``moon``
- ``nonIsoscelesTrapezoid``
- ``noSmoking``
- ``notchedRightArrow``
- ``octagon``
- ``parallelogram``
- ``pentagon``
- ``pie``
- ``pieWedge``
- ``plaque``
- ``plaqueTabs``
- ``plus``
- ``quadArrow``
- ``quadArrowCallout``
- ``rect``
- ``ribbon``
- ``ribbon2``
- ``rightArrow``
- ``rightArrowCallout``
- ``rightBrace``
- ``rightBracket``
- ``round1Rect``
- ``round2DiagRect``
- ``round2SameRect``
- ``roundRect``
- ``rtTriangle``
- ``smileyFace``
- ``snip1Rect``
- ``snip2DiagRect``
- ``snip2SameRect``
- ``snipRoundRect``
- ``squareTabs``
- ``star10``
- ``star12``
- ``star16``
- ``star24``
- ``star32``
- ``star4``
- ``star5``
- ``star6``
- ``star7``
- ``star8``
- ``straightConnector1``
- ``stripedRightArrow``
- ``sun``
- ``swooshArrow``
- ``teardrop``
- ``trapezoid``
- ``triangle``
- ``upArrow``
- ``upArrowCallout``
- ``upDownArrow``
- ``upDownArrowCallout``
- ``uturnArrow``
- ``verticalScroll``
- ``wave``
- ``wedgeEllipseCallout``
- ``wedgeRectCallout``
- ``wedgeRoundRectCallout``

This demo code will demonstrate how we can use this function for all the available shapes. We can also resize and rotate them using the following parameters.

Example Generic Shape:

.. code-block:: php

     * @param  int $fromX Starting point x offset
     * @param  int $fromY Starting point y offset
     * @param  int $toX Ending point x offset
     * @param  int $toY Ending point y offset
     * @param  int $rotation Used for the rotation clockwise or anti-clockwise
     * @param  string $shape Used for giving a dynamic shape option are in this link "http://officeopenxml.com/drwSp-prstGeom.php"
     * @return \PhpOffice\PhpPresentation\Shape\GenericShape

	$shape = $slide->createGenricShape( 20,200,90,350,0, 'wedgeEllipseCallout' )
		->getBorder()
        ->setLineStyle(Border::LINE_SINGLE)
        ->setLineWidth(2)
        ->getColor()
        ->setARGB('FF2980b9');

Arrow Pointer
-------------

Arrow pointers are used to connect different shapes together. Arrow pointers are useful as compare to simple connectors because arrow pointer can show the flow, and direction.

.. code-block:: php

    /**
     * Create an arrow pointer
     *
     * @param  int $fromX Starting point x offset
     * @param  int $fromY Starting point y offset
     * @param  int $toX Ending point x offset
     * @param  int $toY Ending point y offset
     * @return \PhpOffice\PhpPresentation\Shape\ArrowPointer
     */

    $slide->createArrowPointer(270,440,650,440)
        ->getBorder()
        ->setLineStyle(Border::LINE_SINGLE)
        ->setLineWidth(2)
        ->getColor()
        ->setARGB('FF2980b9');

Line
----

To create a line, use `createLineShape` method of slide.

.. code-block:: php

    $slide->createLineShape(270,440,650,440)
        ->getBorder()
        ->setLineStyle(Border::LINE_SINGLE)
        ->setLineWidth(2)
        ->getColor()
        ->setARGB('FF0000FF');
