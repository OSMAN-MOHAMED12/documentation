==============
Quality checks
==============

.. |QCP| replace:: :abbr:`QCP (Quality Control Point)`

Quality checks are manual inspections conducted by employees, and are used to ensure the quality of
products. A quality check can be conducted for a single product, or multiple products within the
same inventory operation or manufacturing order.

Using a Quality Control Point (QCP), it is possible to create quality checks automatically at
regular intervals. A |QCP| can be configured to create quality checks for specific products or
operations, or a combination of both. For a full explanation of how to create and configure a |QCP|,
see the documentation on :ref:`Quality Control Points
<manufacturing/quality_control/quality-control-points>`.

While quality checks are most commonly created through a |QCP|, it is also possible to manually
create a single quality check. Doing so may be necessary if quality checks need to be conducted
outside of those created at regular intervals by a |QCP|.

Manual quality check
====================

To manually create a single quality check, navigate to :menuselection:`Quality --> Quality Control
--> Quality Checks`, and click :guilabel:`New`. On the new Quality Check form, begin by selecting an
option from the :guilabel:`Control per` drop-down menu, either :guilabel:`Operation`,
:guilabel:`Product`, or :guilabel:`Quantity`.

Select :guilabel:`Operation` to request a check for an entire operation (ex. delivery order) and all
products within it. Select :guilabel:`Product` to request a check for every unit of a product that
is part of an operation (ex. every unit of a product within a delivery order).

Select :guilabel:`Quantity` to request a check for every quantity of a product that is part of an
operation (ex. one check for five units of a product within a delivery order). Selecting
:guilabel:`Quantity` also causes a :guilabel:`Lot/Serial` drop-down field to appear, from which can
be selected a specific lot or serial number that the quality check should be conducted for.

Next, select an inventory operation from the :guilabel:`Picking` drop-down menu or a manufacturing
order from the :guilabel:`Production Order` drop-down menu. This is necessary because Odoo needs to
know which operation the quality check is being conducted for.

If the quality check should be assigned to a specific |QCP|, select it from the :guilabel:`Control
Point` drop-down menu. This is useful if the quality check is being created manually but should
still be recognized as belonging to a specific |QCP|.

Select a quality check type from the :guilabel:`Type` drop-down field:
- :guilabel:`Instructions` provides specific instructions for how to conduct the quality check.
- :guilabel:`Take a Picture` requires a picture to be attached to the check before the check can be
completed.
- :guilabel:`Pass - Fail` is used when the product being checked must meet a certain criteria to
pass the check.
- Selecting :guilabel:`Measure` causes a :guilabel:`Measure` input field to appear, in which a
measurement must be entered before the check can be completed.
- Selecting :guilabel:`Worksheet` causes a :guilabel:`Quality Template` drop-down field to appear,
from which can be selected a quality worksheet that must be filled out to complete the check.

In the :guilabel:`Team` field, select the quality team that is responsible for the quality check. In
the :guilabel:`Company` field, select the company that owns the product being inspected.

On the :guilabel:`Notes` tab at the bottom of the form, enter any relevant instructions in the
:guilabel:`Instructions` text entry box (ex. attach a picture of the product). Add any other
information that needs to be included in the :guilabel:`Notes` text entry field.

Process quality check
=====================

Quality checks are most commonly processed by selecting the :guilabel:`Quality Checks` button on an
inventory operation or manufacturing order, or within the tablet view for a specific work order.
However, it is also possible to process a quality check directly on the check itself.

To process a quality check on the check itself, begin by navigating to :menuselection:`Quality -->
Quality Control --> Quality Checks`, and select a Quality Check. Complete any actions required to
fulfill the quality check.

If the criteria of the quality check has been met, click the :guilabel:`Pass` button at the top left
of the screen. If the criteria of the check has not been met, click the :guilabel:`Fail` button
instead.
