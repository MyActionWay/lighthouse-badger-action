<h1 align="center">Lighthouse-Badger | GitHub Action</h1>
<p align="center"><img src="https://repository-images.githubusercontent.com/359823564/31d7b800-af1f-11eb-8d4b-431075ac940c"/></p>
<p align="center"><a title="Check it out" target="_blank" href="https://github.com/myactionway/lighthouse-badger-action/blob/master/LICENSE.txt"><img src="https://img.shields.io/github/license/myactionway/lighthouse-badger-action?label=License" /></a>
<img src="https://img.shields.io/github/repo-size/myactionway/lighthouse-badger-action?label=RepoSize" /></p>
<hr>

The [Lighthouse-Badger](https://github.com/myactionway/lighthouse-badger-action "Get it") GitHub action makes it easy to manually/automatically generate, add and update Lighthouse badges and reports from one/multiple input URL-group(s) to one/multiple target repo(s)/branch(es).

If you've it [set up](#-setups "Go there"), you only need to add the result links to your use case once. Then the [Lighthouse-Badger](https://github.com/myactionway/lighthouse-badger-action "Get it") will automatically keep the badges up to date for you. So sit back and let the Badger do the job :wink:.

## | Credits

I, [Sitdisch](https://github.com/sitdisch "Visit me"), created the [Lighthouse-Badger](https://github.com/myactionway/lighthouse-badger-action "Get it") because I needed a GitHub action that would automatically update my Lighthouse badges on a regular basis and I haven't found a suitable solution.

The badge creation is based on the [Lighthouse-Badges](https://github.com/emazzotta/lighthouse-badges "Go there") repository  [License: [MIT](https://github.com/emazzotta/lighthouse-badges/blob/master/LICENSE.md "Go there"); Copyright (c) 2018 [Emanuele Mazzotta](https://github.com/emazzotta "Visit him")] and the pagespeed badge on the [Readme-Pagespeed-Insights](https://github.com/ankurparihar/readme-pagespeed-insights "Go there") repository  [License: [Apache-2.0](https://github.com/ankurparihar/readme-pagespeed-insights/blob/master/LICENSE "Go there"); Copyright (c) 2021 [Ankur Parihar](https://github.com/ankurparihar "Visit him")]. Check out both. They are magnificent and maybe better suited for your use case than the [Lighthouse-Badger](https://github.com/myactionway/lighthouse-badger-action "Get it").

Last but not least, everything is based on the extraordinary work of the contributors to the <a title="Visit the Lighthouse" target="_blank" href="https://github.com/GoogleChrome/lighthouse"><img src="https://raw.githubusercontent.com/GoogleChrome/lighthouse/master/assets/lighthouse-logo.svg" width="25"/> GoogleChrome/lighthouse </a> repository <b>"Chapeau!"</b>.

## | Previews

### Pagespeed Badge

<img src="https://raw.githubusercontent.com/sitdisch/lighthouse-badges/master/assets/img/scores/pagespeed.svg">

### Plastic Badges

<img src="https://raw.githubusercontent.com/sitdisch/lighthouse-badges/master/assets/img/scores/lighthouse_performance.svg"> <img src="https://raw.githubusercontent.com/sitdisch/lighthouse-badges/master/assets/img/scores/lighthouse_accessibility.svg"> <img src="https://raw.githubusercontent.com/sitdisch/lighthouse-badges/master/assets/img/scores/lighthouse_best-practices.svg"> <img src="https://raw.githubusercontent.com/sitdisch/lighthouse-badges/master/assets/img/scores/lighthouse_seo.svg"> <img src="https://raw.githubusercontent.com/sitdisch/lighthouse-badges/master/assets/img/scores/lighthouse_pwa.svg">

### Single Plastic Badge

<img src="https://raw.githubusercontent.com/sitdisch/lighthouse-badges/master/assets/img/scores/lighthouse.svg">

### Reports

The awesome [htmlpreview.github.com](https://github.com/htmlpreview/htmlpreview.github.com) repository makes it easy to show up your Lighthouse reports instantly rendered. Just put this `https://htmlpreview.github.io/?` before the URL where you placed your Lighthouse report e.&nbsp;g. `https://htmlpreview.github.io/?https://github.com/sitdisch/cloud/blob/master/lighthouse-results/dark-particle/desktop/mythemeway_github_io_dark_particle_.html`<br>

Examples: <a href="https://htmlpreview.github.io/?https://raw.githubusercontent.com/sitdisch/cloud/master/lighthouse-results/dark-particle/desktop/mythemeway_github_io_dark_particle_.html" title="Check it out" target="_blank">Main Page </a> | <a href="https://htmlpreview.github.io/?https://raw.githubusercontent.com/sitdisch/cloud/master/lighthouse-results/dark-particle/desktop/mythemeway_github_io_dark_particle_projects_2020_10_31_project_1_html.html" title="Check it out" target="_blank">Project Page</a>

<img src="https://raw.githubusercontent.com/sitdisch/cloud/master/images/lighthousebadger_report.png" />

## | Setups

First, choose one of these three workflow files:

### [lighthouse-badger-default.yml](https://github.com/MyActionWay/lighthouse-badger-workflows/blob/master/.github/workflows/lighthouse-badger-default.yml "Get it")
Generates, adds & updates manually/automatically Lighthouse badges & reports from <b>one/multiple input URL(s)</b> to a selected target repository & branch.

<details><summary><b>Set it up (click to toggle)</b></summary>

1. add the [lighthouse-badger-default.yml](https://github.com/MyActionWay/lighthouse-badger-workflows/blob/master/.github/workflows/lighthouse-badger-default.yml "Get it") workflow file to a repository
	* the path has to be `.github/workflows/lighthouse-badger-default.yml`
	* it doesn't have to be the repository where you want to add the Lighthouse results; e.&nbsp;g., you can simply [fork](https://github.com/myactionway/lighthouse-badger-workflows/fork "fork it") the `myactionway/lighthouse-badger-workflows` repository
		* CONSIDER: with a forked repository, you need to confirm that you want to use a workflow before you can actually use it (repo menu > actions tab > push the button)
2. create a new encrypted repository secret [[procedure]](https://docs.github.com/en/actions/reference/encrypted-secrets#creating-encrypted-secrets-for-a-repository "Learn how")
	* add the secret to the same repository where you added this workflow file
	* give the secret a name e.&nbsp;g. `LIGHTHOUSE_BADGER_TOKEN`
	* the value of the secret must be the value of the personal access token for the repository where you want to add the Lighthouse results.
		* [procedure for creating a personal access token](https://docs.github.com/en/github/authenticating-to-github/creating-a-personal-access-token "Learn how")
		* select only the minimum scopes and permissions required e.&nbsp;g. repo
3. adapt your [lighthouse-badger-default.yml](https://github.com/MyActionWay/lighthouse-badger-workflows/blob/master/.github/workflows/lighthouse-badger-default.yml "Get it") file
	* for manual triggers
		* all you have to do is enter your secret name e.&nbsp;g. `LIGHTHOUSE_BADGER_TOKEN`
			```yml
			env:
			#	Token for all triggers
				TOKEN: ${{ secrets.LIGHTHOUSE_BADGER_TOKEN }}
			```
			* CONSIDER: never enter the actual value of the personal access token
		* [procedure for manually running a workflow on GitHub](https://docs.github.com/en/actions/managing-workflow-runs/manually-running-a-workflow#running-a-workflow-on-github "Learn how")
			<img src="https://raw.githubusercontent.com/sitdisch/cloud/master/images/lighthousebadger_manual_inputs.png" />
			* CONSIDER: currently, you can't change the `TOKEN` in the UI
		* [procedure for manually running a workflow using the GitHub CLI](https://docs.github.com/en/actions/managing-workflow-runs/manually-running-a-workflow#running-a-workflow-using-github-cli)
		* [procedure for manually running a workflow using the REST API](https://docs.github.com/en/actions/managing-workflow-runs/manually-running-a-workflow#running-a-workflow-using-the-rest-api)
	* for all other triggers
		* adapt this section
			```yml
			##############################################################
			# DEFINE YOUR TOKEN, INPUTS AND TRIGGERS IN THE FOLLOWING
			##############################################################

			# TOKEN and INPUTS as environmental variables
			env:
			#	Token for all triggers
				TOKEN: # e.g. ${{ secrets.LIGHTHOUSE_BADGER_TOKEN }}
			# 
			#	Inputs for not manually triggered workflows
				URLS: # URL(s) to be checked e.g. 'https://github.com/sitdisch https://github.com/mythemeway'
				REPOSITORY: # target repository e.g. 'dummy/mytargetrepo'
				BRANCH: # target branch e.g. 'master'
				BADGES-ARGS: # badge-style '-b {flat,...}', preceding-label '-l "Lighthouse "', output-path '-o lighthouse_results/dummy', save-report '-r', single-badge '-s'
				RESULTS-TYPE: # 'mobile', 'desktop' or 'both'
				MOBILE-LIGHTHOUSE-PARAMS: # Lighthouse parameters mobile audit
				DESKTOP-LIGHTHOUSE-PARAMS: # Lighthouse parameters desktop audit
				USER-NAME: # user who should commit e.g. 'dummy'
				USER-EMAIL: # e.g. 'dummy@gmail.com'
				COMMIT-MESSAGE: # e.g. 'Lighthouse results added'

			# TRIGGERS
			on:
			#	page_build:
			#	schedule:
			#		- cron: '55 23 * * 0'
			```
		* CONSIDER:
			* token: never enter the actual value of the personal access token
			* inputs:
				* you only have to insert `URLS`; if any other input is blank, one of these default values will be used instead
					```yml
					DEFAULT-REPOSITORY: ${{ github.repository }} # repo with this file
					DEFAULT-BRANCH: 'master'
					DEFAULT-BADGES-ARGS: '-b pagespeed -o lighthouse_results -r'
					DEFAULT-RESULTS-TYPE: 'both'
					DEFAULT-MOBILE-LIGHTHOUSE-PARAMS: '--throttling.cpuSlowdownMultiplier=2'
					DEFAULT-DESKTOP-LIGHTHOUSE-PARAMS: '--preset=desktop --throttling.cpuSlowdownMultiplier=1'
					DEFAULT-USER-NAME: 'github-actions[bot]'
					DEFAULT-USER-EMAIL: '41898282+github-actions[bot]@users.noreply.github.com'
					DEFAULT-COMMIT-MESSAGE: 'Lighthouse-Badger[bot]: Results Added'
					```
				* badges-args: 
					* more information about the optional arguments can be found [here](https://github.com/sitdisch/lighthouse-badges#help "Go there")
					* in contrast to the Lighthouse-Badges repository
						* do not enter any URL(s) here
						* mobile or/and desktop is/are always added to your output-path
			* triggers:
				* page_build: Lighthouse results are generated every time after the GitHub page is built
				* schedule:
					* e.&nbsp;g. `cron: '55 23 * * 0'` executes the [Lighthouse-Badger](https://github.com/myactionway/lighthouse-badger-action "Get it") every Sunday at 23:55
					* you can check your inputs [here](https://crontab.guru/ "Go there")

That's it. Happy audits.

</details><p>

### [lighthouse-badger-n-groups.yml](https://github.com/MyActionWay/lighthouse-badger-workflows/blob/master/.github/workflows/lighthouse-badger-n-groups.yml "Get it")
Generates, adds & updates manually/automatically Lighthouse badges & reports for <b>different input URL-groups</b> to a selected target repository & branch.

<details><summary><b>Set it up (click to toggle)</b></summary>

1. add the [lighthouse-badger-n-groups.yml](https://github.com/MyActionWay/lighthouse-badger-workflows/blob/master/.github/workflows/lighthouse-badger-n-groups.yml "Get it") workflow file to a repository
	* the path has to be `.github/workflows/lighthouse-badger-n-groups.yml`
	* it doesn't have to be the repository where you want to add the Lighthouse results; e.&nbsp;g., you can simply [fork](https://github.com/myactionway/lighthouse-badger-workflows/fork "fork it") the `myactionway/lighthouse-badger-workflows` repository
		* CONSIDER: with a forked repository, you need to confirm that you want to use a workflow before you can actually use it (repo menu > actions tab > push the button)
2. create a new encrypted repository secret [[procedure]](https://docs.github.com/en/actions/reference/encrypted-secrets#creating-encrypted-secrets-for-a-repository "Learn how")
	* add the secret to the same repository where you added this workflow file
	* give the secret a name e.&nbsp;g. `LIGHTHOUSE_BADGER_TOKEN`
	* the value of the secret must be the value of the personal access token for the repository where you want to add the Lighthouse results.
		* [procedure for creating a personal access token](https://docs.github.com/en/github/authenticating-to-github/creating-a-personal-access-token "Learn how")
		* select only the minimum scopes and permissions required e.&nbsp;g. repo
3. adapt your [lighthouse-badger-n-groups.yml](https://github.com/MyActionWay/lighthouse-badger-workflows/blob/master/.github/workflows/lighthouse-badger-n-groups.yml "Get it") file
	* define your defaults
		```yml
		########################################################################
		# DEFINE YOUR DEFAULTS (TOKEN, INPUTS & TRIGGERS) IN THE FOLLOWING
		########################################################################

		# TOKEN and INPUTS as environmental variables (env)
		env:
			TOKEN: # e.g. ${{ secrets.LIGHTHOUSE_BADGER_TOKEN }}
			REPOSITORY: # target repository e.g. 'dummy/mytargetrepo'
			BRANCH: # target branch e.g. 'master'
			USER-NAME: # user who should commit e.g. 'dummy'
			USER-EMAIL: # e.g. 'dummy@gmail.com'
			COMMIT-MESSAGE: # e.g. 'Lighthouse results added'
			RESULTS-TYPE: # 'mobile', 'desktop' or 'both'
			MOBILE-LIGHTHOUSE-PARAMS: # Lighthouse parameters mobile audit
			DESKTOP-LIGHTHOUSE-PARAMS: # Lighthouse parameters desktop audit

		# TRIGGERS
		on:
		#	page_build:
		#	schedule:
		#		- cron: '55 23 * * 0' # e.g. every Sunday at 23:55
		#	workflow_dispatch:
		```
		* CONSIDER:
			* token: never enter the actual value of the personal access token
			* inputs:
				* all inputs have predefined values; you can, but you don't have to overwrite them
					```yml
					# Predefined values
					REPOSITORY: ${{ github.repository }} # repo with this file
					BRANCH: 'master'
					USER-NAME: 'github-actions[bot]'
					USER-EMAIL: '41898282+github-actions[bot]@users.noreply.github.com'
					COMMIT-MESSAGE: 'Lighthouse-Badger[bot]: Results Added'
					RESULTS-TYPE: 'both'
					MOBILE-LIGHTHOUSE-PARAMS: '--throttling.cpuSlowdownMultiplier=2'
					DESKTOP-LIGHTHOUSE-PARAMS: '--preset=desktop --throttling.cpuSlowdownMultiplier=1'
					```
			* triggers:
				* page_build: Lighthouse results are generated every time after the GitHub page is built
				* schedule:
					* e.&nbsp;g. `cron: '55 23 * * 0'` executes the [Lighthouse-Badger](https://github.com/myactionway/lighthouse-badger-action "Get it") every Sunday at 23:55
					* you can check your inputs [here](https://crontab.guru/ "Go there")
				* workflow_dispatch:
					* no predefined inputs; the environmental variables defined in this workflow file are used instead when this trigger is triggered
					* [procedure for manually running a workflow on GitHub](https://docs.github.com/en/actions/managing-workflow-runs/manually-running-a-workflow#running-a-workflow-on-github "Learn how")
					* [procedure for manually running a workflow using the GitHub CLI](https://docs.github.com/en/actions/managing-workflow-runs/manually-running-a-workflow#running-a-workflow-using-github-cli)
					* [procedure for manually running a workflow using the REST API](https://docs.github.com/en/actions/managing-workflow-runs/manually-running-a-workflow#running-a-workflow-using-the-rest-api)<p>
	* define your settings for the different input URL-Groups
		```yml
		#
		# FIRST URL-GROUP | DEFINE YOUR ENV IN THE FOLLOWING
		#
		{
		 URLS='https://github.com/sitdisch https://github.com/mythemeway';
		 BADGES_ARGS='-b pagespeed -o lighthouse_results/first_group -r';
		 RESULTS_TYPE='${{ env.RESULTS-TYPE }}';
		 MOBILE_LIGHTHOUSE_PARAMS='${{ env.MOBILE-LIGHTHOUSE-PARAMS }}';
		 DESKTOP_LIGHTHOUSE_PARAMS='${{ env.DESKTOP-LIGHTHOUSE-PARAMS }}';
		 # THAT'S IT; JUMP TO THE NEXT URL-GROUP
		 lighthouse_badger_action
		} &
		#
		# SECOND URL-GROUP | DEFINE YOUR ENV IN THE FOLLOWING
		#
		{
		 URLS='https://mythemeway.github.io/Dark-Particle/ https://mythemeway.github.io/Dark-Particle/projects/2020/10/31/project-1.html';
		 BADGES_ARGS='-b flat -o lighthouse_results/second_group -r';
		 RESULTS_TYPE='${{ env.RESULTS-TYPE }}';
		 MOBILE_LIGHTHOUSE_PARAMS='${{ env.MOBILE-LIGHTHOUSE-PARAMS }}';
		 DESKTOP_LIGHTHOUSE_PARAMS='${{ env.DESKTOP-LIGHTHOUSE-PARAMS }}';
		 # THAT'S IT; JUMP TO THE NEXT URL-GROUP
		 lighthouse_badger_action
		} &
		#
		# THIRD ULR-GROUP | ...
		#
		```
		* CONSIDER: 
			* you just have to change `URLS` and `BADGES_ARGS` for each group
				* `BADGES_ARGS`: 
					* set different output-paths for different groups
					* more information about the optional arguments can be found [here](https://github.com/sitdisch/lighthouse-badges#help "Go there")
					* in contrast to the Lighthouse-Badges repository
						* do not enter any URL(s) here
						* mobile or/and desktop is/are always added to your output-path
			* if you do not change any of the other inputs, your predefined defaults will be used instead
			* you can't change TOKEN, REPOSITORY, BRANCH, USER-NAME, USER-EMAIL and COMMIT-MESSAGE for the different URL-groups; this is possible with the [lighthouse-badger-n-targets.yml](#lighthouse-badger-n-targetsyml "Go there") workflow file

That's it. Happy audits.

</details><p>

### [lighthouse-badger-n-targets.yml](https://github.com/MyActionWay/lighthouse-badger-workflows/blob/master/.github/workflows/lighthouse-badger-n-targets.yml "Get it")
Generates, adds & updates manually/automatically Lighthouse badges & reports for <b>different input URL-groups to different target repositories & branches</b>

<details><summary><b>Set it up (click to toggle)</b></summary>

1. add the [lighthouse-badger-n-targets.yml](https://github.com/MyActionWay/lighthouse-badger-workflows/blob/master/.github/workflows/lighthouse-badger-n-targets.yml "Get it") workflow file to a repository
	* the path has to be `.github/workflows/lighthouse-badger-n-targets.yml`
	* it doesn't have to be a repository where you want to add Lighthouse results; e.&nbsp;g., you can simply [fork](https://github.com/myactionway/lighthouse-badger-workflows/fork "fork it") the `myactionway/lighthouse-badger-workflows` repository
		* CONSIDER: with a forked repository, you need to confirm that you want to use a workflow before you can actually use it (repo menu > actions tab > push the button)
2. create new encrypted repository secrets [[procedure]](https://docs.github.com/en/actions/reference/encrypted-secrets#creating-encrypted-secrets-for-a-repository "Learn how")
	* add the secrets to the same repository where you added this workflow file
	* give the secrets names e.&nbsp;g. `LIGHTHOUSE_BADGER_TOKEN1` and `LIGHTHOUSE_BADGER_TOKEN2`
	* the values of the secrets must be the values of the personal access tokens for the repositories where you want to add the Lighthouse results.
		* [procedure for creating a personal access token](https://docs.github.com/en/github/authenticating-to-github/creating-a-personal-access-token "Learn how")
		* select only the minimum scopes and permissions required e.&nbsp;g. repo
3. adapt your [lighthouse-badger-n-targets.yml](https://github.com/MyActionWay/lighthouse-badger-workflows/blob/master/.github/workflows/lighthouse-badger-n-targets.yml "Get it") file
	* define your defaults
		```yml
		########################################################################
		# DEFINE YOUR DEFAULTS (TOKEN, INPUTS & TRIGGERS) IN THE FOLLOWING
		########################################################################

		# TOKEN and INPUTS as environmental variables (env)
		env:
			TOKEN: # e.g. ${{ secrets.LIGHTHOUSE_BADGER_TOKEN1 }}
			REPOSITORY: # target repository e.g. 'dummy/mytargetrepo'
			BRANCH: # target branch e.g. 'master'
			USER-NAME: # user who should commit e.g. 'dummy'
			USER-EMAIL: # e.g. 'dummy@gmail.com'
			COMMIT-MESSAGE: # e.g. 'Lighthouse results added'
			RESULTS-TYPE: # 'mobile', 'desktop' or 'both'
			MOBILE-LIGHTHOUSE-PARAMS: # Lighthouse parameters mobile audit
			DESKTOP-LIGHTHOUSE-PARAMS: # Lighthouse parameters desktop audit

		# TRIGGERS
		on:
		#	page_build:
		#	schedule:
		#		- cron: '55 23 * * 0' # e.g. every Sunday at 23:55
		#	workflow_dispatch:
		```
		* CONSIDER:
			* token: never enter the actual value of the personal access token
			* inputs:
				* all inputs have predefined values; you can, but you don't have to overwrite them
					```yml
					# Predefined values
					REPOSITORY: ${{ github.repository }} # repo with this file
					BRANCH: 'master'
					USER-NAME: 'github-actions[bot]'
					USER-EMAIL: '41898282+github-actions[bot]@users.noreply.github.com'
					COMMIT-MESSAGE: 'Lighthouse-Badger[bot]: Results Added'
					RESULTS-TYPE: 'both'
					MOBILE-LIGHTHOUSE-PARAMS: '--throttling.cpuSlowdownMultiplier=2'
					DESKTOP-LIGHTHOUSE-PARAMS: '--preset=desktop --throttling.cpuSlowdownMultiplier=1'
					```
			* triggers:
				* page_build: Lighthouse results are generated every time after the GitHub page is built
				* schedule:
					* e.&nbsp;g. `cron: '55 23 * * 0'` executes the [Lighthouse-Badger](https://github.com/myactionway/lighthouse-badger-action "Get it") every Sunday at 23:55
					* you can check your inputs [here](https://crontab.guru/ "Go there")
				* workflow_dispatch:
					* no predefined inputs; the environmental variables defined in this workflow file are used instead when this trigger is triggered
					* [procedure for manually running a workflow on GitHub](https://docs.github.com/en/actions/managing-workflow-runs/manually-running-a-workflow#running-a-workflow-on-github "Learn how")
					* [procedure for manually running a workflow using the GitHub CLI](https://docs.github.com/en/actions/managing-workflow-runs/manually-running-a-workflow#running-a-workflow-using-github-cli)
					* [procedure for manually running a workflow using the REST API](https://docs.github.com/en/actions/managing-workflow-runs/manually-running-a-workflow#running-a-workflow-using-the-rest-api)<p>
	* define your settings for the first target
		```yml
		###################################################################
		# FIRST TARGET | DEFINE YOUR ENV IN THE FOLLOWING
		###################################################################
		lighthouse-badger-1-target:
			runs-on: ubuntu-20.04
			env:
		#		TOKEN:
				REPOSITORY: 'dummy/first_repo'
		#		BRANCH:
		#		RESULTS-TYPE:
		#		MOBILE-LIGHTHOUSE-PARAMS:
		#		DESKTOP-LIGHTHOUSE-PARAMS:
		#		USER-NAME:
		#		USER-EMAIL:
				COMMIT-MESSAGE: 'Lighthouse-Badger[bot]: Results Added | First Target'
		```
		* CONSIDER: your defaults will be used unless you redefine the env<p>
	* define your settings for the different input URL-Groups of the first target
		```yml
		#
		# FIRST URL-GROUP | FIRST TARGET | DEFINE YOUR ENV BELOW
		#
		{
		 URLS='https://github.com/sitdisch https://github.com/mythemeway';
		 BADGES_ARGS='-b pagespeed -o lighthouse_results/first_group -r';
		 RESULTS_TYPE='${{ env.RESULTS-TYPE }}';
		 MOBILE_LIGHTHOUSE_PARAMS='${{ env.MOBILE-LIGHTHOUSE-PARAMS }}';
		 DESKTOP_LIGHTHOUSE_PARAMS='${{ env.DESKTOP-LIGHTHOUSE-PARAMS }}';
		 # THAT'S IT; JUMP TO THE NEXT URL-GROUP
		 lighthouse_badger_action
		} &
		#
		# SECOND URL-GROUP | FIRST TARGET | DEFINE YOUR ENV BELOW
		#
		{
		 URLS='https://mythemeway.github.io/Dark-Particle/ https://mythemeway.github.io/Dark-Particle/projects/2020/10/31/project-1.html';
		 BADGES_ARGS='-b flat -o lighthouse_results/second_group -r';
		 RESULTS_TYPE='${{ env.RESULTS-TYPE }}';
		 MOBILE_LIGHTHOUSE_PARAMS='${{ env.MOBILE-LIGHTHOUSE-PARAMS }}';
		 DESKTOP_LIGHTHOUSE_PARAMS='${{ env.DESKTOP-LIGHTHOUSE-PARAMS }}';
		 # THAT'S IT; JUMP TO THE NEXT URL-GROUP
		 lighthouse_badger_action
		} &
		#
		# THIRD ULR-GROUP | ...
		#
		```
		* CONSIDER: 
			* you just have to change `URLS` and `BADGES_ARGS` for each group
				* `BADGES_ARGS`: 
					* set different output-paths for different groups
					* more information about the optional arguments can be found [here](https://github.com/sitdisch/lighthouse-badges#help "Go there")
					* in contrast to the Lighthouse-Badges repository
						* do not enter any URL(s) here
						* mobile or/and desktop is/are always added to your output-path
			* if you do not change any of the other inputs, your predefined defaults will be used instead
			* you can't change TOKEN, REPOSITORY, BRANCH, USER-NAME, USER-EMAIL and COMMIT-MESSAGE for the different URL-groups;
	* define your settings for the second target
		```yml
		###################################################################
		# SECOND TARGET | DEFINE YOUR ENV IN THE FOLLOWING
		###################################################################
		lighthouse-badger-2-target:
			runs-on: ubuntu-20.04
			env:
				TOKEN: ${{ secrets.LIGHTHOUSE_BADGER_TOKEN2 }}
				REPOSITORY: 'dummy/second_repo'
		#		BRANCH:
		#		RESULTS-TYPE:
		#		MOBILE-LIGHTHOUSE-PARAMS:
		#		DESKTOP-LIGHTHOUSE-PARAMS:
		#		USER-NAME:
		#		USER-EMAIL:
				COMMIT-MESSAGE: 'Lighthouse-Badger[bot]: Results Added | Second Target'
	* define your settings for the different input URL-Groups of the second target
		```yml
		#
		# FIRST URL-GROUP | SECOND TARGET | DEFINE YOUR ENV BELOW
		#
		{
		 URLS='https://github.com/myactionway';
		 BADGES_ARGS='-b pagespeed -o lighthouse_results/first_group -r';
		 RESULTS_TYPE='${{ env.RESULTS-TYPE }}';
		 MOBILE_LIGHTHOUSE_PARAMS='${{ env.MOBILE-LIGHTHOUSE-PARAMS }}';
		 DESKTOP_LIGHTHOUSE_PARAMS='${{ env.DESKTOP-LIGHTHOUSE-PARAMS }}';
		 # THAT'S IT; JUMP TO THE NEXT URL-GROUP
		 lighthouse_badger_action
		} &
		#
		# SECOND URL-GROUP | ...
		#
		```
	* feel free to add more targets like above

That's it. Happy audits.

</details><p>

## | Known issues & possible solutions
* No scores are displayed in the pagespeed.svg file.
	* They are there, if not, NA is inserted. Try opening the SVG with a browser and the scores will pop up, I promise.
* The repository size is growing continuously due to the automatic updating of the badges.
	* The [Branch-Pruner](https://github.com/myactionway/branch-pruner-action "Get it") can help. E.&nbsp;g. put your Lighthouse results on a separate branch and automatically prune that branch with the Pruner, as you like. 
* The workflow logs do not provide enough detail to diagnose why a workflow, job, or step is not working as expected.
	* enable [addition debug logging](https://docs.github.com/en/actions/managing-workflow-runs/enabling-debug-logging)

## | Application example
<a href="https://github.com/mythemeway/Dark-Particle" title="Check it out" target="_blank"><img src="https://raw.githubusercontent.com/sitdisch/cloud/master/gifs/lighthouse_badger_example.gif" /></a>
