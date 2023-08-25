=========
Documents
=========

**Odoo Documents** allows you to store, view and manage files within Odoo.

You can upload any type of file (max 64MB per file on Odoo Online), and organize them in various
workspaces.

.. seealso::
   - `Odoo Documents: product page <https://www.odoo.com/app/documents>`_
   - `Odoo Tutorials: Documents basics <https://www.odoo.com/slides/slide/documents-basics-674>`_
   - `Odoo Tutorials: Using Documents with your Accounting App
     <https://www.odoo.com/slides/slide/using-documents-with-your-accounting-app-675?fullscreen=1#>`_

Configuration
=============

By going to :menuselection:`Documents --> Configuration --> Settings`, you can enable the
centralization of files attached to a specific area of your activity. For example, by ticking
:guilabel:`Human Resources`, your HR documents are automatically available in the HR workspace,
while documents related to Payroll are automatically available in the Payroll sub-workspace . You
can change the default workspace by using the dropdown menu and edit its properties by clicking the
internal link button (:guilabel:`➔`).

.. image:: documents/files-centralization.png
   :align: center
   :alt: Enable the centralization of files attached to a specific area of your activity.

.. note::
   - If you enable the centralization of your accounting files and documents, it is necessary to
     click on :guilabel:`Journals` and define each journal independently to allow automatic
     synchronization.

     .. image:: documents/accounting-files-centralization.png
      :align: center
      :alt: Enable the centralization of files attached to your accounting.

   - If you select a new workspace, existing documents aren't moved. Only newly created documents
     will be found under the new workspace.

Workspaces
==========

Workspaces are hierarchical folders having their own set of tags and actions. Default workspaces
exist, but you can create your own by going to :menuselection:`Documents --> Configuration -->
Workspaces` and clicking on :guilabel:`Create`.

.. note::
   :guilabel:`Workspaces` and :guilabel:`Sub-workspaces` can be created, edited, or deleted by
   clicking on the gear icon :guilabel:`⚙` on the left menu.

.. image:: documents/sub-workspaces-creation.png
   :align: center
   :alt: Create sub-workspaces from the left menu

Tags
====

Tags are used within workspaces to add a level of differentiation between documents. They are
organized per category and filters can be used to sort them.

.. note::
   - The tags of a parent workspace apply to the child workspaces automatically.
   - Tags can be created and modified by going to :menuselection:`Configuration --> Tags`.
   - Tags can also be created, edited, or deleted, by clicking on the gear icon :guilabel:`⚙`, on
     the left menu.

Documents management
====================

When selecting a document, the right panel displays different options. On the top, additional
options might be available: :guilabel:`Download`, :guilabel:`Share`, :guilabel:`Replace`,
:guilabel:`Lock` or :guilabel:`Split`. It is also possible to :guilabel:`Open chatter` or
:guilabel:`Archive` the document.

.. image:: documents/right-panel-options.png
   :align: center
   :alt: right panel options

Then, you can modify the name of your file by clicking on :guilabel:`Document`. A
:guilabel:`Contact` or an :guilabel:`Owner` can be assigned. The related :guilabel:`Workspace` can
be modified and it is possible to access the related :guilabel:`Journal Entry` or to add
:guilabel:`Tags`.

.. note::
   - The :guilabel:`Contact` is the person related to the document and assigned to it. He can only
     view the document and not modify it. I.e.: an existing supplier in your database is the contact
     for their bill.
   - The person who creates a document is, by default :guilabel:`Owner` of it and has complete
     rights to the document. It is possible to replace the owner of a document. I.e.: an employee
     must be owner of a document to be able to see it in "My Profile".

Finally, different :ref:`Actions <documents/workflow-actions>` are available at the bottom of the
right panel, depending on the workspace where your document is stored.

Split documents
---------------

Select the document you want to split, and click the :guilabel:`Split` icon. A new page opens and
displays all the pages of the document.

The scissors between pages indicate where the split will occur. Click on the scissors if you
don't want to split your document between two specific pages.

.. image:: documents/split-pdf.png
   :align: center
   :alt: split your documents

.. note::

   To merge documents, select them from your dashboard and click the :guilabel:`Split` icon. Then,
   click on the scissors between pages to remove the cut, and click :guilabel:`Split`. Your
   documents are now merged.

Additional features
-------------------

Select a specific workspace and click on the arrow next to the :guilabel:`Upload` button to access
additional features:

Request
~~~~~~~

To request a missing file, click :guilabel:`Request`. Add the :guilabel:`Document name`, select the
person you need it from in the :guilabel:`Request to` field, fill in the :guilabel:`Due date`, add
the :guilabel:`Workspace` the document should belong to, and eventually add :guilabel:`Tags` and a
:guilabel:`Note`. A file reflecting the missing document is created in the workspace.

To see all the documents you requested, go to the :guilabel:`Activity` view and to the
:guilabel:`Requested Document` column.

.. Note::

   To send a **reminder email** to all users you are waiting a document from, click on ⋮, and
   :guilabel:`Document Request: Reminder`.

   Click on a date to see the details of a specific request. You can update it by clicking on the
   pen icon, :guilabel:`Preview` the content of the reminder email, or :guilabel:`Send Now` to send
   a reminder email.

   .. image:: documents/reminder-email.png
      :align: center
      :alt: send a reminder email from the Activity view

Add a link
~~~~~~~~~~

To add a url to your documents dashboard, click on :guilabel:`Add a link`, enter the :guilabel:`URL`
and :guilabel:`Name` it. A file reflecting the url is created.

