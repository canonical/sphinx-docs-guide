How to set up your documentation on Read the Docs
=================================================

You will need to a working documentation repository for the following steps to work.


Create the project on Read the Docs
----------------------------------------

On `the Read the Docs Dashboard <https://readthedocs.com/dashboard/>`_, create a new project.

* for a public Git repository, use the **Import** button
* for a private Git repository, or if you can't easily find the repository, use
  the `manual import <https://readthedocs.com/dashboard/import/manual/>`_

..  admonition:: When importing your project, make sure that you check the *Default branch*
	field.

	If your repository does not have a |wokeignore:rule=master| branch,
        and you don't specify the correct default branch, it will default to |wokeignore:rule=master-code| and will not be able to check out the repository and find the correct one.

        If this does happen, the solution is to add a |wokeignore:rule=master-code| branch to the project until you're able to build it once, then specify the correct branch.

Select the appropriate *Team* - this determines who gets admin access.

Leave the *Advanced project options* alone for now.

Hit **Next**.

You should see a message: *Successfully added deploy key to GitHub project.*

Hit **Build version**. You should see the build progressing, then a *Build completed* message.

Hit **View Docs** - which should take you to the built documentation.


Check the settings on the Dashboard
------------------------------------

Back on the Dashboard for the project, hit **Admin**. Most of the settings are reasonably self-explanatory.

* *Edit versions*: Your *Latest* version will be *Private* by default - you
  can change that to *Public* if appropriate.

* *Advanced settings*:

  * If you don't need multiple languages or versions right now, select
    the *Single version* option.
  * For *Documentation type*, choose ``SphinxHtmlDir`` (this creates nicer URLs,
    without the ``.html`` suffix).


.. |wokeignore:rule=master| replace:: master
.. |wokeignore:rule=master-code| replace:: ``master``
