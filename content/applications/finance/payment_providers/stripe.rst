======
Stripe
======

`Stripe <https://stripe.com/>`_ is a United States-based online payment solution provider, allowing
businesses to accept **credit cards** and other payment methods.

Link your Stripe Account with Odoo
==================================

.. seealso::
   - :ref:`payment_providers/add_new`

The method to acquire your credentials depends on your hosting type:

.. tabs::
   .. group-tab:: Odoo Online

      #. Go to the **eCommerce** or the **Sales** app and click on the *Activate Stripe* or the *Set
         payments* button on the onboarding banner.
      #. Fill in the requested information and submit the form.
      #. Confirm your email address when Stripe sends you a confirmation email.
      #. At the end of the process, you are redirected to Odoo. If you submitted all the requested
         information, you are all set and your payment provider is enabled.
<<<<<<< HEAD
||||||| parent of 59ccadeb5 (temp)
      #. You can continue to :ref:`stripe/local-payment-methods`.
=======
      #. Your can continue to :ref:`stripe/local-payment-methods`.
>>>>>>> 59ccadeb5 (temp)

      .. tip::
         To use your own API keys, :ref:`activate the Developer mode <developer-mode>` and
         :ref:`enable Stripe manually <payment_providers/add_new>`. You can then :ref:`Fill in your
         credentials <stripe/api_keys>`, :ref:`generate a webhook <stripe/webhook>` and enable the
         payment provider.

   .. group-tab:: Odoo.sh or On-premise

      #. Go to the **eCommerce** or the **Sales** app and click on the *Activate Stripe* or the *Set
         payments* button on the onboarding banner.
      #. Fill in the requested information and submit the form.
      #. Confirm your email address when Stripe sends you a confirmation email.
      #. At the end of the process, you are redirected to the payment provider **Stripe** on Odoo.
      #. :ref:`Fill in your credentials <stripe/api_keys>`.
      #. :ref:`Generate a webhook <stripe/webhook>`.
      #. Enable the payment provider.

.. tip::
   To connect your Stripe account after the onboarding is already completed, go to
   :menuselection:`Accounting --> Configuration --> Payment Providers --> Stripe` and click on the
   *Connect Stripe* button.

.. important::
   If you are testing Stripe (in **test mode**), change the **State** to *Test Mode*. We recommend
   doing this on a test Odoo database rather than on your main database.

.. _stripe/api_keys:

Fill in your credentials
------------------------

In case your **API Credentials** are required to connect with your Stripe account, these are the
credentials that must be completed:

- :ref:`Publishable Key <stripe/api_keys>`: The key solely used to identify the account with Stripe.
- :ref:`Secret Key <stripe/api_keys>`: The key to sign the merchant account with Stripe.
- :ref:`Webhook Signing Secret <stripe/webhook>`: When you enable your webhook on your Stripe
  account, this signing secret must be set to authenticate the messages sent from Stripe to Odoo.

To retrieve the publishable and secret keys, follow this `link to your API keys
<https://dashboard.stripe.com/account/apikeys>`_, or log into your Stripe dashboard and go to
:menuselection:`Developers --> API Keys --> Standard Keys`.

.. _stripe/webhook:

Generate a webhook
------------------

In case your **Webhook Signing Secret** is required to connect with your Stripe account, you can
create a webhook either automatically or manually.

.. tabs::
   .. tab:: Create the webhook automatically

      Make sure your :ref:`Publishable and Secret keys <stripe/api_keys>` are filled in, then click
      on the *Generate your Webhook* button.

   .. tab:: Create the webhook manually

      Visit the `webhooks page on Stripe <https://dashboard.stripe.com/webhooks>`_, or log into your
      Stripe dashboard and go to :menuselection:`Developers --> Webhooks`. Then, click on **Add
      endpoint** in your **Hosted endpoints** and insert the following data into the pop-up form:

      - | In the **Endpoint URL**, enter your Odoo database's URL followed by
        | `/payment/stripe/webhook`.
        | For example: `https://yourcompany.odoo.com/payment/stripe/webhook`
<<<<<<< HEAD
      - At the bottom of the form, click :guilabel:`+ Select events`, then:

        - In the :guilabel:`Charge` section, select :guilabel:`charge.refunded` and
          :guilabel:`charge.refund.updated`.
        - In the :guilabel:`Payment Intent` section, select
          :guilabel:`payment_intent.amount_capturable_updated`,
          :guilabel:`payment_intent.payment_failed`, :guilabel:`payment_intent.processing` and
          :guilabel:`payment_intent.succeeded`.
        - In the :guilabel:`Setup Intent` section, select :guilabel:`setup_intent.succeeded`.
        - In the :guilabel:`Charge` section, select :guilabel:`charge.refunded` and
          :guilabel:`charge.refund.updated`.
||||||| parent of 59ccadeb5 (temp)
      - At the bottom of the form, click :guilabel:`+ Select events`, then:

        - In the :guilabel:`Charge` section, select :guilabel:`charge.refunded` and
          :guilabel:`charge.refund.updated`.
        - In the :guilabel:`Payment Intent` section, select
          :guilabel:`payment_intent.amount_capturable_updated`,
          :guilabel:`payment_intent.payment_failed` and
          :guilabel:`payment_intent.succeeded`.
        - In the :guilabel:`Setup Intent` section, select :guilabel:`setup_intent.succeeded`.
