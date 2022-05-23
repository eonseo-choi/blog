---
layout: post
title:  "22-05-20 git pull의 중요성"
date:   2022-05-22 11:15:54 +0900
categories: jekyll update
---

login as: eschoi
eschoi@10.21.8.152's password:
Welcome to Ubuntu 18.04.5 LTS (GNU/Linux 5.4.0-109-generic x86_64)

 * Documentation:  https://help.ubuntu.com
 * Management:     https://landscape.canonical.com
 * Support:        https://ubuntu.com/advantage

60 updates can be applied immediately.
4 of these updates are standard security updates.
To see these additional updates run: apt list --upgradable

New release '20.04.4 LTS' available.
Run 'do-release-upgrade' to upgrade to it.

Your Hardware Enablement Stack (HWE) is supported until April 2023.
*** System restart required ***
Last login: Wed May 18 13:36:40 2022 from 10.2.0.247
mkdeschoi@dna-db2:~$ mkdir ToyProject
eschoi@dna-db2:~$ cd ToyProject/
eschoi@dna-db2:~/ToyProject$ ls
eschoi@dna-db2:~/ToyProject$
eschoi@dna-db2:~/ToyProject$
eschoi@dna-db2:~/ToyProject$ git clone http://10.1.203.13:9090/toyproject/petcal                                                                         endar.git
Cloning into 'petcalendar'...
Username for 'http://10.1.203.13:9090': eschoi
Password for 'http://eschoi@10.1.203.13:9090':
remote: Enumerating objects: 49, done.
remote: Counting objects: 100% (49/49), done.
remote: Compressing objects: 100% (43/43), done.
remote: Total 49 (delta 3), reused 0 (delta 0), pack-reused 0
Unpacking objects: 100% (49/49), done.
eschoi@dna-db2:~/ToyProject$
eschoi@dna-db2:~/ToyProject$
eschoi@dna-db2:~/ToyProject$ ls
petcalendar
eschoi@dna-db2:~/ToyProject$
eschoi@dna-db2:~/ToyProject$
eschoi@dna-db2:~/ToyProject$ cd petcalendar/
eschoi@dna-db2:~/ToyProject/petcalendar$ ls
next.config.js  pages      server         tsconfig.server.json
next-env.d.ts   public     styles         yarn.lock
package.json    README.md  tsconfig.json
eschoi@dna-db2:~/ToyProject/petcalendar$
eschoi@dna-db2:~/ToyProject/petcalendar$
eschoi@dna-db2:~/ToyProject/petcalendar$ ls
next.config.js  pages      server         tsconfig.server.json
next-env.d.ts   public     styles         yarn.lock
package.json    README.md  tsconfig.json
eschoi@dna-db2:~/ToyProject/petcalendar$
eschoi@dna-db2:~/ToyProject/petcalendar$
eschoi@dna-db2:~/ToyProject/petcalendar$ vi README.md
eschoi@dna-db2:~/ToyProject/petcalendar$
eschoi@dna-db2:~/ToyProject/petcalendar$
eschoi@dna-db2:~/ToyProject/petcalendar$ git pull remote master
fatal: 'remote' does not appear to be a git repository
fatal: Could not read from remote repository.

Please make sure you have the correct access rights
and the repository exists.
eschoi@dna-db2:~/ToyProject/petcalendar$ git pull origin master
Username for 'http://10.1.203.13:9090': eschoi
Password for 'http://eschoi@10.1.203.13:9090':
remote: Enumerating objects: 12, done.
remote: Counting objects: 100% (10/10), done.
remote: Compressing objects: 100% (6/6), done.
remote: Total 6 (delta 4), reused 0 (delta 0), pack-reused 0
Unpacking objects: 100% (6/6), done.
From http://10.1.203.13:9090/toyproject/petcalendar
 * branch            master     -> FETCH_HEAD
   4f2968b..c376a0b  master     -> origin/master
Updating 4f2968b..c376a0b
Fast-forward
 pages/index.tsx | 68 +++++++--------------------------------------------------
 1 file changed, 8 insertions(+), 60 deletions(-)