Share
~~~~~

Click :guilabel:`Share` to share the content of your workspace. A :guilabel:`URL` is available; you
can :guilabel:`copy` it to share it with the users you want so they can directly access your
document workspace and its content. Tick the :guilabel:`Include Sub Folders` box if you also want
to share subfolders. :guilabel:`Name` the share link and set a validity date for the url by filling
the :guilabel:`Valid Until` field. You can also enable users to :guilabel:`Download` or
:guilabel:`Download and Upload` documents.

New spreadsheet
~~~~~~~~~~~~~~~

To create a new spreadsheet, click :guilabel:`New Spreadsheet`. You can select a
:guilabel:`Blank spreadsheet` or an existing one.

.. _documents/workflow-actions:

Workflow actions
================

Workflow actions help you streamline the management of your documents and your overall business
operations. These are automated actions that can be created and customized for each workspace. For
example, create documents, process bills, sign, organize files, add tags to a file or move it to
another workspace with a single click etc. These workflow actions appear on the right panel when it
meets the criteria you set.

Create workflow actions
-----------------------

To create workflow actions, go to :menuselection:`Documents --> Configuration --> Actions` and then
click on :guilabel:`Create`.

.. note::
   An action applies to all :guilabel:`Child Workspaces` under the :guilabel:`Parent Workspace` you
   selected.

Set the conditions
------------------

You can :guilabel:`Create` a new :guilabel:`Action` or edit an existing one. You can define the
:guilabel:`Action Name` and then set the conditions that trigger the appearance of the action button
(:guilabel:`▶`) on the right-side panel when selecting a file.

There are three basic types of conditions you can set:

#. :guilabel:`Tags`: you can both use the :guilabel:`Contains` and :guilabel:`Does not contain`
   conditions, meaning the files *must have* or *mustn't have* the tags set here.

#. :guilabel:`Contact`: the files must be associated with the contact set here.

#. :guilabel:`Owner`: the files must be associated with the owner set here.

.. image:: documents/basic-condition-example.png
   :align: center
   :alt: Example of a workflow action's basic condition in Odoo Documents

.. tip::
   If you don't set any conditions, the action button appears for all files located inside the
   selected workspace.

Advanced condition type: domain
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

.. important::
   It is recommended to have some knowledge of Odoo development to properly configure *Domain*
   filters.

To access the *Domain* condition, the :ref:`developer mode <developer-mode>` needs to be activated.
Once that's done, select the :guilabel:`Domain` condition type, and click on :guilabel:`Add Filter`.

.. image:: documents/activate-domain-condition.png
   :align: center
   :alt: Activating the domain condition type in Odoo Documents

To create a rule, you typically select a :guilabel:`field`, an :guilabel:`operator`, and a
:guilabel:`value`. For example, if you want to add a workflow action to all the PDF files inside a
workspace, set the :guilabel:`field` to *Mime Type*, the :guilabel:`operator` to *contains*, and the
:guilabel:`value` to *pdf*.

.. image:: documents/domain-condition-example.png
   :align: center
   :alt: Example of a workflow action's domain condition in Odoo Documents

Click on :guilabel:`Add node` (plus-circle icon) and :guilabel:`Add branch` (ellipsis icon) to add
conditions and sub-conditions. You can then specify if your rule should match :guilabel:`ALL` or
:guilabel:`ANY` conditions. You can also edit the rule directly using the :guilabel:`Code editor`.

.. image:: documents/use-domain-condition.png
   :align: center
   :alt: Add a node or a branch to a workflow action's condition in Odoo Documents

Configure the actions
---------------------

Select the :guilabel:`Actions` tab to set up your action. You can simultaneously:

- **Set Contact**: add a contact to the file, or replace an existing contact with a new one.
- **Set Owner**: add an owner to the file, or replace an existing owner with a new one.
- **Move to Workspace**: move the file to any workspace.
- **Create**: create one of the following items attached to the file in your database:

   - **Link to record**: ??
   - **Product template**: create a product you can edit directly.
   - **Task**: create a Project task you can edit directly.
   - **Signature PDF template**: create a new Sign template to send out.
   - **PDF to sign**: ??
   - **Applicant**: create a new HR application you can edit directly.
   - **Vendor bill**: create a vendor bill using OCR and AI to scrape information from the file
     content.
   - **Customer invoice**: create a customer invoice using OCR and AI to scrape information from
     the file.
   - **Vendor credit note**: create a vendor credit note using OCR and AI to scrape information
     from the file.
   - **Credit note**: create a customer credit note using OCR and AI to scrape information from
     the file.
   - **Miscellaneous Operations**: ??
   - **Bank Statement**: ??
   - **Expense**: create an expense automatically based on a file's content.

- **Set Tags**: add, remove, and replace any number of tags.
- **Activities - Mark all as Done**: mark all activities linked to the file as done.
- **Activities - Schedule Activity**: create a new activity linked to the file as configured in
  the action. You can choose to set the activity on the document owner.

.. image:: documents/workflow-action-example.png
   :align: center
   :alt: Example of a workflow action Odoo Documents

Digitize documents with AI and optical character recognition (OCR)
==================================================================

Documents available in the Finance workspace can be digitized. Select the document you want to
digitize, click on :guilabel:`Create Bill`, :guilabel:`Create Customer Invoice` or
:guilabel:`Create credit note`, and then click on :guilabel:`Send for Digitization`.

.. seealso::
   :doc:`AI-powered document digitization <../finance/accounting/vendor_bills/invoice_digitization>`
