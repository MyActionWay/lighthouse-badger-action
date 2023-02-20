<div align='center'>
<h1>Lighthouse-Badger | GitHub Action</h1>
<img src="https://repository-images.githubusercontent.com/359827195/1a084a2e-f30b-4c5d-b4a8-a3ce60d6f945"/><br><br>

<a title="Check it out" target="_blank" href="https://github.com/GoogleChrome/lighthouse"><img src="https://img.shields.io/github/package-json/dependency-version/myactionway/lighthouse-badges/lighthouse?label=Lighthouse&logo=lighthouse&cacheSeconds=3600" /></a><br>
<img src="https://img.shields.io/github/repo-size/myactionway/lighthouse-badger-action?label=RepoSize&cacheSeconds=3600" />
<a title="Check it out" target="_blank" href="https://github.com/myactionway/lighthouse-badger-action/blob/main/LICENSE.txt"><img src="https://raw.githubusercontent.com/sitdisch/cloud/master/badges/particle/License-MIT.svg" /></a>
<a title="Check it out" target="_blank" href="https://github.com/MyActionWay/lighthouse-badger-action/releases"><img src="https://img.shields.io/github/v/release/myactionway/lighthouse-badger-action?label=LastRelease&cacheSeconds=3600" /></a><br>
<a title="Explore it" target="_blank" href="https://snyk.io/test/github/MyActionWay/lighthouse-badges"><img alt="Snyk Vulnerabilities" src="https://img.shields.io/badge/Snyk-Vulnerabilities-2A2E30.svg?logo=snyk&cacheSeconds=3600" /></a><br>
<a title="Explore it" target="_blank" href="https://snyk.io/test/github/MyActionWay/lighthouse-badges"><img loading="eager" alt="&nbsp;pending..." height="25" src="https://img.shields.io/snyk/vulnerabilities/github/MyActionWay/lighthouse-badges?label=&cacheSeconds=3600" /></a><br>
<b>Full Report: <a title="Check it out" target="_blank" href="https://snyk.io/test/github/MyActionWay/lighthouse-badges">Last&nbsp;One</a></b><br>
[ <a title="Check it out" target="_blank" href="https://github.com/myactionway/lighthouse-badger-workflows">Workflow Readme</a> == <a title="Check it out" target="_blank" href="https://github.com/myactionway/lighthouse-badger-action">Action Readme</a> ]
</div><br>