eschoi@dna-db2:~/ToyProject/petcalendar$ git add .
eschoi@dna-db2:~/ToyProject/petcalendar$ git commit -m "수정수정"
[master d4b3228] 수정수정
 1 file changed, 1 insertion(+), 1 deletion(-)
eschoi@dna-db2:~/ToyProject/petcalendar$ git push
Username for 'http://10.1.203.13:9090': eschoi
Password for 'http://eschoi@10.1.203.13:9090':
Counting objects: 3, done.
Delta compression using up to 16 threads.
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 295 bytes | 295.00 KiB/s, done.
Total 3 (delta 2), reused 0 (delta 0)
To http://10.1.203.13:9090/toyproject/petcalendar.git
   c376a0b..d4b3228  master -> master
eschoi@dna-db2:~/ToyProject/petcalendar$ cd ../..
eschoi@dna-db2:~$ ls
 20220127-compare       DNA_DB_Tech-push               SSDRM                                     vcd-light
 DDT                    examples.desktop               test                                      vcd-light_backup
 dna-db_20220113        ex_pth                         ToyProject                                vcd_service
 DNA_DB_Tech            node                           tp1                                       vcd-work
 DNA_DB_Tech-202110     pconn_agent                    vcd-compare
 DNA_DB_Tech-20211108   Release-20220204_vcd-compare  'vcd-compare_backup(pyinstallerSuccess)'
 DNA-DB_Tech-light      Release_DDT                    vcd-detect-grpc
eschoi@dna-db2:~$ cd tp1/
eschoi@dna-db2:~/tp1$ git clone http://10.1.203.13:9090/eschoi/petcalendar.git
Cloning into 'petcalendar'...
Username for 'http://10.1.203.13:9090': eschoi
Password for 'http://eschoi@10.1.203.13:9090':
remote: Enumerating objects: 45, done.
remote: Counting objects: 100% (45/45), done.
remote: Compressing objects: 100% (39/39), done.
remote: Total 45 (delta 0), reused 45 (delta 0), pack-reused 0
Unpacking objects: 100% (45/45), done.
eschoi@dna-db2:~/tp1$
eschoi@dna-db2:~/tp1$
eschoi@dna-db2:~/tp1$ ls
petcalendar
eschoi@dna-db2:~/tp1$
eschoi@dna-db2:~/tp1$ cd petcalendar/
eschoi@dna-db2:~/tp1/petcalendar$ ls
next.config.js  package.json  public     server  tsconfig.json         yarn.lock
next-env.d.ts   pages         README.md  styles  tsconfig.server.json
eschoi@dna-db2:~/tp1/petcalendar$
eschoi@dna-db2:~/tp1/petcalendar$
eschoi@dna-db2:~/tp1/petcalendar$ vi README.md
eschoi@dna-db2:~/tp1/petcalendar$
eschoi@dna-db2:~/tp1/petcalendar$ git add .
eschoi@dna-db2:~/tp1/petcalendar$ git commit -m "리드미 수정(날짜추가)"
[master 0648094] 리드미 수정(날짜추가)
 1 file changed, 1 insertion(+)
eschoi@dna-db2:~/tp1/petcalendar$ git push
Username for 'http://10.1.203.13:9090': eschoi
Password for 'http://eschoi@10.1.203.13:9090':
Counting objects: 3, done.
Delta compression using up to 16 threads.
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 333 bytes | 333.00 KiB/s, done.
Total 3 (delta 2), reused 0 (delta 0)
To http://10.1.203.13:9090/eschoi/petcalendar.git
   de3ac52..0648094  master -> master
eschoi@dna-db2:~/tp1/petcalendar$ git fetch "git@10.1.203.13:eschoi/petcalendar.git" "master"
git@10.1.203.13's password:
Permission denied, please try again.
git@10.1.203.13's password:
Permission denied, please try again.
git@10.1.203.13's password:
git@10.1.203.13: Permission denied (publickey,password).
fatal: Could not read from remote repository.

Please make sure you have the correct access rights
and the repository exists.
eschoi@dna-db2:~/tp1/petcalendar$ git fetch "git@10.1.203.13:eschoi/petcalendar.git" "master"
git@10.1.203.13's password:

