=======================================
Website analytics with Google Analytics
=======================================

To follow your website's traffic with Google Analytics:

#. `Create a Google Analytics account <https://www.google.com/analytics/>`_ if you don't have any.
#. `Create a Google Analytics property
   <https://support.google.com/analytics/answer/9304153?hl=en/&visit_id=638278591144564289-3612494643&rd=2>`_.
#. Go through the property creation process and accept the Google Analytics Terms of Service
   Agreement.
#. When you reach the **Data collection** step, choose the platform :guilabel:`Web`.

   .. image:: google_analytics/GA_platform.png
      :alt: Choose a platform for your Google Analytics property.

#. Set up your data stream: Specify your :guilabel:`Website URL` and a :guilabel:`Stream name`, then
   click :guilabel:`Create stream`.
#. Copy the :guilabel:`Measurement ID`.

   .. image:: google_analytics/GA_measurement-id.png
      :alt: Measurement ID in Google Analytics.

#. In Odoo, go to :menuselection:`Website --> Configuration --> Settings`.
#. In the :guilabel:`SEO` section, select the :guilabel:`Google Analytics` check box, then paste the
   :guilabel:`Measurement ID`.

.. note::
   If you have :doc:`multiple websites <../configuration/multi_website>` with separate domains, it
   is recommended to create one property per domain. To add a new property to your Google Analytics
   account, sign in to your Google Analytics account and click the gear icon in the bottom-left
   corner of the page to access the Admin page. Then, click :guilabel:`+ Create Property` in the
   :guilabel:`Property` column and go through the steps described above. In Odoo, in the
   **Website settings**, make sure to select the website in the :guilabel:`Settings of Website`
   field before pasting the :guilabel:`Measurement ID`.

   .. image:: google_analytics/GA_add-property.png
      :alt: Add a new property to your Google Analytics account.

To make your first steps in Google Analytics, refer to the `Google Documentation
<https://support.google.com/analytics/answer/1008015?hl=en/>`_.

.. seealso::
   :doc:`google_analytics_dashboard`
