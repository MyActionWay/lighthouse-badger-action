<h1 align="center">Lighthouse-Badger | GitHub Action</h1>
<p align="center"><img src="https://raw.githubusercontent.com/sitdisch/cloud/master/SVGs/badger.svg" width="300" /></p>
<p align="center"><a title="Check it out" target="_blank" href="https://github.com/GoogleChrome/lighthouse"><img src="https://raw.githubusercontent.com/GoogleChrome/lighthouse/master/assets/lighthouse-logo.svg" /></a></p>
<p align="center"><a title="Check it out" target="_blank" href="https://github.com/myactionway/lighthouse-badger-action/blob/master/LICENSE.txt"><img src="https://img.shields.io/github/license/myactionway/lighthouse-badger-action?label=License" /></a>
<img src="https://img.shields.io/github/repo-size/myactionway/lighthouse-badger-action?label=RepoSize" /></p>
<hr>

The [Lighthouse-Badger](https://github.com/myactionway/lighthouse-badger-action "Get it") GitHub action makes it easy to manually or automatically generate, add and update Lighthouse badges and reports from one/multiple input URL(s) to a selected target repository. If you've it [set up](#-setup "Go there"), you only need to add the result links to your use case once. Then the [Lighthouse-Badger](https://github.com/myactionway/lighthouse-badger-action "Get it") will automatically keep the badges up to date for you. So sit back and let the Badger do the job :wink:.

## | Credits

I, [Sitdisch](https://github.com/sitdisch "Visit me"), created the [Lighthouse-Badger](https://github.com/myactionway/lighthouse-badger-action "Get it") because I needed a GitHub action that would automatically update my Lighthouse badges on a regular basis and I haven't found a suitable solution. The badge creation is based on the [Lighthouse-Badges](https://github.com/emazzotta/lighthouse-badges "Go there") repository  [License: [MIT](https://github.com/emazzotta/lighthouse-badges/blob/master/LICENSE.md "Go there"); Copyright (c) 2018 [Emanuele Mazzotta](https://github.com/emazzotta "Visit him")] and the pagespeed badge on the [Readme-Pagespeed-Insights](https://github.com/ankurparihar/readme-pagespeed-insights "Go there") repository  [License: [Apache-2.0](https://github.com/ankurparihar/readme-pagespeed-insights/blob/master/LICENSE "Go there"); Copyright (c) 2021 [Ankur Parihar](https://github.com/ankurparihar "Visit him")]. Check out both. They are magnificent and maybe better suited for your use case than the [Lighthouse-Badger](https://github.com/myactionway/lighthouse-badger-action "Get it").

<div>The badger icon is made by <a href="https://www.freepik.com" title="Freepik">Freepik</a> from <a href="https://www.flaticon.com/" title="Flaticon">www.flaticon.com</a>.</div>

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

## | Setup

OK, let's do it.

1. add the [lighthouse-badger.yml](https://github.com/MyActionWay/lighthouse-badger-workflows/blob/master/.github/workflows/lighthouse-badger.yml "Get it") workflow file to a repository
	* the path has to be `.github/workflows/lighthouse-badger.yml`
	* it doesn't have to be the repository where you want to add the Lighthouse results; e.&nbsp;g., you can simply [fork](https://github.com/myactionway/lighthouse-badger-workflows/fork "fork it") the `myactionway/lighthouse-badger-workflows` repository
		* CONSIDER: with a forked repository, you need to confirm that you want to use a workflow before you can actually use it (repo menu > actions tab > push the button)
2. create a new encrypted repository secret [[procedure]](https://docs.github.com/en/actions/reference/encrypted-secrets#creating-encrypted-secrets-for-a-repository "Learn how")
	* add the secret to the same repository where you added the workflow file
	* give the secret a name e.&nbsp;g. `LIGHTHOUSE_BADGER_TOKEN`
	* the value of the secret must be the value of the personal access token for the repository where you want to add the Lighthouse results.
		* [procedure for creating a personal access token](https://docs.github.com/en/github/authenticating-to-github/creating-a-personal-access-token "Learn how")
		* select only the minimum scopes and permissions required e.&nbsp;g. repo
3. adapt your [lighthouse-badger.yml](https://github.com/MyActionWay/lighthouse-badger-workflows/blob/master/.github/workflows/lighthouse-badger.yml "Get it") file
	* for manual triggers
		* all you have to do is enter your secret name e.&nbsp;g. `LIGHTHOUSE_BADGER_TOKEN`
			```yml
			env:
			 # Token for all triggers
			 TOKEN: ${{ secrets.LIGHTHOUSE_BADGER_TOKEN }}
			```
			* CONSIDER: never enter the actual value of the personal access token
		* [procedure for manually running a workflow on GitHub](https://docs.github.com/en/actions/managing-workflow-runs/manually-running-a-workflow#running-a-workflow-on-github "Learn how")
			<img src="https://raw.githubusercontent.com/sitdisch/cloud/master/images/lighthousebadger_manual_inputs.png" />
			* CONSIDER: currently, you can't change the `TOKEN` in the UI
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
			# page_build:
			# schedule:
			#   - cron: '55 23 * * 0'
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

## | Known issues & possible solutions
* No scores are displayed in the pagespeed.svg file.
	* They are there, if not, NA is inserted. Try opening the SVG with a browser and the scores will pop up, I promise.
* The repository size is growing continuously due to the automatic updating of the badges.
	* The [Branch-Pruner](https://github.com/myactionway/branch-pruner-action "Get it") can help. E.&nbsp;g. put your Lighthouse results on a separate branch and automatically prune that branch with the Pruner, as you like. 
