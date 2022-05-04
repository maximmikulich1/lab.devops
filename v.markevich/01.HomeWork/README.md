<p> 
  134  cd c: <br>
  135  cd Users/VALERA/Documents/ <br>
  136  mk dir 01.HomeWorkLab <br>
  137  mkdir 01.HomeWorkLab <br>
  138  cd 01.HomeWorkLab/<br>
  139  git init<br>
  140  git config user.name 'v.markevich'<br>
  141  git config user.email 'mv@fn.by'<br>
  142  nano Pisun.txt<br>
  143  git add --all<br>
  144  git status<br>
  145  git commit -m 'First Pisun'<br>
  146  echo podsgsdgf >> Pisun.txt<br>
  147  git add .<br>
  148  git commit -m 'Second Change Pisun'<br>
  149  git checkout -b dev<br>
  150  touch piska-sosiska.conf<br>
  151  git add .<br>
  152  git commit -m 'Create file piska-sosiska'<br>
  153  echo gondon >> piska-sosiska.conf<br>
  154  git add .<br>
  155  git commit -m 'Modified piska'<br>
  156  git branch -b features/do_one<br>
  157  git branch -b 'features/do_one'<br>
  158  git checkout -b 'features/do_one'<br>
  159  touch mama<br>
  160  git add .<br>
  161  git commit -m 'features'<br>
  162  echo gfdgf >> mama<br>
  163  git add .<br>
  164  git commit -m 'pampers'<br>
  165  git log<br>
  166  git log --oneline<br>
  167  git reset --hard HEAD~1<br>
  168  git log --oneline<br>
  169  git branch master<br>
  170  git checkout master<br>
  171  git checkout -b hotfix/we_gonna_die<br>
  172  touch 777<br>
  173  git add .<br>
  174  git commit -m '777'<br>
  175  git checkout master<br>
  176  git merge features/do_one<br>
  177  git log --oneline<br>
  178  git checkout hotfix/we_gonna_die<br>
  179  git log --oneline<br>
  180  git checkout master<br>
  181  git cherry-pick 38c2c57<br>
  182  git log<br>
  183  git checkout dev<br>
  184  git cherry-pick 38c2c57<br>
  185  git checkout features/do_one<br>
  186  git cherry-pick 38c2c57<br>
  187  history<br>
</p>
