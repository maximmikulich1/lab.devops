<p> 
  https://github.com/varkevich93/Script.test <br>
  https://git.fn.by/v.markevich/devops.lab <br>
Create Script to .git/hooks/post-commit <br>
chmod +x post-commit <br>
</p>
<p>
#!bin/bash <br>
git push -u gitlab --all <br>
git push -u githubssh --all <br>

</p>
