..
  SPDX-License-Identifier: CC-BY-4.0
  Copyright Contributors to the OpenColorIO Project.
  Do not edit! This file was automatically generated by share/docs/frozendoc.py.

.. py:class:: ViewingRules
   :module: PyOpenColorIO
   :canonical: PyOpenColorIO.ViewingRules

   :ref:`ViewingRules`

   Viewing Rules allow config authors to filter the list of views an application should offer based on the color space of an image. For example, a config may define a large number of views but not all of them may be appropriate for use with all color spaces. E.g., some views may be intended for use with scene-linear color space encodings and others with video color space encodings.

   Each rule has a name key for applications to refer to the rule. Name values must be unique (using case insensitive comparison). Viewing Rules may also have the following keys:

   - colorspaces: Either a single colorspace name or a list of names.
   - encodings: One or more strings to be found in the colorspace's encoding attribute. Either this attribute or colorspaces must be present, but not both.
   - custom : Allows arbitrary key / value string pairs, similar to :ref:`FileRules`.

   Getters and setters are using the rule position, they will throw if the position is not valid.


   .. py:method:: ViewingRules.__init__(self: PyOpenColorIO.ViewingRules) -> None
      :module: PyOpenColorIO

      Creates :ref:`ViewingRules` for a :ref:`Config`.


   .. py:method:: ViewingRules.addColorSpace(self: PyOpenColorIO.ViewingRules, ruleIndex: int, colorSpaceName: str) -> None
      :module: PyOpenColorIO

      Add colorspace name. Will throw if:

      - RuleIndex is invalid.
      - :ref:`getNumEncodings` is not 0.


   .. py:method:: ViewingRules.addEncoding(self: PyOpenColorIO.ViewingRules, ruleIndex: int, encodingName: str) -> None
      :module: PyOpenColorIO

      Add encoding name. Will throw if:

      - RuleIndex is invalid.
      - :ref:`getNumColorSpaces` is not 0.


   .. py:method:: ViewingRules.getColorSpaces(self: PyOpenColorIO.ViewingRules, ruleIndex: int) -> PyOpenColorIO.ViewingRules.ViewingRuleColorSpaceIterator
      :module: PyOpenColorIO


   .. py:method:: ViewingRules.getCustomKeyName(self: PyOpenColorIO.ViewingRules, ruleIndex: int, key: int) -> str
      :module: PyOpenColorIO

      Get name of key. Will throw if ruleIndex or keyIndex is invalid.


   .. py:method:: ViewingRules.getCustomKeyValue(self: PyOpenColorIO.ViewingRules, ruleIndex: int, key: int) -> str
      :module: PyOpenColorIO

      Get value for the key. Will throw if ruleIndex or keyIndex is invalid.


   .. py:method:: ViewingRules.getEncodings(self: PyOpenColorIO.ViewingRules, ruleIndex: int) -> PyOpenColorIO.ViewingRules.ViewingRuleEncodingIterator
      :module: PyOpenColorIO


   .. py:method:: ViewingRules.getIndexForRule(self: PyOpenColorIO.ViewingRules, ruleName: str) -> int
      :module: PyOpenColorIO

      Get the index from the rule name. Will throw if there is no rule named ruleName.


   .. py:method:: ViewingRules.getName(self: PyOpenColorIO.ViewingRules, ruleIndex: int) -> str
      :module: PyOpenColorIO

      Get name of the rule. Will throw if ruleIndex is invalid.


   .. py:method:: ViewingRules.getNumCustomKeys(self: PyOpenColorIO.ViewingRules, ruleIndex: int) -> int
      :module: PyOpenColorIO

      Get number of key/value pairs. Will throw if ruleIndex is invalid.


   .. py:method:: ViewingRules.getNumEntries(self: PyOpenColorIO.ViewingRules) -> int
      :module: PyOpenColorIO


   .. py:method:: ViewingRules.insertRule(self: PyOpenColorIO.ViewingRules, ruleIndex: int, name: str) -> None
      :module: PyOpenColorIO

      Insert a rule at a given ruleIndex.

      Rule currently at ruleIndex will be pushed to index: ruleIndex + 1. If ruleIndex is ViewingRules::getNumEntries, a new rule will be added at the end. Will throw if:
      - RuleIndex is invalid (must be less than or equal to ViewingRules::getNumEntries).
      - RuleName already exists.


   .. py:method:: ViewingRules.removeColorSpace(self: PyOpenColorIO.ViewingRules, ruleIndex: int, colorSpaceIndex: int) -> None
      :module: PyOpenColorIO

      Remove colorspace. Will throw if ruleIndex or colorSpaceIndex is invalid.


   .. py:method:: ViewingRules.removeEncoding(self: PyOpenColorIO.ViewingRules, ruleIndex: int, encodingIndex: int) -> None
      :module: PyOpenColorIO

      Remove encoding. Will throw if ruleIndex or encodingIndex is invalid.


   .. py:method:: ViewingRules.removeRule(self: PyOpenColorIO.ViewingRules, ruleIndex: int) -> None
      :module: PyOpenColorIO

      Remove a rule. Throws if ruleIndex is not valid.


   .. py:method:: ViewingRules.setCustomKey(self: PyOpenColorIO.ViewingRules, ruleIndex: int, key: str, value: str) -> None
      :module: PyOpenColorIO

      Adds a key/value or replace value if key exists. Setting a NULL or an empty value will erase the key. Will throw if ruleIndex is invalid.