eschoi@dna-db2:~/tp1/petcalendar$
eschoi@dna-db2:~/tp1/petcalendar$
eschoi@dna-db2:~/tp1/petcalendar$
eschoi@dna-db2:~/tp1/petcalendar$ git fetch "git@10.1.203.13:eschoi/petcalendar.git" "master"
git@10.1.203.13's password:
Permission denied, please try again.
git@10.1.203.13's password:
Permission denied, please try again.
git@10.1.203.13's password:

eschoi@dna-db2:~/tp1/petcalendar$ ^C
eschoi@dna-db2:~/tp1/petcalendar$ git fetch "http://10.1.203.13:9090/eschoi/petcalendar.git" "master"
Username for 'http://10.1.203.13:9090': eschoi
Password for 'http://eschoi@10.1.203.13:9090':
remote: HTTP Basic: Access denied
fatal: Authentication failed for 'http://10.1.203.13:9090/eschoi/petcalendar.git/'
eschoi@dna-db2:~/tp1/petcalendar$ git pull
Username for 'http://10.1.203.13:9090': eschoi
Password for 'http://eschoi@10.1.203.13:9090':
Already up to date.
eschoi@dna-db2:~/tp1/petcalendar$
eschoi@dna-db2:~/tp1/petcalendar$
eschoi@dna-db2:~/tp1/petcalendar$ git pull origin master
Username for 'http://10.1.203.13:9090': eschoi
Password for 'http://eschoi@10.1.203.13:9090':
From http://10.1.203.13:9090/eschoi/petcalendar
 * branch            master     -> FETCH_HEAD
Already up to date.
eschoi@dna-db2:~/tp1/petcalendar$
eschoi@dna-db2:~/tp1/petcalendar$
eschoi@dna-db2:~/tp1/petcalendar$ ls
next.config.js  package.json  public     server  tsconfig.json         yarn.lock
next-env.d.ts   pages         README.md  styles  tsconfig.server.json
eschoi@dna-db2:~/tp1/petcalendar$ vi README.md
eschoi@dna-db2:~/tp1/petcalendar$
eschoi@dna-db2:~/tp1/petcalendar$
eschoi@dna-db2:~/tp1/petcalendar$ git remote -v
origin  http://10.1.203.13:9090/eschoi/petcalendar.git (fetch)
origin  http://10.1.203.13:9090/eschoi/petcalendar.git (push)
eschoi@dna-db2:~/tp1/petcalendar$
eschoi@dna-db2:~/tp1/petcalendar$ git remote add remote git@10.1.203.13:toyproject/petcalendar.git
eschoi@dna-db2:~/tp1/petcalendar$
eschoi@dna-db2:~/tp1/petcalendar$ git remote -v
origin  http://10.1.203.13:9090/eschoi/petcalendar.git (fetch)
origin  http://10.1.203.13:9090/eschoi/petcalendar.git (push)
remote  git@10.1.203.13:toyproject/petcalendar.git (fetch)
remote  git@10.1.203.13:toyproject/petcalendar.git (push)
eschoi@dna-db2:~/tp1/petcalendar$ git pull remote
git@10.1.203.13's password:
Permission denied, please try again.
git@10.1.203.13's password:
Permission denied, please try again.
git@10.1.203.13's password:

eschoi@dna-db2:~/tp1/petcalendar$
eschoi@dna-db2:~/tp1/petcalendar$
eschoi@dna-db2:~/tp1/petcalendar$ git pull remote origin
git@10.1.203.13's password:
Permission denied, please try again.
git@10.1.203.13's password:
Permission denied, please try again.
git@10.1.203.13's password:

eschoi@dna-db2:~/tp1/petcalendar$
eschoi@dna-db2:~/tp1/petcalendar$
eschoi@dna-db2:~/tp1/petcalendar$ git fetch
Username for 'http://10.1.203.13:9090': escho^C
eschoi@dna-db2:~/tp1/petcalendar$
eschoi@dna-db2:~/tp1/petcalendar$
eschoi@dna-db2:~/tp1/petcalendar$ git fetch remote
git@10.1.203.13's password:
Permission denied, please try again.
git@10.1.203.13's password:
Permission denied, please try again.
git@10.1.203.13's password:
git@10.1.203.13: Permission denied (publickey,password).
fatal: Could not read from remote repository.

