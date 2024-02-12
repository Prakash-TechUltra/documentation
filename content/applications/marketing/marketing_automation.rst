:show-content:

====================
Marketing Automation
====================

The Odoo *Marketing Automation* application unlocks a range of actions that can be automated within
an Odoo database. While the application is designed to be user-friendly for quickly creating,
launching, and reviewing marketing campaigns, it also provides advanced features to automate manual
and repetitive tasks throughout the database.

*Marketing Automation* enables users to create dynamic campaigns with actions that automatically
occur within a defined duration, such as sending a series of timed mass emails or engaging with
leads based on their interactions.

Get started by creating a :ref:`new campaign from scratch or with a campaign template
<marketing_automation/campaigns>`.

.. seealso::
   `Odoo Tutorials: Marketing <https://www.odoo.com/slides/marketing-27>`_

.. cards::

   .. card:: Target an audience
      :target: marketing_automation/target_audience

      Configure the target audience for a campaign.

   .. card:: Workflow activities
      :target: marketing_automation/workflow_activities

      Define the activities that occur within a campaign.

   .. card:: Testing/running campaigns
      :target: marketing_automation/testing_running

      Launch a test or run a campaign.

   .. card:: Campaign metrics
      :target: marketing_automation/understanding_metrics

      Review the metrics of a campaign.

Configuration
=============

To install the *Marketing Automation* application, navigate to :menuselection:`Apps` and search for
`Marketing Automation`. In the list of results, click the :guilabel:`Activate` button on the
:guilabel:`Marketing Automation` application to install it.

.. important::
   Installing the *Marketing Automation* application also installs the :doc:`Email Marketing
   <email_marketing>` application as dependency.

   Additionally, install the :doc:`CRM <../sales/crm>` and :doc:`SMS Marketing <sms_marketing>`
   applications to access all of the features available in *Marketing Automation*.

   The following documentation assumes that all three of these dependencies are installed on the
   database.

.. _marketing_automation/campaigns:

Campaigns
=========

A *campaign* consists of a target audience and a workflow containing activities that are
automatically executed to a specific group of records based on predefined filters, triggers and
durations of activities.

A new campaign can be created from scratch or from a template. To create a campaign, navigate to the
:menuselection:`Marketing Automation` application from the main Odoo dashboard to open the
:guilabel:`Campaigns` dashboard. From here, click the :guilabel:`New` button to reveal a new
campaign form.

.. _marketing-automation/campaign-templates:

Campaign templates
------------------

Odoo provides six campaign templates to help users get started. The campaign template cards only
display while there are no existing campaigns in the database. Once a campaign has been created, the
template cards on the *Campaigns* dashboard are replaced with a Kanban view of the existing
campaigns.

To get started with a template, navigate to the :menuselection:`Marketing Automation` application
from the main Odoo dashboard to open the :guilabel:`Campaigns` dashboard, which displays six
campaign template cards:

- | :guilabel:`Tag Hot Contacts`
  | :guilabel:`Send a welcome email to contacts and tag them if they click it.`
- | :guilabel:`Welcome Flow`
  | :guilabel:`Send a welcome email to new subscribers, remove the address that bounced.`
- | :guilabel:`Double Opt-in`
  | :guilabel:`Send an email to new recipients to confirm their consent.`
- | :guilabel:`Commercial prospection`
  | :guilabel:`Send a free catalog and follow-up according to reactions.`
- | :guilabel:`Schedule Calls`
  | :guilabel:`If a lead is created for existing contact, schedule a call with their salesperson.`
- | :guilabel:`Prioritize Hot leads`
  | :guilabel:`Send an email to new leads and assign them a high priority if they open it.`

These templates are designed to be used as starting points for creating new campaigns. Click one of
the template cards to open the campaign form.

.. tip::
   To display the campaign template cards again after a campaign has been created, type the name of
   a campaign that does not exist in the database into the :guilabel:`Search...` bar, then press
   :kbd:`Enter`.

   For example, searching for `empty` displays the campaign template cards again as long as there is
   not a campaign with the name "empty" in the database.

Targets & filters
=================

The *Target* and *Filter* section of the campaign form, also referred to as the domain, contains the
fields used to define the target audience for the campaign's reach (i.e., records).

Records
-------

The contacts in the system that fit the specified criteria for a campaign are referred to as
*records*.

The number of records that are displayed next to the campaign *Filter* represents the total number
of records the campaign is targeting.

Participants
------------

The records that are engaged by the campaign are referred to as *participants*.

The number of participants engaged in a test run are shown in the *Tests #* smart button. The number
of participants engaged in a running or stopped campaign are shown in the *Participants #* smart
button.

.. seealso::
   :doc:`marketing_automation/target_audience`

Workflow
========

A *workflow* consists of an activity, many activities, and/or a sequence of activities organized in
a campaign. A campaign's workflow is defined in the *Workflow* section of the *Campaign* form.

Activities
----------

*Activities* are the methods of communication or server actions, organized in a *Workflow*, that are
executed within a campaign. Once running, each activity displays the number of participants that
are engaged by the activity as *Success* and *Rejected* counts.

The following are the available activities in the *Marketing Automation* application:

- *Email*: send an email to the target audience.
- *SMS*: send an SMS to the target audience.
- *Server Action*: executes an automated action.

.. seealso::
   :doc:`marketing_automation/workflow_activities`

Testing & running
=================

Once a campaign has been created, it can be tested to ensure the workflow is functioning as
expected. After testing, the campaign can be launched to start engaging the target audience.

.. seealso::
   :doc:`marketing_automation/testing_running`

Reporting
=========

A range of reporting metrics are available to measure the success of each campaign. The following
are the reporting options in the *Reporting* menu of the *Marketing Automation* app:

- *Link Tracker*: displays the metrics of links to track the number of clicks.
- *Traces*: displays the results of all activities from all campaigns.
- *Participants*: displays an overview of the participants of all campaigns.

Additionally, each activity within the workflow of a campaign displays it's engagement metrics.

.. seealso::
   :doc:`marketing_automation/understanding_metrics`

.. toctree::
   :titlesonly:

   marketing_automation/target_audience
   marketing_automation/workflow_activities
   marketing_automation/testing_running
   marketing_automation/understanding_metrics
