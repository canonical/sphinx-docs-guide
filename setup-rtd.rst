How to set up your documentation on RTD.com
==============================================


Create the project on Read the Docs
----------------------------------------

On `the readthedocs.com Dashboard <https://readthedocs.com/dashboard/>`_, create a new project.

* for a public Git repository, use the **Import** button
* for a private Git repository, or if you can't easily find the repository, use
  https://readthedocs.com/dashboard/import/manual/

..  admonition:: When importing your project, make sure that you check the *Default branch*
	field.

	If your repository does not have a master branch, and you don't specify the
	correct default branch, it will default to ``master`` and will not be able to check
	out the repository and find the correct one.

	If this does happen, the solution is to add a ``master`` branch to the project until
	you're able to build it once, then specify the correct branch.
