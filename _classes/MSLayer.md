---
layout: class
title:  "MSLayer"
rels:
  - MSLayerGroup
  - MSRect
  - GKRect
  - MSStyle
  - MSPage
---

## Overview

MSLayer is the base class that represents a layer object.

## Methods & Attributes

### frame (readonly)

An instance of [MSRect](MSRect.html). Determines size and position on the canvas

### style (readonly)

An instance of [MSStyle](MSStyle.html). Determines all style-related attributes such as Borders, Fills, Shadows and more

### name / setName

The name of the layer as it appears in the layer list. An NSString.

### isVisible / setIsVisible

Returns `true` if the layer is visible, and `false` if it is hidden.

To **hide** a layer, do:

    [layer setIsVisible:false]

If you want to toggle a layer’s visibility, do:

    [layer setIsVisible:![layer isVisible]]


### isLocked / setIsLocked

Returns `true` if the layer is locked, and `false` if it isn’t locked.

To **lock** a layer, do:

    [layer setIsLocked:true]

If you want to toggle a layer’s lock status, do:

    [layer setIsLocked:![layer isLocked]]

### rotation / setRotation

An integer denoting the rotation of the layer - in degrees. Rotation happens counter-clockwise.

### isFlippedHorizontal / setIsFlippedHorizontal | isFlippedVertical / setIsFlippedVertical

Flips the layer horizontally or vertically.

    [layer isFlippedHorizontal]

### parentGroup

Returns the parent group of this layer. Note that this can return an [MSPage](MSPage.html) or [MSArtboardGroup](MSArtboardGroup.html) as well as an [MSLayerGroup](MSLayerGroup.html)

### isSelected / setIsSelected

True if the layer is selected, false otherwise.

### select:byExpandingSelection

Check the [Working with Selections](../02-common-tasks/02.html) section for some examples.

### absoluteRect (readonly)

Returns a [GKRect](GKRect.html) object that returns the bounds of this layer in absolute coordinates; it takes into account the layer’s rotation and that of any of its parents.

### duplicate

Duplicates the layer and insert the copy above itself.