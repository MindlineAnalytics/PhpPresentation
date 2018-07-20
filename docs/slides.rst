.. _slides:

Slides
======

Slides are pages in a presentation. Slides are stored as a zero based array in ``PHPPresentation`` object. Use ``createSlide`` to create a new slide and retrieve the slide for other operation such as creating shapes for that slide.

Name
----

By default, a slide has not a name.
You can define it with the method ``setName``.

.. code-block:: php

	$oSlide = $oPHPPresentation->createSlide();
	$oSlide->setName('Title of the slide');

Visibility
----------

By default, a slide is visible.
You can define it with the method ``setIsVisible``.

.. code-block:: php

	$oSlide = $oPHPPresentation->createSlide();
	$oSlide->setIsVisible(false);
	var_dump($oSlide->isVisible());

Master Slides
-------------

We can make one or more than one ``master`` slides for presentations. Slide layout can also be set using the sample code.

.. code-block:: php

    //Master Slide 1
    $oMasterSlide1 = $objPhpPowerPoint->getAllMasterSlides()[0];
    $shape = $oMasterSlide1->createDrawingShape();

    //Master Slide 2
    $oMasterSlide2 = $objPhpPowerPoint->getAllMasterSlides()[1];
    $shape = $oMasterSlide2->createDrawingShape();

By default Master 1 is always default, and to apply Master 2

.. code-block:: php

    $oSlideLayout = $oMasterSlide2->createSlideLayout();

    //Slide in which you want to apply Master 2

    $slide = $objPhpPowerPoint->createSlide();
    $slide->setSlideLayout($oSlideLayout);