=======
      - At the end of the form, you can **Select events** to listen to. Click on it and, in the
        **Checkout** section, select **checkout.session.completed**.
>>>>>>> 59ccadeb5 (temp)

        .. note::
           It is possible to select other events, but they are currently not processed by Odoo.

      When you click on **Add endpoint**, your Webhook is configured. You can then click on
      **reveal** to display your signing secret.

<<<<<<< HEAD
.. _stripe/express-checkout:

Enable express checkout
~~~~~~~~~~~~~~~~~~~~~~~

After ticking the :guilabel:`Allow Express Checkout` checkbox, **Google Pay** is enabled out of the
box, but **Apple Pay** requires extra steps: You must register your web domain with Apple. This can
be done either automatically from Odoo, or manually from Stripe.

.. tabs::
  .. tab:: Register automatically from Odoo

     #. Navigate to your payment provider and make sure that it is :guilabel:`enabled`.
     #. Go to the :guilabel:`Configuration` tab and click the :guilabel:`Enable Apple Pay`
        button. A notification shows that the web domain was successfully registered with Apple.

  .. tab:: Register manually from Stripe

     Visit the `Apple pay web domains page on Stripe
     <https://dashboard.stripe.com/settings/payments/apple_pay>`_, or log into your Stripe
     dashboard and go to :menuselection:`Settings --> Payments methods --> Apple Pay --> Configure
     --> Web domains`. Then, click :guilabel:`Add new domain` and insert the web domain of your
     Odoo database into the pop-up form. Odoo already hosts the verification file of Stripe. Click
     :guilabel:`Add` to register your web domain with Apple.

.. important::
   This operation must be repeated whenever your web domain changes.

.. seealso::
   - :ref:`payment_providers/features/express_checkout`
||||||| parent of 59ccadeb5 (temp)
.. _stripe/local-payment-methods:

Enable local payment methods
============================

Local payment methods are payment methods that are only available for certain merchants and
customers countries and currencies.

Odoo supports the following local payment methods:

- Bancontact
- EPS
- giropay
- iDEAL
- Przelewy24 (P24)

To enable some of these local payment methods with Stripe, go to
:menuselection:`Payment Providers --> Stripe --> Configuration` and add the desired payment methods
in the :guilabel:`Supported Payment Methods` field. If the desired payment method is already listed,
you don't have anything to do.

.. image:: stripe/stripe_enable_local_payment_method.png
   :align: center
   :alt: Select and add icons of the payment methods you want to enable

.. note::
   - If a payment method record does not exist in the database and its related local payment method is
     listed above, it is considered enabled with Stripe.
   - If a local payment method is not listed, it is not supported and cannot be enabled.

.. _stripe/express-checkout:

Enable express checkout
=======================

.. seealso::
   :ref:`payment_providers/features/express_checkout`

After ticking the :guilabel:`Allow Express Checkout` checkbox, **Google Pay** is enabled out of the
box, but **Apple Pay** requires extra steps: You must register your web domain with Apple. This can
be done either automatically from Odoo, or manually from Stripe.

.. tabs::
  .. tab:: Register automatically from Odoo

     #. Navigate to your payment provider and make sure that it is :guilabel:`enabled`.
     #. Go to the :guilabel:`Configuration` tab and click the :guilabel:`Enable Apple Pay`
        button. A notification shows that the web domain was successfully registered with Apple.

  .. tab:: Register manually from Stripe

     Visit the `Apple pay web domains page on Stripe
     <https://dashboard.stripe.com/settings/payments/apple_pay>`_, or log into your Stripe
     dashboard and go to :menuselection:`Settings --> Payments methods --> Apple Pay --> Configure
     --> Web domains`. Then, click :guilabel:`Add new domain` and insert the web domain of your
     Odoo database into the pop-up form. Odoo already hosts the verification file of Stripe. Click
     :guilabel:`Add` to register your web domain with Apple.

.. important::
   This operation must be repeated whenever your web domain changes.
=======
.. _stripe/local-payment-methods:

Enable local payment methods
============================

Local payment methods are payment methods that are only available for certain merchants and
customers countries and currencies.

Odoo supports the following local payment methods:

- Bancontact
- EPS
- giropay
- iDEAL
- Przelewy24 (P24)

To enable some of these local payment methods with Stripe, list them as supported payment icons. To
do so, go to :menuselection:`Payment Providers --> Stripe --> Configuration` and add the desired
payment methods in the **Supported Payment Icons** field. If the desired payment method is already
listed, you do not have anything to do.

.. image:: stripe/payments-config.png
   :alt: Select and add icons of the payment methods you want to enable

.. note::
   - If a payment method record does not exist in the database and its related local payment method
     is listed above, it is considered enabled with Stripe.
   - If a local payment method is not listed above, it is not supported and cannot be enabled.

.. seealso::
   - :doc:`../payment_providers`
>>>>>>> 59ccadeb5 (temp)