Please make sure you have the correct access rights
and the repository exists.
eschoi@dna-db2:~/tp1/petcalendar$
eschoi@dna-db2:~/tp1/petcalendar$
eschoi@dna-db2:~/tp1/petcalendar$ git remote add remote http://10.1.203.13:9090/toyproject/petcalendar.git
fatal: remote remote already exists.
eschoi@dna-db2:~/tp1/petcalendar$ git remote rm remote
eschoi@dna-db2:~/tp1/petcalendar$ git remote add remote http://10.1.203.13:9090/toyproject/petcalendar.git
eschoi@dna-db2:~/tp1/petcalendar$ git pull remote
Username for 'http://10.1.203.13:9090': eschoi
Password for 'http://eschoi@10.1.203.13:9090':
remote: HTTP Basic: Access denied
fatal: Authentication failed for 'http://10.1.203.13:9090/toyproject/petcalendar.git/'
eschoi@dna-db2:~/tp1/petcalendar$ git pull remote
Username for 'http://10.1.203.13:9090': eschoi
Password for 'http://eschoi@10.1.203.13:9090':
remote: Enumerating objects: 19, done.
remote: Counting objects: 100% (19/19), done.
remote: Compressing objects: 100% (15/15), done.
remote: Total 15 (delta 10), reused 0 (delta 0), pack-reused 0
Unpacking objects: 100% (15/15), done.
From http://10.1.203.13:9090/toyproject/petcalendar
 * [new branch]      master     -> remote/master
