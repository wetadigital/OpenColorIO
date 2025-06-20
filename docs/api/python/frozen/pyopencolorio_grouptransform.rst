..
  SPDX-License-Identifier: CC-BY-4.0
  Copyright Contributors to the OpenColorIO Project.
  Do not edit! This file was automatically generated by share/docs/frozendoc.py.

.. py:class:: GroupTransform
   :module: PyOpenColorIO
   :canonical: PyOpenColorIO.GroupTransform


   .. py:method:: GroupTransform.GetWriteFormats() -> PyOpenColorIO.GroupTransform.WriteFormatIterator
      :module: PyOpenColorIO
      :staticmethod:


   .. py:method:: GroupTransform.__init__(*args, **kwargs)
      :module: PyOpenColorIO

      Overloaded function.

      1. __init__(self: PyOpenColorIO.GroupTransform) -> None

      2. __init__(self: PyOpenColorIO.GroupTransform, transforms: list[PyOpenColorIO.Transform] = [], direction: PyOpenColorIO.TransformDirection = <TransformDirection.TRANSFORM_DIR_FORWARD: 0>) -> None


   .. py:method:: GroupTransform.appendTransform(self: PyOpenColorIO.GroupTransform, transform: PyOpenColorIO.Transform) -> None
      :module: PyOpenColorIO

      Adds a transform to the end of the group.


   .. py:method:: GroupTransform.getDirection(self: PyOpenColorIO.Transform) -> PyOpenColorIO.TransformDirection
      :module: PyOpenColorIO


   .. py:method:: GroupTransform.getFormatMetadata(self: PyOpenColorIO.GroupTransform) -> PyOpenColorIO.FormatMetadata
      :module: PyOpenColorIO


   .. py:method:: GroupTransform.getTransformType(self: PyOpenColorIO.Transform) -> PyOpenColorIO.TransformType
      :module: PyOpenColorIO


   .. py:method:: GroupTransform.prependTransform(self: PyOpenColorIO.GroupTransform, transform: PyOpenColorIO.Transform) -> None
      :module: PyOpenColorIO

      Add a transform at the beginning of the group.


   .. py:method:: GroupTransform.setDirection(self: PyOpenColorIO.Transform, direction: PyOpenColorIO.TransformDirection) -> None
      :module: PyOpenColorIO

      Note that this only affects the evaluation and not the values stored in the object.


   .. py:method:: GroupTransform.validate(self: PyOpenColorIO.Transform) -> None
      :module: PyOpenColorIO

      Will throw if data is not valid.


   .. py:method:: GroupTransform.write(*args, **kwargs)
      :module: PyOpenColorIO

      Overloaded function.

      1. write(self: PyOpenColorIO.GroupTransform, formatName: str, fileName: str, config: PyOpenColorIO.Config = None) -> None

      Write the transforms comprising the group to the stream.

      Writing (as opposed to Baking) is a lossless process. An exception is thrown if the processor cannot be losslessly written to the specified file format. Transforms such as :ref:`FileTransform` or :ref:`ColorSpaceTransform` are resolved into write-able simple transforms using the config and context. Supported formats include CTF, CLF, and CDL. All available formats can be listed with the following: .. code-block:: cpp

          // What are the allowed writing output formats?
          std::ostringstream formats;
          formats << "Formats to write to: ";
          for (int i = 0; i < :ref:`GroupTransform::GetNumWriteFormats`(); ++i)
          {
             if (i != 0) formats << ", ";
             formats << :ref:`GroupTransform::GetFormatNameByIndex`(i);
             formats << " (." << GroupTransform::GetFormatExtensionByIndex(i) << ")";
          }

      2. write(self: PyOpenColorIO.GroupTransform, formatName: str, config: PyOpenColorIO.Config = None) -> str

      Write the transforms comprising the group to the stream.

      Writing (as opposed to Baking) is a lossless process. An exception is thrown if the processor cannot be losslessly written to the specified file format. Transforms such as :ref:`FileTransform` or :ref:`ColorSpaceTransform` are resolved into write-able simple transforms using the config and context. Supported formats include CTF, CLF, and CDL. All available formats can be listed with the following: .. code-block:: cpp

          // What are the allowed writing output formats?
          std::ostringstream formats;
          formats << "Formats to write to: ";
          for (int i = 0; i < :ref:`GroupTransform::GetNumWriteFormats`(); ++i)
          {
             if (i != 0) formats << ", ";
             formats << :ref:`GroupTransform::GetFormatNameByIndex`(i);
             formats << " (." << GroupTransform::GetFormatExtensionByIndex(i) << ")";
          }


.. py:class:: WriteFormatIterator
   :module: PyOpenColorIO.GroupTransform
   :canonical: PyOpenColorIO.GroupTransform.WriteFormatIterator


   .. py:method:: WriteFormatIterator.__getitem__(self: PyOpenColorIO.GroupTransform.WriteFormatIterator, arg0: int) -> tuple
      :module: PyOpenColorIO.GroupTransform


   .. py:method:: WriteFormatIterator.__iter__(self: PyOpenColorIO.GroupTransform.WriteFormatIterator) -> PyOpenColorIO.GroupTransform.WriteFormatIterator
      :module: PyOpenColorIO.GroupTransform


   .. py:method:: WriteFormatIterator.__len__(self: PyOpenColorIO.GroupTransform.WriteFormatIterator) -> int
      :module: PyOpenColorIO.GroupTransform


   .. py:method:: WriteFormatIterator.__next__(self: PyOpenColorIO.GroupTransform.WriteFormatIterator) -> tuple
      :module: PyOpenColorIO.GroupTransform


.. py:class:: TransformIterator
   :module: PyOpenColorIO.GroupTransform
   :canonical: PyOpenColorIO.GroupTransform.TransformIterator


   .. py:method:: TransformIterator.__getitem__(self: PyOpenColorIO.GroupTransform.TransformIterator, arg0: int) -> PyOpenColorIO.Transform
      :module: PyOpenColorIO.GroupTransform


   .. py:method:: TransformIterator.__iter__(self: PyOpenColorIO.GroupTransform.TransformIterator) -> PyOpenColorIO.GroupTransform.TransformIterator
      :module: PyOpenColorIO.GroupTransform


   .. py:method:: TransformIterator.__len__(self: PyOpenColorIO.GroupTransform.TransformIterator) -> int
      :module: PyOpenColorIO.GroupTransform


   .. py:method:: TransformIterator.__next__(self: PyOpenColorIO.GroupTransform.TransformIterator) -> PyOpenColorIO.Transform
      :module: PyOpenColorIO.GroupTransform

