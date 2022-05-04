
<h1 134  cd c: </h1>
  135  cd Users/VALERA/Documents/
  136  mk dir 01.HomeWorkLab
  137  mkdir 01.HomeWorkLab
  138  cd 01.HomeWorkLab/
  139  git init
  140  git config user.name 'v.markevich'
  141  git config user.email 'mv@fn.by'
  142  nano Pisun.txt
  143  git add --all
  144  git status
  145  git commit -m 'First Pisun'
  146  echo podsgsdgf >> Pisun.txt
  147  git add .
  148  git commit -m 'Second Change Pisun'
  149  git checkout -b dev
  150  touch piska-sosiska.conf
  151  git add .
  152  git commit -m 'Create file piska-sosiska'
  153  echo gondon >> piska-sosiska.conf
  154  git add .
  155  git commit -m 'Modified piska'
  156  git branch -b features/do_one
  157  git branch -b 'features/do_one'
  158  git checkout -b 'features/do_one'
  159  touch mama
  160  git add .
  161  git commit -m 'features'
  162  echo gfdgf >> mama
  163  git add .
  164  git commit -m 'pampers'
  165  git log
  166  git log --oneline
  167  git reset --hard HEAD~1
  168  git log --oneline
  169  git branch master
  170  git checkout master
  171  git checkout -b hotfix/we_gonna_die
  172  touch 777
  173  git add .
  174  git commit -m '777'
  175  git checkout master
  176  git merge features/do_one
  177  git log --oneline
  178  git checkout hotfix/we_gonna_die
  179  git log --oneline
  180  git checkout master
  181  git cherry-pick 38c2c57
  182  git log
  183  git checkout dev
  184  git cherry-pick 38c2c57
  185  git checkout features/do_one
  186  git cherry-pick 38c2c57
  187  history
</h1>

