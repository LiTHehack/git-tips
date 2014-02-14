#Git-tips
Här har vi samlat ett gäng bra Git-kommandon som kan hjälpa dig komma igång med Git.

Vi vill också passa på att höja ett varningens finger för att använda grafiska gränssnitt för Git. Risken för att det blir fel och för att framförallt merge-konfilkter krånglar blir då mycket större. Vårt tips är därför att du lär dig dessa kommandon och kanske lägger lite tid på det.

##Kommandon

Se till att starta ett nytt respository

    // börja ett nytt repository
    $ git init

Eller kopiera ett befintligt från exempelvis github eller ett lokalt repository

    // kopiera ett befintligt repository
    $ git clone [..]

Fyll det med filer manuellt och sedan tracka dem genom att lägga till dem

    // lägg till eller ta bort fil från repositoryt
	$ git add sokvag/till/fil.txt
	$ git rm tar/bort/fil.txt

För att se förändringar sedan senaste commit eller status för repositoryt

    // visa status, commits och grafiskt
	$ git status
	$ git log
	$ git log --graph
	$ gitk

Bekräfta ändringar för att ge filerna en hållpunkt

    // bekräfta ändringar
	$ git commit -m "message"
	// om fil missats vid commiten kan den läggad till i efterhand
	$ git add [..]
	$ git commit --amend

Branches är praktiskt vid test av nya experimentella funktioner då inte

    // skapa en ny branch, lista branches och sedan checka ut
	$ git branch namn-pa-branch
	$ git branch -a
	$ git checkout namn-pa-branch
	// ovanstående kortkommando
	$ git branch -b namn-pa-branch

Hämta tillbaka gammal commit eller fil

    // Hämta fil från commit
	$ git checkout [commit-id]^ -- [..]
	// hämta en hel commit
	$ git checkout [commit-id]
	// slå ihop med annan commit
	git merge [commit-id]

## Lär dig mer
Det vi tar upp här är mycket, men långt ifrån allt. Därför har vi samlat några bra länkar här, där du kan lära dig mer:
* Mer om branches: http://pcottle.github.io/learnGitBranching/
* En bra interaktiv Git-tutorial: http://try.github.io/
* Branching-modellen vi visade på Git-föreläsningen: http://nvie.com/posts/a-successful-git-branching-model/
* Koppla Git med GitHub: https://help.github.com/articles/set-up-git
