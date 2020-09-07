---
layout: post
title: "FirstPost : FrigidSec Blog"
author: Saket Upadhyay
subtitle: "Topics, Writing Style, Peer Review, GitHub Structure, CoC and everything in between"
date: 2020-08-30 04:23:13 
background: '/img/posts/def.jpg' 
---

Welcome to the first post of **FrigidSec Blog**!

And what's better than getting familiar with the structure of the blog and its code of conduct?

So, let's have a quick glance at the basics :

## Topics

The writer may choose anything that helps to add to the community knowledge of Cybersecurity, its concepts, tips, tricks, etc.

The interest of this blog generally revolve around technical and practical cybersecurity, including but not limited to :

* Interesting CTF Writeup
* BugBounty Tip / Tricks
* Personal Research Results
* Random interesting findings in the field
* Writeup of your significant project proposal/findings
* etc.

## Writing Style: Tone, Gesture and Coverage

The writing style can be semi-casual, but should not exclude any technical details of the topic. 

The tone of the article can be `anything but disrespectful`.
If the article is found to be too aggressive, disrespectful, targetted, or mentions certain topics, items, people, etc. which are not acceptable or might hurt the reader's feelings, it will be rejected.

Serious or `intentional breach of conduct will result in temporary BAN of the author` which can be extended as should the requirements arise.

`The article should be >70% original`, and can contain references to other facts, articles, papers, posters, journals, announcements, news, etc. over the internet to build a base or to support a conclusion.

## Peer Review

Not everyone is good at writing articles and expressing their findings in writing and that's okay. We are here to support you and your work, together as a community.

Hence, peer review. Every article is checked and enhanced by the members of the community who are good in literature and can help in improving the article's overall presentation: grammar, structure, tone, and so on...


## GitHub Structure
This blog is hosted on GitHub pages via FrigidSec/blog repo's `deployment` branch. 

It is based on Ruby - Jekyll stack and the posts are written in Markdown in the `_posts` directory in dep. branch.

The `master-branch` is reserved for front matter presentation and `post-submission` from fellow members.

Anyone who wants to submit their article for the Community Blog should `fork` the repo and `push` the article in `Submission` Directory of the `master` branch within a new folder named as --  `date_title` *(for example 2020-08-12\_firstblog)*

Following is the structure of the general article submission folder structure :

```
Master						[branch]
 |
 |
 \---> Submissions				[folder]
	|
	|---> DATE_TITLE			[folder]
	|	|
 	|	|---> images			[folder]
 	|	|	|---> image1		[file (.png, .jpg)]
 	|	|	|---> image2		[file (.png, .jpg)]
 	|	|	\ ...
 	|	|
 	|	|---> article.docx		[file (.txt, .md, .docx)]
	|	|---> status.txt		[file (NOT to be edited by author)]
 	|	\---> rnotes.txt		[file (for review notes)]
	|
 	\---> 2020-08-01_How-to-do-BOF		[folder]
		|
		|---> images			[folder]
		|	|---> ss1.png		[file (.png, .jpg)]
		|	|---> ss2.jpg		[file (.png, .jpg)]
		|	\ ...
		|
		|---> article.docx		[file (.txt, .md, .docx)]
		|---> status.txt		[file (NOT to be edited by author)]
		\---> rnotes.txt		[file (for review notes)]

```



Then create a `pull-request` for `master` and it will be under review.

After submission, the team will engage and might ask you for some modification, clarity, etc. or they might themselves rectify the things according to their capabilities.

After the article is accepted and the PR is accepted, we will internally pull the post from `master` and process it in `deployment` so that it is added to the actual blog online.



## Code of Conduct

1. Editors must obey laws on confidentiality in their own jurisdiction. Regardless of local statutes, however, they should always protect the confidentiality of individual information obtained in the course of research or professional interactions (e.g. between doctors and patients). It is therefore almost always necessary.
 
2. Zero tolerance for Plagiarism, Bullying, Hate Speech, any kind of Abuse.

3. Credits should be given to Author, Editors, Peers (Reviewers)

4. Proper Citation should be given to all resources

5. All the work is under `CCBY4.0` License by Default. The author can request if needed otherwise.

> Complete CoC can be found @ GitHub/FrigidSec/Documents [DOWNLOAD PDF](https://github.com/FrigidSec/Documents/blob/master/CodeOfConduct/Blog/FrigidBlog_CodeOfConduct_v1.pdf) 
> All documents are 'Work in Progress' as of 31st Aug 2020

## Closing words 

That being said, we look forward to your submissions for the blog!

---

> All current and potential writers, by requesting article publication in FrigiSec Blog are assumed to have accepted the Code of Conduct Mentioned in the Documents repository [HERE](https://github.com/FrigidSec/Documents) 