You asked to pull from the remote 'remote', but did not specify
a branch. Because this is not the default configured remote
for your current branch, you must specify a branch on the command line.
eschoi@dna-db2:~/tp1/petcalendar$ git diff
eschoi@dna-db2:~/tp1/petcalendar$ ls
next.config.js  package.json  public     server  tsconfig.json         yarn.lock
next-env.d.ts   pages         README.md  styles  tsconfig.server.json
eschoi@dna-db2:~/tp1/petcalendar$ cat README.md
This is a [Next.js](https://nextjs.org/) project bootstrapped with [`create-next-app`](https://github.com/vercel/next.js/tree/                           canary/packages/create-next-app).

##20220518
## Getting Started

First, run the development server:

```bash
npm run dev
# or
yarn dev
```

Open [http://localhost:3000](http://localhost:3000) with your browser to see the result.

You can start editing the page by modifying `pages/index.tsx`. The page auto-updates as you edit the file.

[API routes](https://nextjs.org/docs/api-routes/introduction) can be accessed on [http://localhost:3000/api/hello](http://loca                           lhost:3000/api/hello). This endpoint can be edited in `pages/api/hello.ts`.

The `pages/api` directory is mapped to `/api/*`. Files in this directory are treated as [API routes](https://nextjs.org/docs/a                           pi-routes/introduction) instead of React pages.

## Learn More

To learn more about Next.js, take a look at the following resources:

- [Next.js Documentation](https://nextjs.org/docs) - learn about Next.js features and API.
- [Learn Next.js](https://nextjs.org/learn) - an interactive Next.js tutorial.

You can check out [the Next.js GitHub repository](https://github.com/vercel/next.js/) - your feedback and contributions are we                           lcome!

## Deploy on Vercel

The easiest way to deploy your Next.js app is to use the [Vercel Platform](https://vercel.com/new?utm_medium=default-template&                           filter=next.js&utm_source=create-next-app&utm_campaign=create-next-app-readme) from the creators of Next.js.

Check out our [Next.js deployment documentation](https://nextjs.org/docs/deployment) for more details.
eschoi@dna-db2:~/tp1/petcalendar$
eschoi@dna-db2:~/tp1/petcalendar$
eschoi@dna-db2:~/tp1/petcalendar$ git remote -v
origin  http://10.1.203.13:9090/eschoi/petcalendar.git (fetch)
origin  http://10.1.203.13:9090/eschoi/petcalendar.git (push)
remote  http://10.1.203.13:9090/toyproject/petcalendar.git (fetch)
remote  http://10.1.203.13:9090/toyproject/petcalendar.git (push)
eschoi@dna-db2:~/tp1/petcalendar$ git fetch remote
Username for 'http://10.1.203.13:9090': eschoi
Password for 'http://eschoi@10.1.203.13:9090':
eschoi@dna-db2:~/tp1/petcalendar$
eschoi@dna-db2:~/tp1/petcalendar$
eschoi@dna-db2:~/tp1/petcalendar$ ls
next.config.js  package.json  public     server  tsconfig.json         yarn.lock
next-env.d.ts   pages         README.md  styles  tsconfig.server.json
eschoi@dna-db2:~/tp1/petcalendar$ vi README.md
eschoi@dna-db2:~/tp1/petcalendar$
eschoi@dna-db2:~/tp1/petcalendar$
eschoi@dna-db2:~/tp1/petcalendar$
eschoi@dna-db2:~/tp1/petcalendar$ git pull
Username for 'http://10.1.203.13:9090': eschoi
Password for 'http://eschoi@10.1.203.13:9090':
Already up to date.
eschoi@dna-db2:~/tp1/petcalendar$
eschoi@dna-db2:~/tp1/petcalendar$
eschoi@dna-db2:~/tp1/petcalendar$ git checkout remote
error: pathspec 'remote' did not match any file(s) known to git.
eschoi@dna-db2:~/tp1/petcalendar$
eschoi@dna-db2:~/tp1/petcalendar$ git branches
git: 'branches' is not a git command. See 'git --help'.
eschoi@dna-db2:~/tp1/petcalendar$ git branch
* master
eschoi@dna-db2:~/tp1/petcalendar$
eschoi@dna-db2:~/tp1/petcalendar$
eschoi@dna-db2:~/tp1/petcalendar$ git remote show remote
Username for 'http://10.1.203.13:9090': eschoi
Password for 'http://eschoi@10.1.203.13:9090':
* remote remote
  Fetch URL: http://10.1.203.13:9090/toyproject/petcalendar.git
  Push  URL: http://10.1.203.13:9090/toyproject/petcalendar.git
  HEAD branch: master
  Remote branch:
    master tracked
  Local ref configured for 'git push':
    master pushes to master (local out of date)
eschoi@dna-db2:~/tp1/petcalendar$ git pull remote
Username for 'http://10.1.203.13:9090': eschoi
Password for 'http://eschoi@10.1.203.13:9090':
You asked to pull from the remote 'remote', but did not specify
a branch. Because this is not the default configured remote
for your current branch, you must specify a branch on the command line.
eschoi@dna-db2:~/tp1/petcalendar$ git pull remote origin
Username for 'http://10.1.203.13:9090': eschoi
Password for 'http://eschoi@10.1.203.13:9090':
fatal: Couldn't find remote ref origin
eschoi@dna-db2:~/tp1/petcalendar$ git pull remote master
Username for 'http://10.1.203.13:9090': eschoi
Password for 'http://eschoi@10.1.203.13:9090':
remote: HTTP Basic: Access denied
fatal: Authentication failed for 'http://10.1.203.13:9090/toyproject/petcalendar.git/'
eschoi@dna-db2:~/tp1/petcalendar$
eschoi@dna-db2:~/tp1/petcalendar$
eschoi@dna-db2:~/tp1/petcalendar$
eschoi@dna-db2:~/tp1/petcalendar$
eschoi@dna-db2:~/tp1/petcalendar$ git pull remote master
Username for 'http://10.1.203.13:9090': eschoi
Password for 'http://eschoi@10.1.203.13:9090':
From http://10.1.203.13:9090/toyproject/petcalendar
 * branch            master     -> FETCH_HEAD
Auto-merging README.md
CONFLICT (content): Merge conflict in README.md
Automatic merge failed; fix conflicts and then commit the result.
eschoi@dna-db2:~/tp1/petcalendar$ vi README.md
eschoi@dna-db2:~/tp1/petcalendar$
eschoi@dna-db2:~/tp1/petcalendar$
eschoi@dna-db2:~/tp1/petcalendar$ ls
next.config.js  package.json  public     server  tsconfig.json         yarn.lock
next-env.d.ts   pages         README.md  styles  tsconfig.server.json
eschoi@dna-db2:~/tp1/petcalendar$ vi README.md
eschoi@dna-db2:~/tp1/petcalendar$ ls
next.config.js  package.json  public     server  tsconfig.json         yarn.lock
next-env.d.ts   pages         README.md  styles  tsconfig.server.json
eschoi@dna-db2:~/tp1/petcalendar$
eschoi@dna-db2:~/tp1/petcalendar$ git add .
eschoi@dna-db2:~/tp1/petcalendar$ git commit -m "error fix"
[master b9cdb06] error fix
eschoi@dna-db2:~/tp1/petcalendar$ git push
Username for 'http://10.1.203.13:9090': eschoi
Password for 'http://eschoi@10.1.203.13:9090':
Counting objects: 16, done.
Delta compression using up to 16 threads.
Compressing objects: 100% (16/16), done.
Writing objects: 100% (16/16), 1.93 KiB | 990.00 KiB/s, done.
Total 16 (delta 10), reused 0 (delta 0)
To http://10.1.203.13:9090/eschoi/petcalendar.git
   0648094..b9cdb06  master -> master
eschoi@dna-db2:~/tp1/petcalendar$
eschoi@dna-db2:~/tp1/petcalendar$
eschoi@dna-db2:~/tp1/petcalendar$ ls
next.config.js  package.json  public     server  tsconfig.json         yarn.lock
next-env.d.ts   pages         README.md  styles  tsconfig.server.json
eschoi@dna-db2:~/tp1/petcalendar$ vi next.config.js
eschoi@dna-db2:~/tp1/petcalendar$ git add .
eschoi@dna-db2:~/tp1/petcalendar$ git commit -m "날짜 추가"
[master 70c62a3] 날짜 추가
 1 file changed, 1 insertion(+)
eschoi@dna-db2:~/tp1/petcalendar$ git push
Username for 'http://10.1.203.13:9090': eschoi
Password for 'http://eschoi@10.1.203.13:9090':
remote: HTTP Basic: Access denied
fatal: Authentication failed for 'http://10.1.203.13:9090/eschoi/petcalendar.git/'
eschoi@dna-db2:~/tp1/petcalendar$ git push
Username for 'http://10.1.203.13:9090': eschoi
Password for 'http://eschoi@10.1.203.13:9090':
eschoi@dna-db2:~/tp1/petcalendar$
eschoi@dna-db2:~/tp1/petcalendar$
eschoi@dna-db2:~/tp1/petcalendar$ git remote -v
origin  http://10.1.203.13:9090/eschoi/petcalendar.git (fetch)
origin  http://10.1.203.13:9090/eschoi/petcalendar.git (push)
remote  http://10.1.203.13:9090/toyproject/petcalendar.git (fetch)
remote  http://10.1.203.13:9090/toyproject/petcalendar.git (push)
eschoi@dna-db2:~/tp1/petcalendar$ git push origin master
Username for 'http://10.1.203.13:9090': eschoi
Password for 'http://eschoi@10.1.203.13:9090':
Counting objects: 3, done.
Delta compression using up to 16 threads.
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 299 bytes | 299.00 KiB/s, done.
Total 3 (delta 2), reused 0 (delta 0)
To http://10.1.203.13:9090/eschoi/petcalendar.git
   b9cdb06..70c62a3  master -> master
eschoi@dna-db2:~/tp1/petcalendar$


Jekyll also offers powerful support for code snippets:

{% highlight ruby %}
def print_hi(name)
  puts "Hi, #{name}"
end
print_hi('Tom')
#=> prints 'Hi, Tom' to STDOUT.
{% endhighlight %}

Check out the [Jekyll docs][jekyll-docs] for more info on how to get the most out of Jekyll. File all bugs/feature requests at [Jekyll’s GitHub repo][jekyll-gh]. If you have questions, you can ask them on [Jekyll Talk][jekyll-talk].

[jekyll-docs]: https://jekyllrb.com/docs/home
[jekyll-gh]:   https://github.com/jekyll/jekyll
[jekyll-talk]: https://talk.jekyllrb.com/