The [Lighthouse-Badger](https://github.com/myactionway/lighthouse-badger-action "Get it") GitHub action makes it easy to manually/automatically generate, add and update Lighthouse badges and reports from one/multiple input URL-group(s) to one/multiple target repo(s)/branch(es) in parallel.

Once you have it [set up](#-setups "Go there"), you only need to add the links to the results once in your use case (e.&nbsp;g. Github readme, website,...). The [Lighthouse-Badger](https://github.com/myactionway/lighthouse-badger-action "Get it") will then automatically keep the results up to date for you. So sit back and let the Badger do the job :wink:.

> <b>**Warning**: Don't embed your SVG badge files via URLs containing content hashes from GitHub. Otherwise, your badges will not automatically update in your use case</b> [[more info](#-known-issues--possible-solutions "Go there")].

<br>

## | Credits

I, [Sitdisch](https://github.com/sitdisch "Visit me"), created the [Lighthouse-Badger](https://github.com/myactionway/lighthouse-badger-action "Get it") because I needed a GitHub action that would automatically update my Lighthouse badges and reports on a regular basis and I haven't found a suitable solution.

The badge creation is based on the [Lighthouse-Badges](https://github.com/emazzotta/lighthouse-badges "Go there") repository [License: [MIT](https://github.com/emazzotta/lighthouse-badges/blob/master/LICENSE.md "Go there"); Copyright: © 2018 [Emanuele Mazzotta](https://github.com/emazzotta "Visit him"); Changes: made] and the pagespeed badge on the [Readme-Pagespeed-Insights](https://github.com/ankurparihar/readme-pagespeed-insights "Go there") repository [License: [Apache-2.0](https://github.com/ankurparihar/readme-pagespeed-insights/blob/master/LICENSE "Go there"); Copyright: © 2021 [Ankur Parihar](https://github.com/ankurparihar "Visit him"); Changes: made]. Check out both. They are magnificent and maybe better suited for your use case than the [Lighthouse-Badger](https://github.com/myactionway/lighthouse-badger-action "Get it").

Last but not least, everything is based on the extraordinary work of the contributors to the <a title="Visit the Lighthouse" target="_blank" href="https://github.com/GoogleChrome/lighthouse"><img align="top" src="https://raw.githubusercontent.com/GoogleChrome/lighthouse/master/assets/lighthouse-logo.svg" width="25"/> GoogleChrome/lighthouse</a> repository [License: [Apache-2.0](https://github.com/GoogleChrome/lighthouse/blob/master/LICENSE)] <b>"Chapeau!"</b>.

P.S. the badger and military medal icon are from the [googlefonts/noto-emoji](https://github.com/googlefonts/noto-emoji "Go there") repository [License: [Apache-2.0](https://github.com/googlefonts/noto-emoji/blob/main/LICENSE)].<br><br>

## | Previews

### Pagespeed Badge

<img width="700" src="https://raw.githubusercontent.com/sitdisch/lighthouse-badges/master/assets/img/scores/pagespeed.svg"/>

### Plastic Badges

<img src="https://raw.githubusercontent.com/sitdisch/lighthouse-badges/master/assets/img/scores/lighthouse_performance.svg"/> <img src="https://raw.githubusercontent.com/sitdisch/lighthouse-badges/master/assets/img/scores/lighthouse_accessibility.svg"/> <img src="https://raw.githubusercontent.com/sitdisch/lighthouse-badges/master/assets/img/scores/lighthouse_best-practices.svg"/> <img src="https://raw.githubusercontent.com/sitdisch/lighthouse-badges/master/assets/img/scores/lighthouse_seo.svg"/> <img src="https://raw.githubusercontent.com/sitdisch/lighthouse-badges/master/assets/img/scores/lighthouse_pwa.svg"/>

### Single Plastic Badge

<img src="https://raw.githubusercontent.com/sitdisch/lighthouse-badges/master/assets/img/scores/lighthouse.svg"/>

### Reports

The awesome [htmlpreview.github.com](https://github.com/htmlpreview/htmlpreview.github.com) repository makes it easy to show up your Lighthouse reports instantly rendered. Just put this `https://htmlpreview.github.io/?` before the URL where you placed your Lighthouse report e.&nbsp;g. `https://htmlpreview.github.io/?https://github.com/sitdisch/cloud/blob/master/lighthouse_results/dark_particle/desktop/mythemeway_github_io_dark_particle_.html`<br>

Examples: <a href="https://htmlpreview.github.io/?https://raw.githubusercontent.com/sitdisch/cloud/master/lighthouse_results/dark_particle/desktop/mythemeway_github_io_dark_particle_.html" title="Check it out" target="_blank">Main Page </a> | <a href="https://htmlpreview.github.io/?https://raw.githubusercontent.com/sitdisch/cloud/master/lighthouse_results/dark_particle/desktop/mythemeway_github_io_dark_particle_projects_2020_10_31_project_1_html.html" title="Check it out" target="_blank">Project Page</a>

<a href="https://htmlpreview.github.io/?https://raw.githubusercontent.com/sitdisch/cloud/master/lighthouse_results/dark_particle/desktop/mythemeway_github_io_dark_particle_.html" title="Check it out" target="_blank"><img width="600" src="https://raw.githubusercontent.com/sitdisch/cloud/master/images/lighthousebadger_report.png" /></a><br><br>

## | Setups

First, choose a workflow file:

### [lighthouse-badger-easy.yml](https://github.com/MyActionWay/lighthouse-badger-workflows/blob/main/.github/workflows/lighthouse-badger-easy.yml "Get it")
Generates, adds & updates manually/automatically Lighthouse badges & reports from one/multiple input <b>URL(s) to the current repository & main branch with minimal settings</b>.

<details><summary><b>Set it up (click to toggle)</b></summary>

<p>

> <details><summary><b>1. add the lighthouse-badger-easy.yml workflow file to a repository</b></summary>
> 
>	* [get the file](https://github.com/MyActionWay/lighthouse-badger-workflows/blob/main/.github/workflows/lighthouse-badger-easy.yml "Get it")
> 
>	* it has to be the target repository where you want to add the Lighthouse results (this is not the case with the other workflow files)
>	* the path has to be `.github/workflows/lighthouse-badger-easy.yml`
> 
> </details>

> <details><summary><b>2. create a new encrypted repository secret</b></summary>
> 
>	* [see how to do this in general](https://docs.github.com/en/actions/reference/encrypted-secrets#creating-encrypted-secrets-for-a-repository "Learn how")
>	
>	* give the secret a name e.&nbsp;g. `LIGHTHOUSE_BADGER_TOKEN`
>	* the value of the secret must be the value of the Personal Access Token (PAT) for the repository where you want to add the Lighthouse results
>		* procedure for creating a [PAT (fine-grained)](https://docs.github.com/en/authentication/keeping-your-account-and-data-secure/creating-a-personal-access-token#creating-a-fine-grained-personal-access-token "Learn how") or a [PAT (classic)](https://docs.github.com/en/authentication/keeping-your-account-and-data-secure/creating-a-personal-access-token#creating-a-personal-access-token-classic "Learn how")
>		
>		* select only the minimum scopes and permissions required
>			* PAT (fine-grained): repository permissions
>			
>				 * contents => access: read and write
>				 
>				 * metadata => access: read-only
>				 
>			* PAT (classic): e.&nbsp;g. repo
>			
>		* <b>CONSIDER</b>: [PAT expiration](https://docs.github.com/en/authentication/keeping-your-account-and-data-secure/token-expiration-and-revocation) requires you to regenerate the PAT and set it as the secret's value again
>		
>	* add the secret to the same repository where you added this workflow file
> 
> </details>

> <details><summary><b>3. adapt your lighthouse-badger-easy.yml file</b></summary>
> 
> <p>
> 
> <details><summary><b>&nbsp;3.1 for manual triggers</b></summary>
>	
> 	* you don't have to adjust anything in the workflow file; just use it
> 	
> 		* [procedure for manually running a workflow on GitHub](https://docs.github.com/en/actions/managing-workflow-runs/manually-running-a-workflow#running-a-workflow-on-github "Learn how")
> 		
> 			<img src="https://raw.githubusercontent.com/sitdisch/cloud/master/images/lighthousebadger_minimal_manual_inputs.png" />
> 		* [procedure for manually running a workflow using the GitHub CLI](https://docs.github.com/en/actions/managing-workflow-runs/manually-running-a-workflow#running-a-workflow-using-github-cli)
> 		* [procedure for manually running a workflow using the REST API](https://docs.github.com/en/actions/managing-workflow-runs/manually-running-a-workflow#running-a-workflow-using-the-rest-api)
> 
> </details>
> 
> <details><summary><b>&nbsp;3.2 for all other triggers</b></summary>
>	
> 	* adapt this section:
> 		```yml
> 		##############################################################
> 		# DEFINE YOUR INPUTS AND TRIGGERS IN THE FOLLOWING
> 		##############################################################
> 		
> 		# INPUTS as environmental variables (env)
> 		env:
> 			URLS: # URL(s) to be checked e.g. 'https://github.com/sitdisch https://github.com/mythemeway'
> 			TOKEN_NAME: # target token name e.g. 'LIGHTHOUSE_BADGER_TOKEN'
> 		
> 		# TRIGGERS
> 		on:
> 		#	page_build:
> 		#	schedule:
> 		#		- cron: '55 23 * * 0'
> 		```
> 		
> 		<b>CONSIDER</b>:
> 		* INPUTS:
> 		
> 			* you only have to define `URLS` and `TOKEN_NAME`;
> 			
> 			* `TOKEN_NAME`: never enter the actual value of the personal access token
> 		* TRIGGERS:
> 			* `page_build`: Lighthouse results are generated every time after the GitHub page is built
> 			
> 			* `schedule`:
> 				* e.&nbsp;g. `cron: '55 23 * * 0'` executes the [Lighthouse-Badger](https://github.com/myactionway/lighthouse-badger-action "Get it") every Sunday at 23:55
> 				
> 				* you can check your inputs [here](https://crontab.guru/ "Go there")
> 		* hidden defaults (changeable with the other workflow files):
> 			* target repository & branch: Repository with this workflow file and main branch
> 			
> 			* outputs:
> 				* badges: pagespeed.svg
> 				
> 				* reports: yes
> 				* output-paths: 
> 					* lighthouse_results/mobile
> 					
> 					* lighthouse_results/desktop
> 			* audit types:
> 				* mobile:
> 					* parameters: '--throttling.cpuSlowdownMultiplier=2' 		
> 					
> 				* desktop:
> 					* parameters: '--throttling.cpuSlowdownMultiplier=1'
> 			* other settings:
> 				* user who commit: github-actions[bot]
> 				
> 				* user e-mail address: 41898282+github-actions[bot]@users.noreply.github.com
> 				* commit message: Lighthouse-Badger[bot]: Results Added
> 
> <b>That's it. Happy audits.</b>
>	
> </details>
>
> </p>
> 
> </details>

</p>

</details>

### [lighthouse-badger-default.yml](https://github.com/MyActionWay/lighthouse-badger-workflows/blob/main/.github/workflows/lighthouse-badger-default.yml "Get it")
Generates, adds & updates manually/automatically Lighthouse badges & reports from one/multiple input <b>URL(s) to a selected target repository & branch</b>.

<details><summary><b>Set it up (click to toggle)</b></summary>

<p>

> <details><summary><b>1. add the lighthouse-badger-default.yml workflow file to a repository</b></summary>
> 
>	* [get the file](https://github.com/MyActionWay/lighthouse-badger-workflows/blob/main/.github/workflows/lighthouse-badger-default.yml "Get it")
> 
> 	* it doesn't have to be the repository where you want to add the Lighthouse results; e.&nbsp;g., you can simply [fork](https://github.com/myactionway/lighthouse-badger-workflows/fork "fork it") the `myactionway/lighthouse-badger-workflows` repository
> 		* <b>CONSIDER</b>: with a forked repository, you need to confirm that you want to use a workflow before you can actually use it (repo menu > actions tab > push the button)
> 	* the path has to be `.github/workflows/lighthouse-badger-default.yml`
> 
> </details>

> <details><summary><b>2. create a new encrypted repository secret</b></summary>
> 
>	* [see how to do this in general](https://docs.github.com/en/actions/reference/encrypted-secrets#creating-encrypted-secrets-for-a-repository "Learn how")
>	
>	* give the secret a name e.&nbsp;g. `LIGHTHOUSE_BADGER_TOKEN`
>	* the value of the secret must be the value of the Personal Access Token (PAT) for the repository where you want to add the Lighthouse results
>		* procedure for creating a [PAT (fine-grained)](https://docs.github.com/en/authentication/keeping-your-account-and-data-secure/creating-a-personal-access-token#creating-a-fine-grained-personal-access-token "Learn how") or a [PAT (classic)](https://docs.github.com/en/authentication/keeping-your-account-and-data-secure/creating-a-personal-access-token#creating-a-personal-access-token-classic "Learn how")
>		
>		* select only the minimum scopes and permissions required
>			* PAT (fine-grained): repository permissions
>			
>				 * contents => access: read and write
>				 
>				 * metadata => access: read-only
>				 
>			* PAT (classic): e.&nbsp;g. repo
>			
>		* <b>CONSIDER</b>: [PAT expiration](https://docs.github.com/en/authentication/keeping-your-account-and-data-secure/token-expiration-and-revocation) requires you to regenerate the PAT and set it as the secret's value again
>		
> * add the secret to the same repository where you added this workflow file
> 
> </details>

> <details><summary><b>3. adapt your lighthouse-badger-default.yml file</b></summary>
> 
> <p>
> 
> <details><summary><b>&nbsp;3.1 for manual triggers</b></summary>
>	
> 	* you don't have to adjust anything in the workflow file; just use it
> 	
> 		* [procedure for manually running a workflow on GitHub](https://docs.github.com/en/actions/managing-workflow-runs/manually-running-a-workflow#running-a-workflow-on-github "Learn how")
> 		
> 			<img src="https://raw.githubusercontent.com/sitdisch/cloud/master/images/lighthousebadger_manual_inputs.png" />
> 		* [procedure for manually running a workflow using the GitHub CLI](https://docs.github.com/en/actions/managing-workflow-runs/manually-running-a-workflow#running-a-workflow-using-github-cli)
> 		* [procedure for manually running a workflow using the REST API](https://docs.github.com/en/actions/managing-workflow-runs/manually-running-a-workflow#running-a-workflow-using-the-rest-api)
> 
> </details>
> 
> <details><summary><b>&nbsp;3.2 for all other triggers</b></summary>
>	
> 	* adapt this section:
> 		```yml
> 		##############################################################
> 		# DEFINE YOUR INPUTS AND TRIGGERS IN THE FOLLOWING
> 		##############################################################
> 
> 		# INPUTS as environmental variables (env)
> 		env:
> 			URLS: # URL(s) to be checked e.g. 'https://github.com/sitdisch https://github.com/mythemeway'
> 			TOKEN_NAME: # target token name e.g. 'LIGHTHOUSE_BADGER_TOKEN'
> 			REPO_BRANCH: # target repository & branch e.g. 'dummy/mytargetrepo main'
> 			BADGES_ARGS: # badge-style '-b {flat,...}', preceding-label '-l "Lighthouse "', output-path '-o lighthouse_results/dummy', save-report '-r', single-badge '-s'
> 			AUDIT_TYPE: # 'mobile', 'desktop', 'both' or 'both_p' 
> 			MOBILE_LIGHTHOUSE_PARAMS: # Lighthouse parameters mobile audit
> 			DESKTOP_LIGHTHOUSE_PARAMS: # Lighthouse parameters desktop audit
> 			USER_NAME: # user who should commit e.g. 'dummy'
> 			USER_EMAIL: # e.g. 'dummy@gmail.com'
> 			COMMIT_MESSAGE: # e.g. 'Lighthouse results added'
> 
> 		# TRIGGERS
> 		on:
> 		#	page_build:
> 		#	schedule:
> 		#		- cron: '55 23 * * 0'
> 		```
> 		
> 		<b>CONSIDER</b>:
> 		* INPUTS:
> 		
> 			* you only have to define `URLS` and `TOKEN_NAME`; if any other input is blank, one of these default values will be used instead
> 				```yml
> 				DEFAULT_REPO_BRANCH: '${{ github.repository }} main' # repo with this file and main branch
> 				DEFAULT_BADGES_ARGS: '-b pagespeed -o lighthouse_results -r'
> 				DEFAULT_AUDIT_TYPE: 'both'
> 				DEFAULT_MOBILE_LIGHTHOUSE_PARAMS: '--throttling.cpuSlowdownMultiplier=2'
> 				DEFAULT_DESKTOP_LIGHTHOUSE_PARAMS: '--preset=desktop --throttling.cpuSlowdownMultiplier=1'
> 				DEFAULT_USER_NAME: 'github-actions[bot]'
> 				DEFAULT_USER_EMAIL: '41898282+github-actions[bot]@users.noreply.github.com'
> 				DEFAULT_COMMIT_MESSAGE: 'Lighthouse-Badger[bot]: Results Added'
> 				```
> 			* `TOKEN_NAME`: never enter the actual value of the personal access token
> 			
> 			* `BADGES_ARGS`: 
> 				* more information about the optional arguments can be found [here](https://github.com/sitdisch/lighthouse-badges#help "Go there")
> 				
> 				* in contrast to the Lighthouse-Badges repository
> 					* do not enter any URL(s) here
> 					
> 					* mobile or/and desktop is/are always added to your output-path
> 			* `MOBILE/DESKTOP_LIGHTHOUSE_PARAMS`:
> 				* more information about the optional arguments can be found [here](https://github.com/GoogleChrome/lighthouse#cli-options)
> 			* `AUDIT_TYPE`:
> 				* `'both_p'`: desktop and mobile audits are carried out in parallel
> 				
> 					* <b>it's not recommended</b> as it can skew the performance results [<a title="Check it out" target="_blank" href="https://github.com/GoogleChrome/lighthouse/issues/7104#issuecomment-458368476">source</a>] and it can also be slower than `'both'`
> 		* TRIGGERS:
> 			* `page_build`: Lighthouse results are generated every time after the GitHub page is built
> 			
> 			* `schedule`:
> 				* e.&nbsp;g. `cron: '55 23 * * 0'` executes the [Lighthouse-Badger](https://github.com/myactionway/lighthouse-badger-action "Get it") every Sunday at 23:55
> 				
> 				* you can check your inputs [here](https://crontab.guru/ "Go there")
> 
> <b>That's it. Happy audits.</b>
>	
> </details>
>
> </p>
> 
> </details>

</p>

</details>

### [lighthouse-badger-advanced.yml](https://github.com/MyActionWay/lighthouse-badger-workflows/blob/main/.github/workflows/lighthouse-badger-advanced.yml "Get it")
Generates, adds & updates manually/automatically Lighthouse badges & reports from one/multiple input <b>URL-group(s) to one/multiple target repo(s)/branch(es) in parallel</b>.

<details><summary><b>Set it up (click to toggle)</b></summary>

<p>

> <details><summary><b>1. add the lighthouse-badger-advanced.yml workflow file to a repository</b></summary>
> 
>	* [get the file](https://github.com/MyActionWay/lighthouse-badger-workflows/blob/main/.github/workflows/lighthouse-badger-advanced.yml "Get it")
>	
>	* it doesn't have to be a repository where you want to add Lighthouse results; e.&nbsp;g., you can simply [fork](https://github.com/myactionway/lighthouse-badger-workflows/fork "fork it") the `myactionway/lighthouse-badger-workflows` repository
>		* <b>CONSIDER</b>: with a forked repository, you need to confirm that you want to use a workflow before you can actually use it (repo menu > actions tab > push the button)
>	* the path has to be `.github/workflows/lighthouse-badger-advanced.yml`
>
> </details>

> <details><summary><b>2. create new encrypted repository secrets</b></summary>
> 
>	* [see how to do this in general](https://docs.github.com/en/actions/reference/encrypted-secrets#creating-encrypted-secrets-for-a-repository "Learn how")
>	
>	* give the secrets names e.&nbsp;g. `LIGHTHOUSE_BADGER_TOKEN_1` and `LIGHTHOUSE_BADGER_TOKEN_2`
>	* the values of the secrets must be the values of the Personal Access Tokens (PAT) for the repositories where you want to add the Lighthouse results
>		* procedure for creating a [PAT (fine-grained)](https://docs.github.com/en/authentication/keeping-your-account-and-data-secure/creating-a-personal-access-token#creating-a-fine-grained-personal-access-token "Learn how") or a [PAT (classic)](https://docs.github.com/en/authentication/keeping-your-account-and-data-secure/creating-a-personal-access-token#creating-a-personal-access-token-classic "Learn how")
>		
>		* select only the minimum scopes and permissions required
>			* PAT (fine-grained): repository permissions
>			
>				 * contents => access: read and write
>				 
>				 * metadata => access: read-only
>				 
>			* PAT (classic): e.&nbsp;g. repo
>			
>		* <b>CONSIDER</b>: [PAT expiration](https://docs.github.com/en/authentication/keeping-your-account-and-data-secure/token-expiration-and-revocation) requires you to regenerate the PAT and set it as the secret's value again
>		
>	* add the secrets to the same repository where you added this workflow file
>
> </details>

> <details><summary><b>3. adapt your lighthouse-badger-advanced.yml file</b></summary>
> 
> <p>
> 
> <details><summary><b>&nbsp;3.1 define your defaults</b></summary>
>	
> 	* adapt this section:
> 		```yml
> 		##############################################################
> 		# DEFINE YOUR DEFAULTS (INPUTS & TRIGGERS) IN THE FOLLOWING
> 		##############################################################
> 	
> 		# INPUTS as environmental variables (env)
> 		env:
>    		TOKEN_NAME: # target token name e.g. 'LIGHTHOUSE_BADGER_TOKEN_1'
>    		REPO_BRANCH: # target repository & branch e.g. 'dummy/mytargetrepo_1 main'
>    		AUDIT_TYPE: # 'mobile', 'desktop', 'both' or 'both_p' 
>    		MOBILE_LIGHTHOUSE_PARAMS: # Lighthouse parameters mobile audit
>    		DESKTOP_LIGHTHOUSE_PARAMS: # Lighthouse parameters desktop audit
>    		USER_NAME: # user who should commit e.g. 'dummy'
>    		USER_EMAIL: # e.g. 'dummy@gmail.com'
>    		COMMIT_MESSAGE: # e.g. 'Lighthouse results added'
> 	
> 		# TRIGGERS
> 		on:
> 		#	page_build:
> 		#	schedule:
> 		#		- cron: '55 23 * * 0'
>  	 		workflow_dispatch:
> 		```
> 		
> 		<b>CONSIDER</b>:
> 		* INPUTS:
> 
> 			* `TOKEN_NAME`: never enter the actual value of the personal access token
> 
> 			* all inputs except `TOKEN_NAME` have predefined values; you can, but you don't have to overwrite them
> 				```yml
> 				# Predefined values
> 				REPO_BRANCH: '${{ github.repository }} main' # repo with this file and main branch
> 				AUDIT_TYPE: 'both'
> 				MOBILE_LIGHTHOUSE_PARAMS: '--throttling.cpuSlowdownMultiplier=2'
> 				DESKTOP_LIGHTHOUSE_PARAMS: '--preset=desktop --throttling.cpuSlowdownMultiplier=1'
> 				USER_NAME: 'github-actions[bot]'
> 				USER_EMAIL: '41898282+github-actions[bot]@users.noreply.github.com'
> 				COMMIT_MESSAGE: 'Lighthouse-Badger[bot]: Results Added'
> 				```
> 			* `MOBILE/DESKTOP_LIGHTHOUSE_PARAMS`:
> 				* more information about the optional arguments can be found [here](https://github.com/GoogleChrome/lighthouse#cli-options)
> 			* `AUDIT_TYPE`:
> 				* `'both_p'`: desktop and mobile audits are carried out in parallel
> 
> 					* <b>it's not recommended</b> as it can skew the performance results [<a title="Check it out" target="_blank" href="https://github.com/GoogleChrome/lighthouse/issues/7104#issuecomment-458368476">source</a>] and it can also be slower than `'both'`
> 		* TRIGGERS:
> 			* `page_build`: Lighthouse results are generated every time after the GitHub page is built
> 
> 			* `schedule`:
> 				* e.&nbsp;g. `cron: '55 23 * * 0'` executes the [Lighthouse-Badger](https://github.com/myactionway/lighthouse-badger-action "Get it") every Sunday at 23:55
> 
> 				* you can check your inputs [here](https://crontab.guru/ "Go there")
> 			* `workflow_dispatch`:
> 				* no predefined inputs; the `env` defined in this workflow file are used instead when this trigger is triggered
> 
> 				* [procedure for manually running a workflow on GitHub](https://docs.github.com/en/actions/managing-workflow-runs/manually-running-a-workflow#running-a-workflow-on-github "Learn how")
> 				* [procedure for manually running a workflow using the GitHub CLI](https://docs.github.com/en/actions/managing-workflow-runs/manually-running-a-workflow#running-a-workflow-using-github-cli)
> 				* [procedure for manually running a workflow using the REST API](https://docs.github.com/en/actions/managing-workflow-runs/manually-running-a-workflow#running-a-workflow-using-the-rest-api)
> 
> </details>
> 
> <details><summary><b>&nbsp;3.2 define your settings for the different input URL-Groups</b></summary>
>	
> 	* adapt this section:
> 		```yml
> 		##############################################################
> 		# FIRST URL-GROUP | DEFINE YOUR ENV IN THE FOLLOWING
> 		##############################################################
> 		-	NAME: 'URL-GROUP 1'
>    		URLS: 'https://github.com/sitdisch https://github.com/mythemeway'
>    		BADGES_ARGS: '-b pagespeed -o lighthouse_results/first_group -r'
> 		#	TOKEN_NAME:
> 		#	REPO_BRANCH:
> 		#	AUDIT_TYPE:
> 		#	MOBILE_LIGHTHOUSE_PARAMS:
> 		#	DESKTOP_LIGHTHOUSE-PARAMS:
> 		#	USER_NAME:
> 		#	USER_EMAIL:
> 		#	COMMIT_MESSAGE: # e.g. 'Lighthouse-Badger[bot]: Results Added | First URL-Group'
> 		##############################################################
> 		# SECOND URL-GROUP | DEFINE YOUR ENV IN THE FOLLOWING
> 		##############################################################
> 		-	NAME: 'URL-GROUP 2'
>    		URLS: 'https://mythemeway.github.io/Dark-Particle/ https://mythemeway.github.io/Dark-Particle/projects/2020/10/31/project-1.html'
>    		BADGES_ARGS: '-b flat -o lighthouse_results/second_group -r'
> 		#	TOKEN_NAME: # e.g. 'LIGHTHOUSE_BADGER_TOKEN_2'
> 		#	REPO_BRANCH: # e.g. 'dummy/mytargetrepo_2 main'
> 		#	AUDIT_TYPE:
> 		#	MOBILE_LIGHTHOUSE_PARAMS:
> 		#	DESKTOP_LIGHTHOUSE_PARAMS:
> 		#	USER_NAME:
> 		#	USER_EMAIL:
> 		#	COMMIT_MESSAGE: # e.g. 'Lighthouse-Badger[bot]: Results Added | Second URL-Group'
> 		##############################################################
> 		# THIRD URL-GROUP | FEEL FREE TO ADD MORE URL-GROUPS...
> 		```
> 		<b>CONSIDER</b>:
> 
> 		* you just have to define `NAME`, `URLS` and `BADGES_ARGS` for each group; if you do not define any of the other inputs, your predefined defaults will be used instead
> 
> 		* `BADGES_ARGS`: 
> 			* more information about the optional arguments can be found [here](https://github.com/sitdisch/lighthouse-badges#help "Go there")
> 
> 			* set different output-paths for different groups
> 			* in contrast to the Lighthouse-Badges repository
> 				* do not enter any URL(s) here
> 
> 				* mobile or/and desktop is/are always added to your output-path
> 		* `TOKEN_NAME`: never enter the actual value of the personal access token
> 		* only a maximum of <b>256 URL-Groups</b> per workflow run is possible [[GitHub restriction](https://docs.github.com/en/actions/reference/workflow-syntax-for-github-actions#jobsjob_idstrategymatrix "Go there")]
> 
> <b>That's it. Happy audits.</b>
>	
> </details>
>
> </p>
> 
> </details>

</p>

</details>

<br>

## | Known issues & possible solutions

> <details><summary><b>Your SVG badge file was not automatically updated in your use case:</b></summary>
>
> * You embedded your SVG badge file via a URL containing a content hash from GitHub.
> 
> 	* e.&nbsp;g. `https://raw.githubusercontent.com/sitdisch/lighthouse-badges/94ff556d0d5a451a56839813e6322da811fce9f6/assets/img/scores/pagespeed.svg` has the content hash `94ff556d0d5a451a56839813e6322da811fce9f6`
> 	
> 	* A badge embedded via such a URL will never be updated.
> 	* You get such a URL when you hover over a SVG file in your GitHub repository + `Right Mouse Click` + `Copy Image Link`
> * Instead, use a URL that includes the branch name where your badge is stored on GitHub.
> 	* e.&nbsp;g. `https://raw.githubusercontent.com/sitdisch/lighthouse-badges/master/assets/img/scores/pagespeed.svg`
> 	
> 	* here only the content hash `94ff556d0d5a451a56839813e6322da811fce9f6` is replaced by the branch name `master`
> 	* A badge embedded via such a URL can be updated automatically.
> 
></details>

> <details><summary><b><i>"Error: fatal: could not read Username for '<span>h</span>ttps://github.com': terminal prompts disabled":</i></b></summary>
> 
> <p>
> 
> * your [personal access token may has expired](https://docs.github.com/en/authentication/keeping-your-account-and-data-secure/token-expiration-and-revocation) and you need to set a new one as the value of the encrypted repository secret; that means back to the [setup section](#-setups "Go there")
> 
> * more information about this GitHub action checkout issue can be found e.&nbsp;g. [here](https://github.com/actions/checkout/issues/664)
> 
> </p>
> 
> </details>

> <details><summary><b><i>"remote: Permission to ... denied to ... fatal: unable to access '<span>h</span>ttps://github.com/...': The requested URL returned error: 403":</i></b></summary>
> 
> <p>
> 
> * your personal access token used does not have the minimum scopes/permissions required to add the Lighthouse results to your target repository
> 
> </p>
> 
> </details>

> <details><summary><b>No scores are displayed in the pagespeed.svg file:</b></summary>
> 
> <p>
> 
> * They are there, if not, `NA` is inserted. Try opening the SVG with a browser and the scores will pop up, I promise.
> 
> </p>
> 
> </details>

> <details><summary><b>You get a failed job because it exceeded the maximum execution time:</b></summary>
> 
> <p>
> 
> * increase `timeout-minutes` in your workflow file (default = 8min)
>
> * if that doesn't help, maybe it is a lighthouse issue
>
> </p>
> 
> </details>

> <details><summary><b>You get a failed job because not all remote commits were fetched during parallel computing:</b></summary>
> 
> <p>
> 
> * increase `max_push_attempts` in your workflow file (default = 5)
>
> </p>
> 
> </details>

> <details><summary><b>The repository size is growing continuously due to the automatic updating of the badges:</b></summary>
> 
> <p>
> 
> * The [Branch-Pruner <img align="top" width="70" src="https://repository-images.githubusercontent.com/352585266/cc34310b-3ab2-4085-b5f5-b1b2cc306a64"/>](https://github.com/myactionway/branch-pruner-action "Get it") can help. E.&nbsp;g. put your Lighthouse results on a separate branch and automatically prune that branch with the Pruner, as you like. That way, you have the repo size under control and also the ability to see the latest history of your badges and reports without the really old stuff. 
> 
> </p>
> 
> </details>

> <details><summary><b>The workflow logs do not provide enough detail to diagnose why a workflow, job, or step is not working as expected:</b></summary>
> 
> <p>
> 
> * enable [addition debug logging](https://docs.github.com/en/actions/managing-workflow-runs/enabling-debug-logging)
> 
> </p>
> 
> </details>

> <details><summary><b>You are experiencing strange behavior from GitHub actions:</b></summary>
> 
> <p>
> 
> * maybe it's a general incident [[status check](https://www.githubstatus.com/ "Check it")]
> 
> </p>
> 
> </details>

> <details><summary><b>Your workflow trigger schedule doesn't fire:</b></summary>
> 
> * in my experience, a workflow file with this trigger must be placed in the default branch
> 
> * in this [chat](https://github.community/t/schedule-workflows-missing/17653/3 "Go there") Brightran said: <i>"... The workaround is to push something to trigger them. ..."</i> and Hless said: <i>"... It appears to me that it takes while before schedules actions run at all in a new repo"</i>. In my experience, they are right.
> 
> </details>

<br>

## | Application example
<a href="https://github.com/mythemeway/Dark-Particle" title="Check it out" target="_blank"><img width="600" src="https://raw.githubusercontent.com/sitdisch/cloud/master/gifs/lighthouse_badger_example.gif" /></a>

<br>

## | Appendix

### Note on protected brand names and logos
> * The use of protected brand names, trade names, utility models and brand logos on this website does not constitute an infringement of copyright; rather, it serves as an illustrative note. Even if this is not marked as such at the respective points, the corresponding legal provisions always apply.
>
> * The brand names and logos used are the property of their respective owners and are subject to their copyright provisions.
> * This offer is in no way related to the legal entities of the protected brand names and logos used.

### Note on liability for links
> * This README contains links to external third-party websites. The README operator has no influence on the content of these sites. Therefore, he cannot assume any liability. Instead, the respective provider is always responsible for the content.
>
> * The linked pages were checked for possible legal violations at the time of linking and illegal content wasn't discernible. A permanent control of the linked pages is unreasonable without concrete evidence of an infringement. However, if the README operator becomes aware of such a violation, he will act immediately. 

### Readme uses
> * [Simple Icons](https://simpleicons.org/ "Check it out") [License: [CC0&nbsp;1.0](https://github.com/simple-icons/simple-icons/blob/develop/LICENSE.md "Go there")]
> 
> * [Shields.io](https://github.com/badges/shields "Check it out") [License: [CC0&nbsp;1.0](https://github.com/badges/shields/blob/master/LICENSE "Go there")]
