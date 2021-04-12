# si_2021_lab1_-171250-
Лабараториска вежба 1
Никита Кечовски Индекс:171250
Прв чекор креирам GitHub :https://github.com/NikitaKechovski/si_2021_lab1_-171250-
На самата страна на GitHub креирам оддалечен репозотириум.
Преку GitBash со командата$ git init si_2021_lab1_[171250] иницијализирам празен локален репозиториум.
Со командите $ git remote add origin https://github.com/NikitaKechovski/si_2021_lab1_-171250-.git   $ git push --set-upstream origin master ги спојувам мојот локален репозиториум со оддалечениот репозиториум, и воедно податоците од локалниот прават upload на remote репозиториум.
Прво пристапувам до податокот (односно го ставам на сцена)$ git add numbers.txt, а потоа правам snapshot од моменталните промени  $git commit –m “Add numbers from 1-5”
Се повторува истиот принцип за следните три commits.
$ git add numbers.txt  $git commit –m “Add numbers from 6-9”
$ git add numbers.txt  $git commit –m “Add some words
Бидејќи сакаме да го промениме последниот commit ја користиме командата $ git reset -- hard HEAD^ , што прави undo на последниот commit и на сите промени.
Ги синхронизираме двата репозиториуми $ git push --set-upstream origin master.
За да можеме да креираме две нови гранки ја користиме командата $ git branch “branch1”  $ git branch “branch2”
Со користење на командата $ git checkout branch1 се префрлуваме на првата гранка.
На таа гранка креираме .txt file и  со следните командите пристапуваме до податокот и сооедветно правиме commit $git add words.txt $ git commit –m “ Add 5 words”.
Со оваа команда ние всушност не правиме нов commit, едноставно го менуваме само стариот $git  commit – amend –m “Add 6 words”, со тоа што све додале уште еден збор во txt фаилот и затоа го менуваме името на комитот
Се префрлуваме на гранката branch2 so командата $ git checkout branch2.
Додаваме зборови во датотеката numbers , и ги поставуваме нашите промени $ git add numbers.txt  $git commit –m “Add numbers from 10-15”
При овој чекор го дава следниот проблем:
$ git push
To https://github.com/NikitaKechovski/si_2021_lab1_-171250-.git
 ! [rejected]        branch1 -> branch1 (non-fast-forward)
error: failed to push some refs to 'https://github.com/NikitaKechovski/si_2021_lab1_-171250-.git'
hint: Updates were rejected because the tip of your current branch is behind
hint: its remote counterpart. Integrate the remote changes (e.g.
hint: 'git pull ...') before pushing again.
hint: See the 'Note about fast-forwards' in 'git push --help' for details.


Во продолжение се досегашните логови:
$ git log
commit 4c868b3f9a3c365cdfd7f29029f151f166ad466c (HEAD -> branch1)
Author: NikitaKechovski <81694941+NikitaKechovski@users.noreply.github.com>
Date:   Mon Apr 12 22:58:14 2021 +0200

    Add 6 words

commit ef645a25c94eeccc404c60167fc6fd6eca58ba2f (master, branch2)
Author: NikitaKechovski <81694941+NikitaKechovski@users.noreply.github.com>
Date:   Mon Apr 12 22:42:08 2021 +0200

    Add some words

commit 2a96191761b8cffbfe9d62ed2acaee3ede4144c6
Author: NikitaKechovski <81694941+NikitaKechovski@users.noreply.github.com>
Date:   Mon Apr 12 22:41:30 2021 +0200

    Add numbers from 6-9

commit 86215888fe87301445663c79f7707e9086041056 (origin/master)
Author: NikitaKechovski <81694941+NikitaKechovski@users.noreply.github.com>
Date:   Mon Apr 12 22:27:34 2021 +0200

    Add some words

commit 996be175474a635e8c366a89eb4fe7f827722267
Author: NikitaKechovski <81694941+NikitaKechovski@users.noreply.github.com>
Date:   Mon Apr 12 22:26:08 2021 +0200

    Add numbers from 6-9

commit 2445edebcd06d50c982eb85b71d68e645b5361d2
Author: NikitaKechovski <81694941+NikitaKechovski@users.noreply.github.com>
Date:   Mon Apr 12 22:23:41 2021 +0200

:...skipping...
commit 4c868b3f9a3c365cdfd7f29029f151f166ad466c (HEAD -> branch1)
Author: NikitaKechovski <81694941+NikitaKechovski@users.noreply.github.com>
Date:   Mon Apr 12 22:58:14 2021 +0200

    Add 6 words

commit ef645a25c94eeccc404c60167fc6fd6eca58ba2f (master, branch2)
Author: NikitaKechovski <81694941+NikitaKechovski@users.noreply.github.com>
Date:   Mon Apr 12 22:42:08 2021 +0200

    Add some words

commit 2a96191761b8cffbfe9d62ed2acaee3ede4144c6
Author: NikitaKechovski <81694941+NikitaKechovski@users.noreply.github.com>
Date:   Mon Apr 12 22:41:30 2021 +0200

    Add numbers from 6-9

commit 86215888fe87301445663c79f7707e9086041056 (origin/master)
Author: NikitaKechovski <81694941+NikitaKechovski@users.noreply.github.com>
Date:   Mon Apr 12 22:27:34 2021 +0200

    Add some words

commit 996be175474a635e8c366a89eb4fe7f827722267
Author: NikitaKechovski <81694941+NikitaKechovski@users.noreply.github.com>
Date:   Mon Apr 12 22:26:08 2021 +0200

    Add numbers from 6-9

commit 2445edebcd06d50c982eb85b71d68e645b5361d2
Author: NikitaKechovski <81694941+NikitaKechovski@users.noreply.github.com>
Date:   Mon Apr 12 22:23:41 2021 +0200

    Add numbers from 1-5
