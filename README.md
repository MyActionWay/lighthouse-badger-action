<h1 align="center">Lighthouse-Badger | GitHub Action</h1>
<p align="center"><img src="https://repository-images.githubusercontent.com/359823564/31d7b800-af1f-11eb-8d4b-431075ac940c"/></p>
<p align="center">
<img src="https://img.shields.io/github/repo-size/myactionway/lighthouse-badger-action?label=RepoSize" />
<a title="Check it out" target="_blank" href="https://github.com/myactionway/lighthouse-badger-action/blob/master/LICENSE.txt"><img src="https://img.shields.io/github/license/myactionway/lighthouse-badger-action?label=License" /></a>
<a title="Check it out" target="_blank" href="https://github.com/MyActionWay/lighthouse-badger-action/releases"><img src="https://img.shields.io/github/v/release/myactionway/lighthouse-badger-action?label=LastRelease" /></a>
</p>
<small><p align="center">[ <a title="Check it out" target="_blank" href="https://github.com/myactionway/lighthouse-badger-workflows">Workflow Readme</a> == <a title="Check it out" target="_blank" href="https://github.com/myactionway/lighthouse-badger-action">Action Readme</a> ]</p></small>
<hr>

The [Lighthouse-Badger](https://github.com/myactionway/lighthouse-badger-action "Get it") GitHub action makes it easy to manually/automatically generate, add and update Lighthouse badges and reports from one/multiple input URL-group(s) to one/multiple target repo(s)/branch(es) in parallel.

Once you have it [set up](#-setups "Go there"), you only need to add the links to your results once in your use case (e.&nbsp;g. Github readme, website,...). The [Lighthouse-Badger](https://github.com/myactionway/lighthouse-badger-action "Get it") will then automatically keep the badges up to date for you. So sit back and let the Badger do the job :wink:.

## | Credits

I, [Sitdisch](https://github.com/sitdisch "Visit me"), created the [Lighthouse-Badger](https://github.com/myactionway/lighthouse-badger-action "Get it") because I needed a GitHub action that would automatically update my Lighthouse badges and reports on a regular basis and I haven't found a suitable solution.

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

The awesome [htmlpreview.github.com](https://github.com/htmlpreview/htmlpreview.github.com) repository makes it easy to show up your Lighthouse reports instantly rendered. Just put this `https://htmlpreview.github.io/?` before the URL where you placed your Lighthouse report e.&nbsp;g. `https://htmlpreview.github.io/?https://github.com/sitdisch/cloud/blob/master/lighthouse_results/dark_particle/desktop/mythemeway_github_io_dark_particle_.html`<br>

Examples: <a href="https://htmlpreview.github.io/?https://raw.githubusercontent.com/sitdisch/cloud/master/lighthouse_results/dark_particle/desktop/mythemeway_github_io_dark_particle_.html" title="Check it out" target="_blank">Main Page </a> | <a href="https://htmlpreview.github.io/?https://raw.githubusercontent.com/sitdisch/cloud/master/lighthouse_results/dark_particle/desktop/mythemeway_github_io_dark_particle_projects_2020_10_31_project_1_html.html" title="Check it out" target="_blank">Project Page</a>

<a href="https://htmlpreview.github.io/?https://raw.githubusercontent.com/sitdisch/cloud/master/lighthouse_results/dark_particle/desktop/mythemeway_github_io_dark_particle_.html" title="Check it out" target="_blank"><img src="https://raw.githubusercontent.com/sitdisch/cloud/master/images/lighthousebadger_report.png" /></a>

## | Setups

First, choose a workflow file:

### [lighthouse-badger-easy.yml](https://github.com/MyActionWay/lighthouse-badger-workflows/blob/master/.github/workflows/lighthouse-badger-easy.yml "Get it")
Generates, adds & updates manually/automatically Lighthouse badges & reports from one/multiple input <b>URL(s) to the current repository & master branch with minimal settings</b>.

<details><summary><b>Set it up (click to toggle)</b></summary>

1. add the [lighthouse-badger-easy.yml](https://github.com/MyActionWay/lighthouse-badger-workflows/blob/master/.github/workflows/lighthouse-badger-easy.yml "Get it") workflow file to a repository
	* it has to be the target repository where you want to add the Lighthouse results (this is not the case with the other workflow files)
	* the path has to be `.github/workflows/lighthouse-badger-easy.yml`
2. create a new encrypted repository secret [[procedure](https://docs.github.com/en/actions/reference/encrypted-secrets#creating-encrypted-secrets-for-a-repository "Learn how")]
	* give the secret a name e.&nbsp;g. `LIGHTHOUSE_BADGER_TOKEN`
	* the value of the secret must be the value of the personal access token for the repository where you want to add the Lighthouse results.
		* [procedure for creating a personal access token](https://docs.github.com/en/github/authenticating-to-github/creating-a-personal-access-token "Learn how")
		* select only the minimum scopes and permissions required e.&nbsp;g. repo
	* add the secret to the same repository where you added this workflow file
3. adapt your [lighthouse-badger-easy.yml](https://github.com/MyActionWay/lighthouse-badger-workflows/blob/master/.github/workflows/lighthouse-badger-easy.yml "Get it") file
	* for manual triggers
		* you don't have to adjust anything in the workflow file; just use it
			* [procedure for manually running a workflow on GitHub](https://docs.github.com/en/actions/managing-workflow-runs/manually-running-a-workflow#running-a-workflow-on-github "Learn how")
				<img src="https://raw.githubusercontent.com/sitdisch/cloud/master/images/lighthousebadger_minimal_manual_inputs.png" />
			* [procedure for manually running a workflow using the GitHub CLI](https://docs.github.com/en/actions/managing-workflow-runs/manually-running-a-workflow#running-a-workflow-using-github-cli)
			* [procedure for manually running a workflow using the REST API](https://docs.github.com/en/actions/managing-workflow-runs/manually-running-a-workflow#running-a-workflow-using-the-rest-api)
	* for all other triggers
		* adapt this section
			```yml
			##############################################################
			# DEFINE YOUR INPUTS AND TRIGGERS IN THE FOLLOWING
			##############################################################

			# INPUTS as environmental variables (env)
			env:
				URLS: # URL(s) to be checked e.g. 'https://github.com/sitdisch https://github.com/mythemeway'
				TOKEN_NAME: # target token name e.g. 'LIGHTHOUSE_BADGER_TOKEN'

			# TRIGGERS
			on:
			#	page_build:
			#	schedule:
			#		- cron: '55 23 * * 0'
			```
		* CONSIDER:
			* INPUTS:
				* you only have to define `URLS` and `TOKEN_NAME`;
				* `TOKEN_NAME`: never enter the actual value of the personal access token
			* TRIGGERS:
				* `page_build`: Lighthouse results are generated every time after the GitHub page is built
				* `schedule`:
					* e.&nbsp;g. `cron: '55 23 * * 0'` executes the [Lighthouse-Badger](https://github.com/myactionway/lighthouse-badger-action "Get it") every Sunday at 23:55
					* you can check your inputs [here](https://crontab.guru/ "Go there")
			* hidden defaults (changeable with the other workflow files):
				* target repository & branch: Repository with this workflow file and master branch
				* outputs:
					* badges: pagespeed.svg
					* reports: yes
					* output-paths: 
						* lighthouse_results/mobile
						* lighthouse_results/desktop
				* audit types:
					* mobile:
						* parameters: '--throttling.cpuSlowdownMultiplier=2' 		
					* desktop:
						* parameters: '--throttling.cpuSlowdownMultiplier=1'
				* other settings:
					* user who commit: github-actions[bot]
					* user e-mail address: 41898282+github-actions[bot]@users.noreply.github.com
					* commit message: Lighthouse-Badger[bot]: Results Added

That's it. Happy audits.

</details><p>

### [lighthouse-badger-default.yml](https://github.com/MyActionWay/lighthouse-badger-workflows/blob/master/.github/workflows/lighthouse-badger-default.yml "Get it")
Generates, adds & updates manually/automatically Lighthouse badges & reports from one/multiple input <b>URL(s) to a selected target repository & branch</b>.

<details><summary><b>Set it up (click to toggle)</b></summary>

1. add the [lighthouse-badger-default.yml](https://github.com/MyActionWay/lighthouse-badger-workflows/blob/master/.github/workflows/lighthouse-badger-default.yml "Get it") workflow file to a repository
	* it doesn't have to be the repository where you want to add the Lighthouse results; e.&nbsp;g., you can simply [fork](https://github.com/myactionway/lighthouse-badger-workflows/fork "fork it") the `myactionway/lighthouse-badger-workflows` repository
		* CONSIDER: with a forked repository, you need to confirm that you want to use a workflow before you can actually use it (repo menu > actions tab > push the button)
	* the path has to be `.github/workflows/lighthouse-badger-default.yml`
2. create a new encrypted repository secret [[procedure](https://docs.github.com/en/actions/reference/encrypted-secrets#creating-encrypted-secrets-for-a-repository "Learn how")]
	* give the secret a name e.&nbsp;g. `LIGHTHOUSE_BADGER_TOKEN`
	* the value of the secret must be the value of the personal access token for the target repository where you want to add the Lighthouse results.
		* [procedure for creating a personal access token](https://docs.github.com/en/github/authenticating-to-github/creating-a-personal-access-token "Learn how")
		* select only the minimum scopes and permissions required e.&nbsp;g. repo
	* add the secret to the same repository where you added this workflow file
3. adapt your [lighthouse-badger-default.yml](https://github.com/MyActionWay/lighthouse-badger-workflows/blob/master/.github/workflows/lighthouse-badger-default.yml "Get it") file
	* for manual triggers
		* you don't have to adjust anything in the workflow file; just use it
			* [procedure for manually running a workflow on GitHub](https://docs.github.com/en/actions/managing-workflow-runs/manually-running-a-workflow#running-a-workflow-on-github "Learn how")
				<img src="https://raw.githubusercontent.com/sitdisch/cloud/master/images/lighthousebadger_manual_inputs.png" />
			* [procedure for manually running a workflow using the GitHub CLI](https://docs.github.com/en/actions/managing-workflow-runs/manually-running-a-workflow#running-a-workflow-using-github-cli)
			* [procedure for manually running a workflow using the REST API](https://docs.github.com/en/actions/managing-workflow-runs/manually-running-a-workflow#running-a-workflow-using-the-rest-api)
	* for all other triggers
		* adapt this section
			```yml
			##############################################################
			# DEFINE YOUR INPUTS AND TRIGGERS IN THE FOLLOWING
			##############################################################

			# INPUTS as environmental variables (env)
			env:
				URLS: # URL(s) to be checked e.g. 'https://github.com/sitdisch https://github.com/mythemeway'
				TOKEN_NAME: # target token name e.g. 'LIGHTHOUSE_BADGER_TOKEN'
				REPO_BRANCH: # target repository & branch e.g. 'dummy/mytargetrepo master'
				BADGES_ARGS: # badge-style '-b {flat,...}', preceding-label '-l "Lighthouse "', output-path '-o lighthouse_results/dummy', save-report '-r', single-badge '-s'
				AUDIT_TYPE: # 'mobile', 'desktop', 'both' or 'both_p' 
				MOBILE_LIGHTHOUSE_PARAMS: # Lighthouse parameters mobile audit
				DESKTOP_LIGHTHOUSE_PARAMS: # Lighthouse parameters desktop audit
				USER_NAME: # user who should commit e.g. 'dummy'
				USER_EMAIL: # e.g. 'dummy@gmail.com'
				COMMIT_MESSAGE: # e.g. 'Lighthouse results added'

			# TRIGGERS
			on:
			#	page_build:
			#	schedule:
			#		- cron: '55 23 * * 0'
			```
		* CONSIDER:
			* INPUTS:
				* you only have to define `URLS` and `TOKEN_NAME`; if any other input is blank, one of these default values will be used instead
					```yml
					DEFAULT_REPO_BRANCH: '${{ github.repository }} master' # repo with this file and master branch
					DEFAULT_BADGES_ARGS: '-b pagespeed -o lighthouse_results -r'
					DEFAULT_AUDIT_TYPE: 'both'
					DEFAULT_MOBILE_LIGHTHOUSE_PARAMS: '--throttling.cpuSlowdownMultiplier=2'
					DEFAULT_DESKTOP_LIGHTHOUSE_PARAMS: '--preset=desktop --throttling.cpuSlowdownMultiplier=1'
					DEFAULT_USER_NAME: 'github-actions[bot]'
					DEFAULT_USER_EMAIL: '41898282+github-actions[bot]@users.noreply.github.com'
					DEFAULT_COMMIT_MESSAGE: 'Lighthouse-Badger[bot]: Results Added'
					```
				* `TOKEN_NAME`: never enter the actual value of the personal access token
				* `BADGES_ARGS`: 
					* more information about the optional arguments can be found [here](https://github.com/sitdisch/lighthouse-badges#help "Go there")
					* in contrast to the Lighthouse-Badges repository
						* do not enter any URL(s) here
						* mobile or/and desktop is/are always added to your output-path
				* `MOBILE/DESKTOP_LIGHTHOUSE_PARAMS`:
					* more information about the optional arguments can be found [here](https://github.com/GoogleChrome/lighthouse#cli-options)
				* `AUDIT_TYPE`:
					* `'both_p'`: desktop and mobile audits are carried out in parallel
						* <b>it's not recommended</b> as it can skew the performance results [<a title="Check it out" target="_blank" href="https://github.com/GoogleChrome/lighthouse/issues/7104#issuecomment-458368476">source</a>] and it can also be slower than `'both'`
			* TRIGGERS:
				* `page_build`: Lighthouse results are generated every time after the GitHub page is built
				* `schedule`:
					* e.&nbsp;g. `cron: '55 23 * * 0'` executes the [Lighthouse-Badger](https://github.com/myactionway/lighthouse-badger-action "Get it") every Sunday at 23:55
					* you can check your inputs [here](https://crontab.guru/ "Go there")

That's it. Happy audits.

</details><p>

### [lighthouse-badger-advanced.yml](https://github.com/MyActionWay/lighthouse-badger-workflows/blob/master/.github/workflows/lighthouse-badger-advanced.yml "Get it")
Generates, adds & updates manually/automatically Lighthouse badges & reports from one/multiple input <b>URL-group(s) to one/multiple target repo(s)/branch(es) in parallel</b>.

<details><summary><b>Set it up (click to toggle)</b></summary>

1. add the [lighthouse-badger-advanced.yml](https://github.com/MyActionWay/lighthouse-badger-workflows/blob/master/.github/workflows/lighthouse-badger-advanced.yml "Get it") workflow file to a repository
	* it doesn't have to be a repository where you want to add Lighthouse results; e.&nbsp;g., you can simply [fork](https://github.com/myactionway/lighthouse-badger-workflows/fork "fork it") the `myactionway/lighthouse-badger-workflows` repository
		* CONSIDER: with a forked repository, you need to confirm that you want to use a workflow before you can actually use it (repo menu > actions tab > push the button)
	* the path has to be `.github/workflows/lighthouse-badger-advanced.yml`
2. create new encrypted repository secrets [[procedure](https://docs.github.com/en/actions/reference/encrypted-secrets#creating-encrypted-secrets-for-a-repository "Learn how")]
	* give the secrets names e.&nbsp;g. `LIGHTHOUSE_BADGER_TOKEN_1` and `LIGHTHOUSE_BADGER_TOKEN_2`
	* the values of the secrets must be the values of the personal access tokens for the target repositories where you want to add the Lighthouse results.
		* [procedure for creating a personal access token](https://docs.github.com/en/github/authenticating-to-github/creating-a-personal-access-token "Learn how")
		* select only the minimum scopes and permissions required e.&nbsp;g. repo
	* add the secrets to the same repository where you added this workflow file
3. adapt your [lighthouse-badger-advanced.yml](https://github.com/MyActionWay/lighthouse-badger-workflows/blob/master/.github/workflows/lighthouse-badger-advanced.yml "Get it") file
	* define your defaults
		```yml
		##############################################################
		# DEFINE YOUR DEFAULTS (INPUTS & TRIGGERS) IN THE FOLLOWING
		##############################################################

		# INPUTS as environmental variables (env)
		env:
			TOKEN_NAME: # target token name e.g. 'LIGHTHOUSE_BADGER_TOKEN_1'
			REPO_BRANCH: # target repository & branch e.g. 'dummy/mytargetrepo_1 master'
			AUDIT_TYPE: # 'mobile', 'desktop', 'both' or 'both_p' 
			MOBILE_LIGHTHOUSE_PARAMS: # Lighthouse parameters mobile audit
			DESKTOP_LIGHTHOUSE_PARAMS: # Lighthouse parameters desktop audit
			USER_NAME: # user who should commit e.g. 'dummy'
			USER_EMAIL: # e.g. 'dummy@gmail.com'
			COMMIT_MESSAGE: # e.g. 'Lighthouse results added'

		# TRIGGERS
		on:
		#	page_build:
		#	schedule:
		#		- cron: '55 23 * * 0'
			workflow_dispatch:
		```
		* CONSIDER:
			* INPUTS:
				* `TOKEN_NAME`: never enter the actual value of the personal access token
				* all inputs except `TOKEN_NAME` have predefined values; you can, but you don't have to overwrite them
					```yml
					# Predefined values
					REPO_BRANCH: '${{ github.repository }} master' # repo with this file and master branch
					AUDIT_TYPE: 'both'
					MOBILE_LIGHTHOUSE_PARAMS: '--throttling.cpuSlowdownMultiplier=2'
					DESKTOP_LIGHTHOUSE_PARAMS: '--preset=desktop --throttling.cpuSlowdownMultiplier=1'
					USER_NAME: 'github-actions[bot]'
					USER_EMAIL: '41898282+github-actions[bot]@users.noreply.github.com'
					COMMIT_MESSAGE: 'Lighthouse-Badger[bot]: Results Added'
					```
				* `MOBILE/DESKTOP_LIGHTHOUSE_PARAMS`:
					* more information about the optional arguments can be found [here](https://github.com/GoogleChrome/lighthouse#cli-options)
				* `AUDIT_TYPE`:
					* `'both_p'`: desktop and mobile audits are carried out in parallel
						* <b>it's not recommended</b> as it can skew the performance results [<a title="Check it out" target="_blank" href="https://github.com/GoogleChrome/lighthouse/issues/7104#issuecomment-458368476">source</a>] and it can also be slower than `'both'`
			* TRIGGERS:
				* `page_build`: Lighthouse results are generated every time after the GitHub page is built
				* `schedule`:
					* e.&nbsp;g. `cron: '55 23 * * 0'` executes the [Lighthouse-Badger](https://github.com/myactionway/lighthouse-badger-action "Get it") every Sunday at 23:55
					* you can check your inputs [here](https://crontab.guru/ "Go there")
				* `workflow_dispatch`:
					* no predefined inputs; the `env` defined in this workflow file are used instead when this trigger is triggered
					* [procedure for manually running a workflow on GitHub](https://docs.github.com/en/actions/managing-workflow-runs/manually-running-a-workflow#running-a-workflow-on-github "Learn how")
					* [procedure for manually running a workflow using the GitHub CLI](https://docs.github.com/en/actions/managing-workflow-runs/manually-running-a-workflow#running-a-workflow-using-github-cli)
					* [procedure for manually running a workflow using the REST API](https://docs.github.com/en/actions/managing-workflow-runs/manually-running-a-workflow#running-a-workflow-using-the-rest-api)<p>
	* define your settings for the different input URL-Groups
		```yml
		##############################################################
		# FIRST URL-GROUP | DEFINE YOUR ENV IN THE FOLLOWING
		##############################################################
		-	NAME: 'URL-GROUP 1'
			URLS: 'https://github.com/sitdisch https://github.com/mythemeway'
			BADGES_ARGS: '-b pagespeed -o lighthouse_results/first_group -r'
		#	TOKEN_NAME:
		#	REPO_BRANCH:
		#	AUDIT_TYPE:
		#	MOBILE_LIGHTHOUSE_PARAMS:
		#	DESKTOP_LIGHTHOUSE-PARAMS:
		#	USER_NAME:
		#	USER_EMAIL:
		#	COMMIT_MESSAGE: # e.g. 'Lighthouse-Badger[bot]: Results Added | First URL-Group'
		##############################################################
		# SECOND URL-GROUP | DEFINE YOUR ENV IN THE FOLLOWING
		##############################################################
		-	NAME: 'URL-GROUP 2'
			URLS: 'https://mythemeway.github.io/Dark-Particle/ https://mythemeway.github.io/Dark-Particle/projects/2020/10/31/project-1.html'
			BADGES_ARGS: '-b flat -o lighthouse_results/second_group -r'
		#	TOKEN_NAME: # e.g. 'LIGHTHOUSE_BADGER_TOKEN_2'
		#	REPO_BRANCH: # e.g. 'dummy/mytargetrepo_2 master'
		#	AUDIT_TYPE:
		#	MOBILE_LIGHTHOUSE_PARAMS:
		#	DESKTOP_LIGHTHOUSE_PARAMS:
		#	USER_NAME:
		#	USER_EMAIL:
		#	COMMIT_MESSAGE: # e.g. 'Lighthouse-Badger[bot]: Results Added | Second URL-Group'
		##############################################################
		# THIRD URL-GROUP | FEEL FREE TO ADD MORE URL-GROUPS...
		```
		* CONSIDER: 
			* you just have to define `NAME`, `URLS` and `BADGES_ARGS` for each group; if you do not define any of the other inputs, your predefined defaults will be used instead
			* `BADGES_ARGS`: 
				* more information about the optional arguments can be found [here](https://github.com/sitdisch/lighthouse-badges#help "Go there")
				* set different output-paths for different groups
				* in contrast to the Lighthouse-Badges repository
					* do not enter any URL(s) here
					* mobile or/and desktop is/are always added to your output-path
			* `TOKEN_NAME`: never enter the actual value of the personal access token
			* only a maximum of <b>256 URL-Groups</b> per workflow run is possible [[GitHub restriction](https://docs.github.com/en/actions/reference/workflow-syntax-for-github-actions#jobsjob_idstrategymatrix "Go there")]

That's it. Happy audits.

</details><p>

## | Known issues & possible solutions
* No scores are displayed in the pagespeed.svg file.
	* They are there, if not, NA is inserted. Try opening the SVG with a browser and the scores will pop up, I promise.
* You get a failed job because not all remote commits were fetched during parallel computing.
	* increase `max_push_attempts` in your workflow file (default = 5)
* The repository size is growing continuously due to the automatic updating of the badges.
	* The [Branch-Pruner](https://github.com/myactionway/branch-pruner-action "Get it") can help. E.&nbsp;g. put your Lighthouse results on a separate branch and automatically prune that branch with the Pruner, as you like. That way, you have the repo size under control and also the ability to see the latest history of your badges and reports without the really old stuff. 
* The workflow logs do not provide enough detail to diagnose why a workflow, job, or step is not working as expected.
	* enable [addition debug logging](https://docs.github.com/en/actions/managing-workflow-runs/enabling-debug-logging)
* You are experiencing strange behavior from GitHub actions.
	* maybe it's a general incident [[status check](https://www.githubstatus.com/ "Check it")]
* Your workflow trigger `schedule` doesn't fire.
	* in my experience, a workflow file with this trigger must be placed in the default branch
	* in this [chat](https://github.community/t/schedule-workflows-missing/17653/3 "Go there") Brightran said: <i>"... The workaround is to push something to trigger them. ..."</i> and Hless said: <i>"... It appears to me that it takes while before schedules actions run at all in a new repo"</i>. In my experience, they are right.

## | Application example
<a href="https://github.com/mythemeway/Dark-Particle" title="Check it out" target="_blank"><img src="https://raw.githubusercontent.com/sitdisch/cloud/master/gifs/lighthouse_badger_example.gif" /></a>
