..
  SPDX-License-Identifier: CC-BY-4.0
  Copyright Contributors to the OpenColorIO Project.
  Do not edit! This file was automatically generated by share/docs/frozendoc.py.

.. py:class:: FileTransform
   :module: PyOpenColorIO
   :canonical: PyOpenColorIO.FileTransform


   .. py:method:: FileTransform.IsFormatExtensionSupported(extension: str) -> bool
      :module: PyOpenColorIO
      :staticmethod:

      Returns true if the extension corresponds to a format supported by :ref:`FileTransform`. The argument is case-insensitive, and a leading dot, if present, is ignored. Note that :ref:`FileTransform` will attempt all format readers on a given file until it is successful, even files that contain an unsupported extension or no extension. However, this function is useful for applications that want to know which files are likely to be LUT files, based on their extension.


   .. py:method:: FileTransform.__init__(*args, **kwargs)
      :module: PyOpenColorIO

      Overloaded function.

      1. __init__(self: PyOpenColorIO.FileTransform) -> None

      2. __init__(self: PyOpenColorIO.FileTransform, src: str = '', cccId: str = '', interpolation: PyOpenColorIO.Interpolation = <Interpolation.INTERP_DEFAULT: 254>, direction: PyOpenColorIO.TransformDirection = <TransformDirection.TRANSFORM_DIR_FORWARD: 0>) -> None


   .. py:method:: FileTransform.getCCCId(self: PyOpenColorIO.FileTransform) -> str
      :module: PyOpenColorIO

      The cccid can be the ID of a CDL or the index of the CDL (as string). If cccid is NULL or empty the first CDL is returned. The cccid is case-sensitive.


   .. py:method:: FileTransform.getCDLStyle(self: PyOpenColorIO.FileTransform) -> PyOpenColorIO.CDLStyle
      :module: PyOpenColorIO


   .. py:method:: FileTransform.getDirection(self: PyOpenColorIO.Transform) -> PyOpenColorIO.TransformDirection
      :module: PyOpenColorIO


   .. py:method:: FileTransform.getFormats() -> PyOpenColorIO.FileTransform.FormatIterator
      :module: PyOpenColorIO
      :staticmethod:


   .. py:method:: FileTransform.getInterpolation(self: PyOpenColorIO.FileTransform) -> PyOpenColorIO.Interpolation
      :module: PyOpenColorIO

      The file parsers that care about interpolation (LUTs) will try to make use of the requested interpolation method when loading the file. In these cases, if the requested method could not be used, a warning is logged. If no method is provided, or a method cannot be used, INTERP_DEFAULT is used.


   .. py:method:: FileTransform.getSrc(self: PyOpenColorIO.FileTransform) -> str
      :module: PyOpenColorIO


   .. py:method:: FileTransform.getTransformType(self: PyOpenColorIO.Transform) -> PyOpenColorIO.TransformType
      :module: PyOpenColorIO


   .. py:method:: FileTransform.setCCCId(self: PyOpenColorIO.FileTransform, cccId: str) -> None
      :module: PyOpenColorIO


   .. py:method:: FileTransform.setCDLStyle(self: PyOpenColorIO.FileTransform, style: PyOpenColorIO.CDLStyle) -> None
      :module: PyOpenColorIO

      Can be used with CDL, CC & CCC formats to specify the clamping behavior of the :ref:`CDLTransform`. Default is CDL_NO_CLAMP.


   .. py:method:: FileTransform.setDirection(self: PyOpenColorIO.Transform, direction: PyOpenColorIO.TransformDirection) -> None
      :module: PyOpenColorIO

      Note that this only affects the evaluation and not the values stored in the object.


   .. py:method:: FileTransform.setInterpolation(self: PyOpenColorIO.FileTransform, interpolation: PyOpenColorIO.Interpolation) -> None
      :module: PyOpenColorIO


   .. py:method:: FileTransform.setSrc(self: PyOpenColorIO.FileTransform, src: str) -> None
      :module: PyOpenColorIO


   .. py:method:: FileTransform.validate(self: PyOpenColorIO.Transform) -> None
      :module: PyOpenColorIO

      Will throw if data is not valid.


.. py:class:: FormatIterator
   :module: PyOpenColorIO.FileTransform
   :canonical: PyOpenColorIO.FileTransform.FormatIterator


   .. py:method:: FormatIterator.__getitem__(self: PyOpenColorIO.FileTransform.FormatIterator, arg0: int) -> tuple
      :module: PyOpenColorIO.FileTransform


   .. py:method:: FormatIterator.__iter__(self: PyOpenColorIO.FileTransform.FormatIterator) -> PyOpenColorIO.FileTransform.FormatIterator
      :module: PyOpenColorIO.FileTransform


   .. py:method:: FormatIterator.__len__(self: PyOpenColorIO.FileTransform.FormatIterator) -> int
      :module: PyOpenColorIO.FileTransform


   .. py:method:: FormatIterator.__next__(self: PyOpenColorIO.FileTransform.FormatIterator) -> tuple
      :module: PyOpenColorIO.FileTransform

