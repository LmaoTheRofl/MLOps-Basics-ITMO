git status
git switch -c modify
git switch -c feature/first-test-func modify
git add .
git commit -m "feat: add first test function"
git push -u origin feature/first-test-func

git status
git switch -c feature/second-test-func modify
git add .
git commit -m "feat: add second test function"
git push -u origin feature/second-test-func

git switch -c release/first-update modify
git add HW_2/README.md
git commit -m "release: update README"
git switch main
git merge --no-ff release/first-update

git switch modify
git merge --no-ff release/first-update

git branch -d release/first-update

git push origin main
git push origin modify