.. py:class:: ViewingRuleColorSpaceIterator
   :module: PyOpenColorIO.ViewingRules
   :canonical: PyOpenColorIO.ViewingRules.ViewingRuleColorSpaceIterator


   .. py:method:: ViewingRuleColorSpaceIterator.__getitem__(self: PyOpenColorIO.ViewingRules.ViewingRuleColorSpaceIterator, arg0: int) -> str
      :module: PyOpenColorIO.ViewingRules


   .. py:method:: ViewingRuleColorSpaceIterator.__iter__(self: PyOpenColorIO.ViewingRules.ViewingRuleColorSpaceIterator) -> PyOpenColorIO.ViewingRules.ViewingRuleColorSpaceIterator
      :module: PyOpenColorIO.ViewingRules


   .. py:method:: ViewingRuleColorSpaceIterator.__len__(self: PyOpenColorIO.ViewingRules.ViewingRuleColorSpaceIterator) -> int
      :module: PyOpenColorIO.ViewingRules


   .. py:method:: ViewingRuleColorSpaceIterator.__next__(self: PyOpenColorIO.ViewingRules.ViewingRuleColorSpaceIterator) -> str
      :module: PyOpenColorIO.ViewingRules


.. py:class:: ViewingRuleEncodingIterator
   :module: PyOpenColorIO.ViewingRules
   :canonical: PyOpenColorIO.ViewingRules.ViewingRuleEncodingIterator


   .. py:method:: ViewingRuleEncodingIterator.__getitem__(self: PyOpenColorIO.ViewingRules.ViewingRuleEncodingIterator, arg0: int) -> str
      :module: PyOpenColorIO.ViewingRules


   .. py:method:: ViewingRuleEncodingIterator.__iter__(self: PyOpenColorIO.ViewingRules.ViewingRuleEncodingIterator) -> PyOpenColorIO.ViewingRules.ViewingRuleEncodingIterator
      :module: PyOpenColorIO.ViewingRules


   .. py:method:: ViewingRuleEncodingIterator.__len__(self: PyOpenColorIO.ViewingRules.ViewingRuleEncodingIterator) -> int
      :module: PyOpenColorIO.ViewingRules


   .. py:method:: ViewingRuleEncodingIterator.__next__(self: PyOpenColorIO.ViewingRules.ViewingRuleEncodingIterator) -> str
      :module: PyOpenColorIO.ViewingRules

