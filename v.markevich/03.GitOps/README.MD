# 03.GitOps homework
## Need to create CI pipeline to find tabs in code
### Requirements:
* run on PR
* should scan all changed files
* checking all changed files in parallel
* result of found tabs should be inside artefacts of each build
### Pipeline log
```bash
2022-05-18T11:53:33.9312104Z Requested labels: ubuntu-latest
2022-05-18T11:53:33.9312155Z Job defined at: varkevich93/Script.test/.github/workflows/Tabs_Test.yaml@refs/pull/11/merge
2022-05-18T11:53:33.9312180Z Waiting for a runner to pick up this job...
2022-05-18T11:53:34.8370987Z Job is waiting for a hosted runner to come online.
2022-05-18T11:53:38.5677315Z Job is about to start running on the hosted runner: Hosted Agent (hosted)
2022-05-18T11:53:42.4937524Z Current runner version: '2.291.1'
2022-05-18T11:53:42.4973178Z ##[group]Operating System
2022-05-18T11:53:42.4973767Z Ubuntu
2022-05-18T11:53:42.4974239Z 20.04.4
2022-05-18T11:53:42.4974580Z LTS
2022-05-18T11:53:42.4974885Z ##[endgroup]
2022-05-18T11:53:42.4975292Z ##[group]Virtual Environment
2022-05-18T11:53:42.4975772Z Environment: ubuntu-20.04
2022-05-18T11:53:42.4976193Z Version: 20220508.1
2022-05-18T11:53:42.4976844Z Included Software: https://github.com/actions/virtual-environments/blob/ubuntu20/20220508.1/images/linux/Ubuntu2004-Readme.md
2022-05-18T11:53:42.4978006Z Image Release: https://github.com/actions/virtual-environments/releases/tag/ubuntu20%2F20220508.1
2022-05-18T11:53:42.4978526Z ##[endgroup]
2022-05-18T11:53:42.4978988Z ##[group]Virtual Environment Provisioner
2022-05-18T11:53:42.4979490Z 1.0.0.0-main-20220421-1
2022-05-18T11:53:42.4979823Z ##[endgroup]
2022-05-18T11:53:42.4980609Z ##[group]GITHUB_TOKEN Permissions
2022-05-18T11:53:42.4981260Z Contents: read
2022-05-18T11:53:42.4981871Z Metadata: read
2022-05-18T11:53:42.4982276Z ##[endgroup]
2022-05-18T11:53:42.4986430Z Secret source: Actions
2022-05-18T11:53:42.4986990Z Prepare workflow directory
2022-05-18T11:53:42.5992547Z Prepare all required actions
2022-05-18T11:53:42.6213356Z Getting action download info
2022-05-18T11:53:42.9155475Z Download action repository 'actions/checkout@v3' (SHA:2541b1294d2704b0964813337f33b291d3f8596b)
2022-05-18T11:53:43.2492818Z Download action repository 'tj-actions/changed-files@v19' (SHA:a6d456f542692915c5289ea834fb89bc07c11208)
2022-05-18T11:53:43.4010399Z Download action repository 'actions/upload-artifact@v2' (SHA:82c141cc518b40d92cc801eee768e7aafc9c2fa2)
2022-05-18T11:53:43.7055508Z Getting action download info
2022-05-18T11:53:43.8399084Z Download action repository 'tj-actions/glob@v7.16' (SHA:7e147c5f2fb842ce53357a35f14589222ee81b7f)
2022-05-18T11:53:44.1524428Z ##[group]Run actions/checkout@v3
2022-05-18T11:53:44.1524775Z with:
2022-05-18T11:53:44.1525028Z   fetch-depth: 0
2022-05-18T11:53:44.1525361Z   repository: varkevich93/Script.test
2022-05-18T11:53:44.1525927Z   token: ***
2022-05-18T11:53:44.1526166Z   ssh-strict: true
2022-05-18T11:53:44.1526452Z   persist-credentials: true
2022-05-18T11:53:44.1526736Z   clean: true
2022-05-18T11:53:44.1526961Z   lfs: false
2022-05-18T11:53:44.1527275Z   submodules: false
2022-05-18T11:53:44.1527554Z   set-safe-directory: true
2022-05-18T11:53:44.1527817Z ##[endgroup]
2022-05-18T11:53:44.5041571Z Syncing repository: varkevich93/Script.test
2022-05-18T11:53:44.5044339Z ##[group]Getting Git version info
2022-05-18T11:53:44.5045578Z Working directory is '/home/runner/work/Script.test/Script.test'
2022-05-18T11:53:44.5046840Z [command]/usr/bin/git version
2022-05-18T11:53:44.5217893Z git version 2.36.1
2022-05-18T11:53:44.5298417Z ##[endgroup]
2022-05-18T11:53:44.5315070Z Temporarily overriding HOME='/home/runner/work/_temp/45b9c8ea-ef72-4abd-b726-bfdb908d567b' before making global git config changes
2022-05-18T11:53:44.5315682Z Adding repository directory to the temporary git global config as a safe directory
2022-05-18T11:53:44.5317001Z [command]/usr/bin/git config --global --add safe.directory /home/runner/work/Script.test/Script.test
2022-05-18T11:53:44.5330997Z Deleting the contents of '/home/runner/work/Script.test/Script.test'
2022-05-18T11:53:44.5334183Z ##[group]Initializing the repository
2022-05-18T11:53:44.5338478Z [command]/usr/bin/git init /home/runner/work/Script.test/Script.test
2022-05-18T11:53:44.5445642Z hint: Using 'master' as the name for the initial branch. This default branch name
2022-05-18T11:53:44.5446210Z hint: is subject to change. To configure the initial branch name to use in all
2022-05-18T11:53:44.5446776Z hint: of your new repositories, which will suppress this warning, call:
2022-05-18T11:53:44.5447121Z hint: 
2022-05-18T11:53:44.5447567Z hint: 	git config --global init.defaultBranch <name>
2022-05-18T11:53:44.5447905Z hint: 
2022-05-18T11:53:44.5448348Z hint: Names commonly chosen instead of 'master' are 'main', 'trunk' and
2022-05-18T11:53:44.5449170Z hint: 'development'. The just-created branch can be renamed via this command:
2022-05-18T11:53:44.5449504Z hint: 
2022-05-18T11:53:44.5449819Z hint: 	git branch -m <name>
2022-05-18T11:53:44.5450233Z Initialized empty Git repository in /home/runner/work/Script.test/Script.test/.git/
2022-05-18T11:53:44.5450750Z [command]/usr/bin/git remote add origin https://github.com/varkevich93/Script.test
2022-05-18T11:53:44.5497999Z ##[endgroup]
2022-05-18T11:53:44.5498823Z ##[group]Disabling automatic garbage collection
2022-05-18T11:53:44.5505392Z [command]/usr/bin/git config --local gc.auto 0
2022-05-18T11:53:44.5543943Z ##[endgroup]
2022-05-18T11:53:44.5544909Z ##[group]Setting up auth
2022-05-18T11:53:44.5552932Z [command]/usr/bin/git config --local --name-only --get-regexp core\.sshCommand
2022-05-18T11:53:44.5596182Z [command]/usr/bin/git submodule foreach --recursive git config --local --name-only --get-regexp 'core\.sshCommand' && git config --local --unset-all 'core.sshCommand' || :
2022-05-18T11:53:44.6120326Z [command]/usr/bin/git config --local --name-only --get-regexp http\.https\:\/\/github\.com\/\.extraheader
2022-05-18T11:53:44.6121514Z [command]/usr/bin/git submodule foreach --recursive git config --local --name-only --get-regexp 'http\.https\:\/\/github\.com\/\.extraheader' && git config --local --unset-all 'http.https://github.com/.extraheader' || :
2022-05-18T11:53:44.6364834Z [command]/usr/bin/git config --local http.https://github.com/.extraheader AUTHORIZATION: basic ***
2022-05-18T11:53:44.6402556Z ##[endgroup]
2022-05-18T11:53:44.6403517Z ##[group]Fetching the repository
2022-05-18T11:53:44.6414052Z [command]/usr/bin/git -c protocol.version=2 fetch --prune --progress --no-recurse-submodules origin +refs/heads/*:refs/remotes/origin/* +refs/tags/*:refs/tags/* +5285dbcf23d71a148f58bffddae820c6d8506ca9:refs/remotes/pull/11/merge
2022-05-18T11:53:44.8541676Z remote: Enumerating objects: 78, done.        
2022-05-18T11:53:44.8542329Z remote: Counting objects:   1% (1/78)        
2022-05-18T11:53:44.8542932Z remote: Counting objects:   2% (2/78)        
2022-05-18T11:53:44.8543485Z remote: Counting objects:   3% (3/78)        
2022-05-18T11:53:44.8544404Z remote: Counting objects:   5% (4/78)        
2022-05-18T11:53:44.8545137Z remote: Counting objects:   6% (5/78)        
2022-05-18T11:53:44.8545827Z remote: Counting objects:   7% (6/78)        
2022-05-18T11:53:44.8546375Z remote: Counting objects:   8% (7/78)        
2022-05-18T11:53:44.8546884Z remote: Counting objects:  10% (8/78)        
2022-05-18T11:53:44.8547420Z remote: Counting objects:  11% (9/78)        
2022-05-18T11:53:44.8547963Z remote: Counting objects:  12% (10/78)        
2022-05-18T11:53:44.8548491Z remote: Counting objects:  14% (11/78)        
2022-05-18T11:53:44.8549029Z remote: Counting objects:  15% (12/78)        
2022-05-18T11:53:44.8549583Z remote: Counting objects:  16% (13/78)        
2022-05-18T11:53:44.8550102Z remote: Counting objects:  17% (14/78)        
2022-05-18T11:53:44.8550639Z remote: Counting objects:  19% (15/78)        
2022-05-18T11:53:44.8551183Z remote: Counting objects:  20% (16/78)        
2022-05-18T11:53:44.8551831Z remote: Counting objects:  21% (17/78)        
2022-05-18T11:53:44.8552351Z remote: Counting objects:  23% (18/78)        
2022-05-18T11:53:44.8552881Z remote: Counting objects:  24% (19/78)        
2022-05-18T11:53:44.8553417Z remote: Counting objects:  25% (20/78)        
2022-05-18T11:53:44.8553929Z remote: Counting objects:  26% (21/78)        
2022-05-18T11:53:44.8554458Z remote: Counting objects:  28% (22/78)        
2022-05-18T11:53:44.8554991Z remote: Counting objects:  29% (23/78)        
2022-05-18T11:53:44.8555496Z remote: Counting objects:  30% (24/78)        
2022-05-18T11:53:44.8556022Z remote: Counting objects:  32% (25/78)        
2022-05-18T11:53:44.8556560Z remote: Counting objects:  33% (26/78)        
2022-05-18T11:53:44.8557064Z remote: Counting objects:  34% (27/78)        
2022-05-18T11:53:44.8557592Z remote: Counting objects:  35% (28/78)        
2022-05-18T11:53:44.8558544Z remote: Counting objects:  37% (29/78)        
2022-05-18T11:53:44.8559075Z remote: Counting objects:  38% (30/78)        
2022-05-18T11:53:44.8559587Z remote: Counting objects:  39% (31/78)        
2022-05-18T11:53:44.8560119Z remote: Counting objects:  41% (32/78)        
2022-05-18T11:53:44.8560651Z remote: Counting objects:  42% (33/78)        
2022-05-18T11:53:44.8561162Z remote: Counting objects:  43% (34/78)        
2022-05-18T11:53:44.8561691Z remote: Counting objects:  44% (35/78)        
2022-05-18T11:53:44.8562219Z remote: Counting objects:  46% (36/78)        
2022-05-18T11:53:44.8562729Z remote: Counting objects:  47% (37/78)        
2022-05-18T11:53:44.8563253Z remote: Counting objects:  48% (38/78)        
2022-05-18T11:53:44.8563787Z remote: Counting objects:  50% (39/78)        
2022-05-18T11:53:44.8564312Z remote: Counting objects:  51% (40/78)        
2022-05-18T11:53:44.8564844Z remote: Counting objects:  52% (41/78)        
2022-05-18T11:53:44.8565371Z remote: Counting objects:  53% (42/78)        
2022-05-18T11:53:44.8565899Z remote: Counting objects:  55% (43/78)        
2022-05-18T11:53:44.8566805Z remote: Counting objects:  56% (44/78)        
2022-05-18T11:53:44.8567331Z remote: Counting objects:  57% (45/78)        
2022-05-18T11:53:44.8567862Z remote: Counting objects:  58% (46/78)        
2022-05-18T11:53:44.8568369Z remote: Counting objects:  60% (47/78)        
2022-05-18T11:53:44.8568893Z remote: Counting objects:  61% (48/78)        
2022-05-18T11:53:44.8569422Z remote: Counting objects:  62% (49/78)        
2022-05-18T11:53:44.8569927Z remote: Counting objects:  64% (50/78)        
2022-05-18T11:53:44.8570447Z remote: Counting objects:  65% (51/78)        
2022-05-18T11:53:44.8570975Z remote: Counting objects:  66% (52/78)        
2022-05-18T11:53:44.8571697Z remote: Counting objects:  67% (53/78)        
2022-05-18T11:53:44.8572223Z remote: Counting objects:  69% (54/78)        
2022-05-18T11:53:44.8572747Z remote: Counting objects:  70% (55/78)        
2022-05-18T11:53:44.8573282Z remote: Counting objects:  71% (56/78)        
2022-05-18T11:53:44.8573792Z remote: Counting objects:  73% (57/78)        
2022-05-18T11:53:44.8574321Z remote: Counting objects:  74% (58/78)        
2022-05-18T11:53:44.8574849Z remote: Counting objects:  75% (59/78)        
2022-05-18T11:53:44.8575357Z remote: Counting objects:  76% (60/78)        
2022-05-18T11:53:44.8575880Z remote: Counting objects:  78% (61/78)        
2022-05-18T11:53:44.8576401Z remote: Counting objects:  79% (62/78)        
2022-05-18T11:53:44.8576905Z remote: Counting objects:  80% (63/78)        
2022-05-18T11:53:44.8577685Z remote: Counting objects:  82% (64/78)        
2022-05-18T11:53:44.8578232Z remote: Counting objects:  83% (65/78)        
2022-05-18T11:53:44.8579127Z remote: Counting objects:  84% (66/78)        
2022-05-18T11:53:44.8579674Z remote: Counting objects:  85% (67/78)        
2022-05-18T11:53:44.8580185Z remote: Counting objects:  87% (68/78)        
2022-05-18T11:53:44.8580710Z remote: Counting objects:  88% (69/78)        
2022-05-18T11:53:44.8581243Z remote: Counting objects:  89% (70/78)        
2022-05-18T11:53:44.8581755Z remote: Counting objects:  91% (71/78)        
2022-05-18T11:53:44.8582279Z remote: Counting objects:  92% (72/78)        
2022-05-18T11:53:44.8582825Z remote: Counting objects:  93% (73/78)        
2022-05-18T11:53:44.8583125Z remote: Counting objects:  94% (74/78)        
2022-05-18T11:53:44.8583439Z remote: Counting objects:  96% (75/78)        
2022-05-18T11:53:44.8583754Z remote: Counting objects:  97% (76/78)        
2022-05-18T11:53:44.8584056Z remote: Counting objects:  98% (77/78)        
2022-05-18T11:53:44.8584368Z remote: Counting objects: 100% (78/78)        
2022-05-18T11:53:44.8584705Z remote: Counting objects: 100% (78/78), done.        
2022-05-18T11:53:44.8585071Z remote: Compressing objects:   2% (1/40)        
2022-05-18T11:53:44.8585408Z remote: Compressing objects:   5% (2/40)        
2022-05-18T11:53:44.8585749Z remote: Compressing objects:   7% (3/40)        
2022-05-18T11:53:44.8586370Z remote: Compressing objects:  10% (4/40)        
2022-05-18T11:53:44.8586697Z remote: Compressing objects:  12% (5/40)        
2022-05-18T11:53:44.8587036Z remote: Compressing objects:  15% (6/40)        
2022-05-18T11:53:44.8587376Z remote: Compressing objects:  17% (7/40)        
2022-05-18T11:53:44.8587697Z remote: Compressing objects:  20% (8/40)        
2022-05-18T11:53:44.8588028Z remote: Compressing objects:  22% (9/40)        
2022-05-18T11:53:44.8588372Z remote: Compressing objects:  25% (10/40)        
2022-05-18T11:53:44.8588703Z remote: Compressing objects:  27% (11/40)        
2022-05-18T11:53:44.8589044Z remote: Compressing objects:  30% (12/40)        
2022-05-18T11:53:44.8589381Z remote: Compressing objects:  32% (13/40)        
2022-05-18T11:53:44.8589998Z remote: Compressing objects:  35% (14/40)        
2022-05-18T11:53:44.8590483Z remote: Compressing objects:  37% (15/40)        
2022-05-18T11:53:44.8590839Z remote: Compressing objects:  40% (16/40)        
2022-05-18T11:53:44.8591185Z remote: Compressing objects:  42% (17/40)        
2022-05-18T11:53:44.8591506Z remote: Compressing objects:  45% (18/40)        
2022-05-18T11:53:44.8591840Z remote: Compressing objects:  47% (19/40)        
2022-05-18T11:53:44.8592178Z remote: Compressing objects:  50% (20/40)        
2022-05-18T11:53:44.8592493Z remote: Compressing objects:  52% (21/40)        
2022-05-18T11:53:44.8592822Z remote: Compressing objects:  55% (22/40)        
2022-05-18T11:53:44.8593154Z remote: Compressing objects:  57% (23/40)        
2022-05-18T11:53:44.8593485Z remote: Compressing objects:  60% (24/40)        
2022-05-18T11:53:44.8593808Z remote: Compressing objects:  62% (25/40)        
2022-05-18T11:53:44.8594140Z remote: Compressing objects:  65% (26/40)        
2022-05-18T11:53:44.8594582Z remote: Compressing objects:  67% (27/40)        
2022-05-18T11:53:44.8594909Z remote: Compressing objects:  70% (28/40)        
2022-05-18T11:53:44.8595241Z remote: Compressing objects:  72% (29/40)        
2022-05-18T11:53:44.8595574Z remote: Compressing objects:  75% (30/40)        
2022-05-18T11:53:44.8595894Z remote: Compressing objects:  77% (31/40)        
2022-05-18T11:53:44.8596227Z remote: Compressing objects:  80% (32/40)        
2022-05-18T11:53:44.8596557Z remote: Compressing objects:  82% (33/40)        
2022-05-18T11:53:44.8596877Z remote: Compressing objects:  85% (34/40)        
2022-05-18T11:53:44.8597210Z remote: Compressing objects:  87% (35/40)        
2022-05-18T11:53:44.8598855Z remote: Compressing objects:  90% (36/40)        
2022-05-18T11:53:44.8599203Z remote: Compressing objects:  92% (37/40)        
2022-05-18T11:53:44.8599523Z remote: Compressing objects:  95% (38/40)        
2022-05-18T11:53:44.8599854Z remote: Compressing objects:  97% (39/40)        
2022-05-18T11:53:44.8600193Z remote: Compressing objects: 100% (40/40)        
2022-05-18T11:53:44.8600529Z remote: Compressing objects: 100% (40/40), done.        
2022-05-18T11:53:44.8601254Z remote: Total 78 (delta 21), reused 68 (delta 17), pack-reused 0        
2022-05-18T11:53:44.8779272Z From https://github.com/varkevich93/Script.test
2022-05-18T11:53:44.8779942Z  * [new branch]      dev                                      -> origin/dev
2022-05-18T11:53:44.8780476Z  * [new branch]      features/do_one                          -> origin/features/do_one
2022-05-18T11:53:44.8784988Z  * [new branch]      hotfix/we_gonna_die                      -> origin/hotfix/we_gonna_die
2022-05-18T11:53:44.8792785Z  * [new branch]      master                                   -> origin/master
2022-05-18T11:53:44.8799567Z  * [new ref]         5285dbcf23d71a148f58bffddae820c6d8506ca9 -> pull/11/merge
2022-05-18T11:53:44.8839265Z ##[endgroup]
2022-05-18T11:53:44.8839836Z ##[group]Determining the checkout info
2022-05-18T11:53:44.8840804Z ##[endgroup]
2022-05-18T11:53:44.8841286Z ##[group]Checking out the ref
2022-05-18T11:53:44.8845541Z [command]/usr/bin/git checkout --progress --force refs/remotes/pull/11/merge
2022-05-18T11:53:44.8895768Z Note: switching to 'refs/remotes/pull/11/merge'.
2022-05-18T11:53:44.8896554Z 
2022-05-18T11:53:44.8898154Z You are in 'detached HEAD' state. You can look around, make experimental
2022-05-18T11:53:44.8899573Z changes and commit them, and you can discard any commits you make in this
2022-05-18T11:53:44.8900171Z state without impacting any branches by switching back to a branch.
2022-05-18T11:53:44.8900753Z 
2022-05-18T11:53:44.8901042Z If you want to create a new branch to retain commits you create, you may
2022-05-18T11:53:44.8901645Z do so (now or later) by using -c with the switch command. Example:
2022-05-18T11:53:44.8901884Z 
2022-05-18T11:53:44.8902255Z   git switch -c <new-branch-name>
2022-05-18T11:53:44.8902565Z 
2022-05-18T11:53:44.8902822Z Or undo this operation with:
2022-05-18T11:53:44.8903008Z 
2022-05-18T11:53:44.8903113Z   git switch -
2022-05-18T11:53:44.8903272Z 
2022-05-18T11:53:44.8903615Z Turn off this advice by setting config variable advice.detachedHead to false
2022-05-18T11:53:44.8903993Z 
2022-05-18T11:53:44.8904399Z HEAD is now at 5285dbc Merge 1785353ea37fa7192de6bcd73b2987153dff85e2 into 1129cc9a78ce5477b18e8d8c24a90585d54eb66f
2022-05-18T11:53:44.8909902Z ##[endgroup]
2022-05-18T11:53:44.8966413Z [command]/usr/bin/git log -1 --format='%H'
2022-05-18T11:53:44.9003335Z '5285dbcf23d71a148f58bffddae820c6d8506ca9'
2022-05-18T11:53:44.9467105Z ##[group]Run tj-actions/changed-files@v19
2022-05-18T11:53:44.9467602Z with:
2022-05-18T11:53:44.9468185Z   token: ***
2022-05-18T11:53:44.9468515Z   separator:  
2022-05-18T11:53:44.9468802Z   files_separator: 

2022-05-18T11:53:44.9469206Z   files_ignore_separator: 

2022-05-18T11:53:44.9469626Z   sha: 5285dbcf23d71a148f58bffddae820c6d8506ca9
2022-05-18T11:53:44.9469977Z   since_last_remote_commit: false
2022-05-18T11:53:44.9470353Z   use_fork_point: false
2022-05-18T11:53:44.9470705Z   quotepath: true
2022-05-18T11:53:44.9471012Z ##[endgroup]
2022-05-18T11:53:44.9833880Z ##[group]Run # "Set base sha..."
2022-05-18T11:53:44.9834361Z ;1m# "Set base sha..."
2022-05-18T11:53:44.9834693Z ;1mif [[ -n "" ]]; then
2022-05-18T11:53:44.9835176Z ;1m  echo "::set-output name=base_sha::"
2022-05-18T11:53:44.9835628Z ;1melif [[ "false" == "true" && "" != "0000000000000000000000000000000000000000" ]]; then
2022-05-18T11:53:44.9836136Z ;1m    echo "::set-output name=base_sha::"
2022-05-18T11:53:44.9836499Z ;1mfi
2022-05-18T11:53:44.9901275Z shell: /usr/bin/bash --noprofile --norc -e -o pipefail {0}
2022-05-18T11:53:44.9901758Z ##[endgroup]
2022-05-18T11:53:45.0320656Z ##[group]Run # "Calculating the previous and current SHA..."
2022-05-18T11:53:45.0321097Z ;1m# "Calculating the previous and current SHA..."
2022-05-18T11:53:45.0321468Z ;1mbash $GITHUB_ACTION_PATH/diff-sha.sh
2022-05-18T11:53:45.0379357Z shell: /usr/bin/bash --noprofile --norc -e -o pipefail {0}
2022-05-18T11:53:45.0379706Z env:
2022-05-18T11:53:45.0379985Z   GITHUB_SERVER_URL: https://github.com
2022-05-18T11:53:45.0380328Z   GITHUB_REPOSITORY: varkevich93/Script.test
2022-05-18T11:53:45.0380649Z   GITHUB_BASE_REF: master
2022-05-18T11:53:45.0380902Z   GITHUB_HEAD_REF: dev
2022-05-18T11:53:45.0381267Z   GITHUB_ACTION_PATH: /home/runner/work/_actions/tj-actions/changed-files/v19
2022-05-18T11:53:45.0381696Z   INPUT_SHA: 5285dbcf23d71a148f58bffddae820c6d8506ca9
2022-05-18T11:53:45.0382006Z   INPUT_BASE_SHA: 
2022-05-18T11:53:45.0382540Z   INPUT_TOKEN: ***
2022-05-18T11:53:45.0382791Z   INPUT_PATH: 
2022-05-18T11:53:45.0383056Z   INPUT_USE_FORK_POINT: false
2022-05-18T11:53:45.0383313Z ##[endgroup]
2022-05-18T11:53:45.0511767Z ##[group]changed-files-diff-sha
2022-05-18T11:53:45.0512124Z Resolving repository path...
2022-05-18T11:53:45.0543328Z Setting up 'temp_changed_files' remote...
2022-05-18T11:53:45.0589737Z No 'temp_changed_files' remote found
2022-05-18T11:53:45.0590567Z Creating 'temp_changed_files' remote...
2022-05-18T11:53:45.0629298Z Getting HEAD SHA...
2022-05-18T11:53:45.2788670Z remote: Total 0 (delta 0), reused 0 (delta 0), pack-reused 0        
2022-05-18T11:53:45.2848906Z From https://github.com/varkevich93/Script.test
2022-05-18T11:53:45.2850156Z  * [new branch]      master     -> master
2022-05-18T11:53:45.2850694Z  * [new branch]      master     -> temp_changed_files/master
2022-05-18T11:53:45.2898133Z Verifying commit SHA...
2022-05-18T11:53:45.2949750Z ##[endgroup]
2022-05-18T11:53:45.3005970Z ##[group]Run tj-actions/glob@v7.16
2022-05-18T11:53:45.3006254Z with:
2022-05-18T11:53:45.3006502Z   files-separator: 

2022-05-18T11:53:45.3006777Z   escape-paths: true
2022-05-18T11:53:45.3007064Z   excluded-files-separator: 

2022-05-18T11:53:45.3007416Z   base-sha: 1129cc9a78ce5477b18e8d8c24a90585d54eb66f
2022-05-18T11:53:45.3007781Z   sha: 5285dbcf23d71a148f58bffddae820c6d8506ca9
2022-05-18T11:53:45.3008102Z   include-deleted-files: true
2022-05-18T11:53:45.3008388Z   separator: |
2022-05-18T11:53:45.3008697Z   files-from-source-file-separator: 

2022-05-18T11:53:45.3009092Z   excluded-files-from-source-file-separator: 

2022-05-18T11:53:45.3009475Z   follow-symbolic-links: true
2022-05-18T11:53:45.3009778Z   strip-top-level-dir: true
2022-05-18T11:53:45.3010043Z ##[endgroup]
2022-05-18T11:53:45.5302469Z [command]/usr/bin/git rev-parse --show-toplevel
2022-05-18T11:53:45.5358542Z /home/runner/work/Script.test/Script.test
2022-05-18T11:53:45.5398283Z [command]/usr/bin/git diff --diff-filter=D --name-only 1129cc9a78ce5477b18e8d8c24a90585d54eb66f 5285dbcf23d71a148f58bffddae820c6d8506ca9
2022-05-18T11:53:45.5445181Z 
2022-05-18T11:53:45.5519437Z ##[group]Run bash $GITHUB_ACTION_PATH/entrypoint.sh
2022-05-18T11:53:45.5519845Z ;1mbash $GITHUB_ACTION_PATH/entrypoint.sh
2022-05-18T11:53:45.5578438Z shell: /usr/bin/bash --noprofile --norc -e -o pipefail {0}
2022-05-18T11:53:45.5578770Z env:
2022-05-18T11:53:45.5579099Z   GITHUB_ACTION_PATH: /home/runner/work/_actions/tj-actions/changed-files/v19
2022-05-18T11:53:45.5579481Z   INPUT_FILES_PATTERN_FILE: 
2022-05-18T11:53:45.5579769Z   INPUT_SEPARATOR:  
2022-05-18T11:53:45.5580012Z   INPUT_PATH: 
2022-05-18T11:53:45.5580356Z   INPUT_PREVIOUS_SHA: 1129cc9a78ce5477b18e8d8c24a90585d54eb66f
2022-05-18T11:53:45.5580761Z   INPUT_CURRENT_SHA: 5285dbcf23d71a148f58bffddae820c6d8506ca9
2022-05-18T11:53:45.5581092Z   INPUT_TARGET_BRANCH: master
2022-05-18T11:53:45.5581378Z   INPUT_CURRENT_BRANCH: dev
2022-05-18T11:53:45.5581672Z   INPUT_QUOTEPATH: true
2022-05-18T11:53:45.5581922Z ##[endgroup]
2022-05-18T11:53:45.5710298Z ##[group]changed-files
2022-05-18T11:53:45.5710655Z Resolving repository path...
2022-05-18T11:53:45.5713682Z Retrieving changes between 1129cc9a78ce5477b18e8d8c24a90585d54eb66f (master) → 5285dbcf23d71a148f58bffddae820c6d8506ca9 (dev)
2022-05-18T11:53:45.5714129Z Getting diff...
2022-05-18T11:53:45.9209187Z Added files: 
2022-05-18T11:53:45.9210118Z Copied files: 
2022-05-18T11:53:45.9213547Z Deleted files: 
2022-05-18T11:53:45.9214131Z Modified files: Pisun.txt
2022-05-18T11:53:45.9214878Z Renamed files: 
2022-05-18T11:53:45.9215310Z Type Changed files: 
2022-05-18T11:53:45.9215608Z Unmerged files: 
2022-05-18T11:53:45.9215844Z Unknown files: 
2022-05-18T11:53:45.9216151Z All changed and modified files: Pisun.txt
2022-05-18T11:53:45.9216469Z All changed files: Pisun.txt
2022-05-18T11:53:45.9216765Z All modified files: Pisun.txt
2022-05-18T11:53:45.9221819Z ##[endgroup]
2022-05-18T11:53:45.9363428Z ##[group]Run for file in Pisun.txt; do
2022-05-18T11:53:45.9363802Z ;1mfor file in Pisun.txt; do
2022-05-18T11:53:45.9364060Z ;1m
2022-05-18T11:53:45.9364360Z ;1m  echo "$file was changed" >> mod_files.log 2>&1
2022-05-18T11:53:45.9364653Z ;1m
2022-05-18T11:53:45.9365023Z ;1m  echo "Count Tab in files: `awk '{print gsub(/\t/,"")}' $file | awk '{s+=$1} END { print s }'`" >> mod_files.log 2>&1
2022-05-18T11:53:45.9365402Z ;1mdone
2022-05-18T11:53:45.9425683Z shell: /usr/bin/bash -e {0}
2022-05-18T11:53:45.9425989Z ##[endgroup]
2022-05-18T11:53:45.9577809Z ##[group]Run actions/upload-artifact@v2
2022-05-18T11:53:45.9578111Z with:
2022-05-18T11:53:45.9578486Z   path: mod_files.log
2022-05-18T11:53:45.9578742Z   name: artifact
2022-05-18T11:53:45.9578995Z   if-no-files-found: warn
2022-05-18T11:53:45.9579264Z ##[endgroup]
2022-05-18T11:53:46.0261697Z With the provided path, there will be 1 file uploaded
2022-05-18T11:53:46.0264655Z Starting artifact upload
2022-05-18T11:53:46.0265963Z For more detailed logs during the artifact upload process, enable step-debugging: https://docs.github.com/actions/monitoring-and-troubleshooting-workflows/enabling-debug-logging#enabling-step-debug-logging
2022-05-18T11:53:46.0267117Z Artifact name is valid!
2022-05-18T11:53:46.1050596Z Container for artifact "artifact" successfully created. Starting upload of file(s)
2022-05-18T11:53:46.1901152Z Total size of all the files uploaded is 44 bytes
2022-05-18T11:53:46.1931146Z File upload process has finished. Finalizing the artifact upload
2022-05-18T11:53:46.2223248Z Artifact has been finalized. All files have been successfully uploaded!
2022-05-18T11:53:46.2223742Z 
2022-05-18T11:53:46.2224112Z The raw size of all the files that were specified for upload is 44 bytes
2022-05-18T11:53:46.2225052Z The size of all the files that were uploaded is 44 bytes. This takes into account any gzip compression used to reduce the upload size, time and storage
2022-05-18T11:53:46.2225646Z 
2022-05-18T11:53:46.2226891Z Note: The size of downloaded zips can differ significantly from the reported size. For more information see: https://github.com/actions/upload-artifact#zipped-artifact-downloads 
2022-05-18T11:53:46.2227635Z 
2022-05-18T11:53:46.2227918Z Artifact artifact has been successfully uploaded!
2022-05-18T11:53:46.2450365Z Post job cleanup.
2022-05-18T11:53:46.2499037Z Post job cleanup.
2022-05-18T11:53:46.3173431Z Post job cleanup.
2022-05-18T11:53:46.4751460Z [command]/usr/bin/git version
2022-05-18T11:53:46.4822639Z git version 2.36.1
2022-05-18T11:53:46.4880004Z Copying '/home/runner/.gitconfig' to '/home/runner/work/_temp/414e3bc5-4f43-4b0b-808d-61eb0e05f4ce/.gitconfig'
2022-05-18T11:53:46.4895346Z Temporarily overriding HOME='/home/runner/work/_temp/414e3bc5-4f43-4b0b-808d-61eb0e05f4ce' before making global git config changes
2022-05-18T11:53:46.4897793Z Adding repository directory to the temporary git global config as a safe directory
2022-05-18T11:53:46.4905492Z [command]/usr/bin/git config --global --add safe.directory /home/runner/work/Script.test/Script.test
2022-05-18T11:53:46.4953547Z [command]/usr/bin/git config --local --name-only --get-regexp core\.sshCommand
2022-05-18T11:53:46.4996414Z [command]/usr/bin/git submodule foreach --recursive git config --local --name-only --get-regexp 'core\.sshCommand' && git config --local --unset-all 'core.sshCommand' || :
2022-05-18T11:53:46.5275264Z [command]/usr/bin/git config --local --name-only --get-regexp http\.https\:\/\/github\.com\/\.extraheader
2022-05-18T11:53:46.5297125Z http.https://github.com/.extraheader
2022-05-18T11:53:46.5310048Z [command]/usr/bin/git config --local --unset-all http.https://github.com/.extraheader
2022-05-18T11:53:46.5351350Z [command]/usr/bin/git submodule foreach --recursive git config --local --name-only --get-regexp 'http\.https\:\/\/github\.com\/\.extraheader' && git config --local --unset-all 'http.https://github.com/.extraheader' || :
2022-05-18T11:53:46.5879791Z Cleaning up orphan processes
```
