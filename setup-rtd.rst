How to set up your documentation on Read the Docs
=================================================

You will need to a working documentation repository for the following steps to work.

This guide assumes you're using :doc:`starter-pack`.
If your documentation repository is set up differently, you might need to adapt the described configuration to your setup.

Get access to Read the Docs
---------------------------

Go to `Read the Docs for Business <https://readthedocs.com/>`_ (``readthedocs.com``, **not** ``readthedocs.org``) and create an account.

Then get in touch with the `documentation team <https://chat.canonical.com/canonical/channels/documentation>`_ to be added to the Canonical organisation.
They will set up a team for your project.
(Note that this is a temporary solution, and a more structured way of granting access to Read the Docs is in the works.)


Create the project on Read the Docs
-----------------------------------

On `the Read the Docs dashboard <https://readthedocs.com/dashboard/>`_, create a new project.

* For a public Git repository, use the :guilabel:`Import a Project` button.
* For a private Git repository, or if you can't easily find the repository, use
  `the manual import <https://readthedocs.com/dashboard/import/manual/>`_.

Most fields are self-explanatory and you can leave the default values.
Check and update the following fields:

* Check the :guilabel:`Default branch` field.

  .. note::

     If your repository does not have a |wokeignore:rule=master| branch,
     and you don't specify the correct default branch, it will default to |wokeignore:rule=master-code| and will not be able to check out the repository and find the correct one.

     If this happens, the solution is to add a |wokeignore:rule=master-code| branch to the project until you're able to build it once, then specify the correct branch.

* Don't select the :guilabel:`Edit advanced project options` check box for now - you will need to edit those settings later anyway.
* Select the appropriate :guilabel:`Team` - this determines who gets admin access.

Click :guilabel:`Next`.
On the resulting page, select the **Admin** tab and update the following settings:

1. Select **Advanced Settings** in the navigation.
#. Select the :guilabel:`Privacy Level` for the project dashboard.
   In most cases, this should be private.
#. Select :guilabel:`Build pull requests for this project`.
#. Select the :guilabel:`Privacy level of Pull Requests`.
   For projects that are developed in the open, change this to public.
#. Change the :guilabel:`Documentation type` to ``Sphinx HtmlDir``.
#. Specify the path to the :guilabel:`Requirements file`.
   In the starter pack, this is :file:`.sphinx/requirements.txt`.
#. Click :guilabel:`Save`.

If you want your documentation to be accessible without logging in to Read the Docs, also change the following configuration:

1. Select **Edit Versions** in the navigation.
#. Click :guilabel:`Edit` for the latest version.
#. Set the :guilabel:`Privacy Level` to public.
#. Click :guilabel:`Save`.

Build and view the documentation
--------------------------------

In the project overview, click :guilabel:`Build version` to start a build.
You should see the build progressing, followed by a ``Build completed`` message.
If the build fails (but local builds work fine), you probably need to adapt some of the advanced project settings.

Click the :guilabel:`View Docs` button to see the built documentation.

.. |wokeignore:rule=master| replace:: master
.. |wokeignore:rule=master-code| replace:: ``master``
