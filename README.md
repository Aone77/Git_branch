1. На локальном репозитории сделать ветки для:
- Postman - `git branch Postman`
- Jmeter - `git branch Jmeter`
- CheckLists - `git branch CheckLists`
- Bug Reports - `git branch Bug_Reports`
- SQL - `git branch SQL`
- Charles - `git branch Charles`
- Mobile testing - `git branch Mobile_testing`
- или `git branch Postman ; git branch Jmeter ; git branch CheckLists ; git branch Bug_Reports ; git branch SQL ; git branch Charles ; git branch Mobile_testing`

2. Запушить все ветки на внешний репозиторий - `git push -u origin --all`
3. В ветке Bug Reports сделать текстовый документ со структурой баг репорта - 
`git checkout Bug_Reports ; cat > bug_report_1.txt`
	+ ID
	+ Environment
	+ Priority
	+ Severity
	+ Title
	+ Module
	+ Precondition
	+ Steps_to_reproduce
	+ Expected_result
	+ Actual_result
`Enter` `CTRL+D`

5. Запушить структуру багрепорта на внешний репозиторий - `git add . ; git commit -m "add bug_report_1.txt" ; git push`
6. Вмержить ветку Bug Reports в Main - `git checkout main ; git merge Bug_Reports`
7. Запушить main на внешний репозиторий - `git add . ; git commit -m "merge Bug report to master" ; git push`

9. В ветке CheckLists набросать структуру чек листа - 
`git checkout CheckLists ; cat > checklist_web.txt`
	+ ID
	+ Title
	+ Precondition
	+ Module
	+ Steps_to_reproduce
	+ Expected_result
	+ Status
`Enter` `CTRL+D`

10. Запушить структуру на внешний репозиторий - ` git add . ; git commit -m "add checklist_web.txt" ; git push` (если выдает ошибку, выполнить команду git push -u origin "Checklists")
12. На внешнем репозитории сделать Pull Request ветки CheckLists в main - Перейти на веб версию github в нужный репозиторий, изменить ветку на Checklists, нажать `Pull Request`
13. Синхронизировать Внешнюю и Локальную ветки Main - `git checkout main ; git pull`
