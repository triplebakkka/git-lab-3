## Варіант          журнал, варіант, прізвище
38; 8; Shukailo.
## 1. stash list    рядок із вашим -m
stash@{0}: On lab3/variant-8-shukailo: повідомлення з таблиці А
## 2. cherry-pick   два хеші і чому вони різні
0e15603; 10840cf; 
Тому що функція «cherry-pick» не просто переміщує або копіює вихідний об’єкт коміту, а створює абсолютно новий коміт у  поточній гілці.
## 3. reflog        два рядки до і після amend
1401541 (tag: v0.1-shukailo, recover/v8) HEAD@{20}: revert: Revert "Зіпсувати рядок"
7a4985a HEAD@{21}: commit: Зіпсувати рядок
7112415 HEAD@{22}: commit (amend): Уточнити пошту групи, варіант 8
e01ad66 HEAD@{23}: cherry-pick: Замінити пошту групи повторно
10840cf HEAD@{24}: checkout: moving from feature/pick-8 to lab3/variant-8-shukailo
## 4. revert        log --oneline, видно обидва коміти
d842364 WIP:чернетка
a46afb4 deleted notes and replaced with new notes file
1401541 (tag: v0.1-shukailo, recover/v8) Revert "Зіпсувати рядок"
7a4985a Зіпсувати рядок
## 5. тег           фрагмент git show: tag, Tagger, повідомлення
Date:   Sun Oct 25 20:00:36 2026 +0200

    changed notes file

diff --git a/NOTES-l3.md b/NOTES-l3.md
new file mode 100644
index 0000000..95efac2
--- /dev/null
+++ b/NOTES-l3.md
@@ -0,0 +1,5 @@
+blame
+origin
+upstream
+fetch upstream
+push
## 6. rebase -i     pick / squash і підсумкове повідомлення
c826a5b (HEAD -> lab3/variant-8-shukailo, origin/lab3/variant-8-shukailo) HEAD@{4}: rebase (star
t): checkout refs/remotes/origin/lab3/variant-8-shukailo
c826a5b (HEAD -> lab3/variant-8-shukailo, origin/lab3/variant-8-shukailo) HEAD@{5}: commit: chan
ged notes file
2c14814 HEAD@{6}: rebase (finish): returning to refs/heads/lab3/variant-8-shukailo
2c14814 HEAD@{7}: rebase (squash): changed config file
976ffc5 HEAD@{8}: rebase (pick): changed config file
6d5a23e HEAD@{9}: rebase (squash): fix typo
19c57de HEAD@{10}: rebase (pick): fix typo
d842364 HEAD@{11}: rebase (pick): WIP:чернетка
## 7. blame         один рядок
 git blame -L 1,5 CONTACT.md
10840cf7 (dimas 2026-10-25 17:16:26 +0200 1) # Головна
14015417 (dimas 2026-10-25 17:37:29 +0200 2) Уточнення варіанта 8
6d5a23eb (dimas 2026-10-25 19:21:44 +0200 3) nobody2@invalid
## 8. fork          origin, upstream, куди push і куди PR
origin це  особистий форк (fork) або копія основного репозиторію на GitHub
upstream це основний репозиторій, від якого зробили форк 
PR створюється з вашого репозиторію (origin) у головний репозиторій 
 push робиться у свій репозиторій — origin