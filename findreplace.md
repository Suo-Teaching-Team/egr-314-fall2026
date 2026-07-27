## Blog stuff that might be useful

### honestly don't remember
Find: ```(\n)*(?<abc>[a-zA-Z0-9\-\.]*.md(.old)*)\:[0-9]+\: +\[[0-9]*\]\: (?<xyz>[a-zA-Z0-9\-\.\/\:_\%]*)```
Replace: ```$<abc> : $<xyz>\n```


### find blogger pages and replace with local

Find: ```https*://esdresources.blogspot.com/[0-9]+/[0-9]+/([a-zA-Z\-_0-9]*.html)```
Replace: ```$1```


### Find all local pages

Find: ```\[[^\]]*\]: (?!https://)(?!http://)([a-zA-Z0-9\-]*).html```
(see script for updat)

### remove all image sizing:

find:
(.jpg)?(.png)?\)\{width ?= ?"[0-9]*.?[0-9]*(?:in)?" height ?= ?"[0-9]*.?[0-9]*(?:in)?"\}

replace: 
$1$2)

### find images 

find:
(!\[[^\]]*\]\([^\)]*\))
$1{class="img-fluid"}



\{width="[0-9\.]*in" height="[0-9\.]*in"\}

## Assignments Specific

- [x] remove image sizes
- put files with media in media folder and re-link to images
	- [x] 304
	- [x] 314
	- [x] 3x4
```
\]\([a-z0-9_\-\/]*/media/(image[0-9]*.(jpg)|(png))\)
]($1)
```
- [x] move each file to its own subfolder

## find all blank headings

```
\n#+\s*\n
\n
```

## Add one level to each heading

```
\n(#+) 
\n$1# 
```

## FInd / replace I2C

```
I^2^C
I$^{\text{2}}$C
```

```
\^([a-zA-Z0-9]+)\^
$^{\\text{$1}}$
```

## find all ~ subscripts

```
([a-zA-Z0-9])+~([a-zA-Z0-9\(\)\-]+)~
$ $1_{$2}$
```

## Other things

find all \
	- [x] first search for ```c:\``` in assignments/ and replace with c:/
	- [x] find and replace all \ 
- [ ] fix all tables
- [ ] find all text highlighting
- [ ] remove author
- [ ] fix code in 304-ind-4
- [ ] render and put .pdfs in each subfolder
- [ ] go through each one and check numbering
- [ ] fix tags
- [ ] fix titles
- [x] remove "_media"
- [x] find and fix ^
- [x] find and fix all gdrive links, 
- [ ] find kicad references
- [x] replace drive.google.com
- [x] replace docs.google.com/forms
- [x] find all cases of [](#)


remove all unique numbering

\n( *)[0-9]+. 
\n$11. 

## Gdrive

ignore findreplace.md

https://docs.google.com/document/d/1Ro6jcPiLVnl5EZwWh3wUa1-_vhCZaKgC7zEQaXWHjtA/edit?usp=sharing --> https://embedded-systems-design.github.io/zipping-folders/
https://drive.google.com/file/d/1DjvQtCnnX0tKc26Dg_9bxzLTTBxbPvyU/view?usp=sharing --> https://www.dropbox.com/s/futmq59a8ftekqs/Agilent_DMM_34461A.pdf?dl=0
https://drive.google.com/file/d/1D4fR8lzklkaj7-2HBhOpkh4Ymo9nrY7m/view?usp=sharing --> https://www.dropbox.com/s/l818d0y20eas2if/PSoC%20Creator%20Workshop%202022_042_BLE.pdf?dl=0
https://drive.google.com/file/d/1lWk6RAqHjkjaFjXM-4nzjHRkzSl0_QSe/view?usp=sharing --> https://www.dropbox.com/s/uch6vnjg1pdluot/PSoC%204%20Lab%204%20-%20ADC%20-%20Lab%20Manual.pdf?dl=0
https://drive.google.com/file/d/1Ns6p8K3XyJ593nfJf-T72bxpPuznUdFQ/view?usp=sharing --> https://www.dropbox.com/s/u2fvszz5fb9zc5v/researcher-interview.mp4?dl=0
https://drive.google.com/file/d/1FfErBZiJLz2hJYblqwd6E_HEYZumOHcc/view?usp=sharing --> https://www.dropbox.com/s/dnzuxsooed6mugu/the-right-question-at-the-right-time.pdf?dl=0
https://drive.google.com/file/d/1lO7VqYL1XVlZCGp5exOZO-r5Ixs0dPqU/view?usp=sharing --> https://www.dropbox.com/s/ryy5fefd22a8smt/ICC2%20Video%20Demo%201%20-%20Adjusting%20output%20frequencies%20through%20the%20function%20generator?dl=0
https://drive.google.com/file/d/1suDWkndFZi7yV_X16ZUictZDDYpmmkfx/view?usp=sharing --> https://www.dropbox.com/s/c11nz27bndt6szi/ICC2%20Video%20Demo%202%20Part%201%20-%20Initial%20setups%20on%20an%20oscilloscope?dl=0
https://drive.google.com/file/d/12YF2fsNSRvW8ksqst3hTGZTVHgb0-t31/view?usp=sharing --> https://www.dropbox.com/s/t366yjidczue78v/ICC2%20Video%20Demo%202%20Part%202%20-%20Adding%20measurements%20through%20an%20oscilloscope?dl=0
https://drive.google.com/file/d/1zVosc_4U5ubucQU0fOhIIONPz780_0aY/view?usp=sharing --> https://www.dropbox.com/s/ixg73lw0w80j5wg/PCB166FootprintsV2.pdf?dl=0
https://drive.google.com/file/d/1Lhwdq3CX7WOWVeYjzVb97loMlO3gL9fa/view?usp=sharing --> https://www.dropbox.com/s/zl4cw2mw9yciovc/USB_UART.zip?dl=0
https://drive.google.com/open?id=1bXV1sEPefDxy0fRaXwCXUTCq78YXa_8b --> https://www.dropbox.com/sh/0pu5curaf0s2bs8/AAC_PwZxVOF_R2ny7IMxwVjea?dl=0
https://drive.google.com/file/d/1a_JoRmNdTWWhL4rNuknohBbHjHdo0L4t/view?usp=sharing --> https://www.dropbox.com/s/0cm6geqigvpwgek/HBR%20Lean%20Startup.pdf?dl=0
https://drive.google.com/file/d/14Hqv5cTWHxAi5W3lpQxgaAnU9IVKEQGn/view?usp=sharing --> https://www.dropbox.com/s/ixg2uu3bmf9254d/GameControllerV2.pdf?dl=0
https://drive.google.com/open?id=1ivDWVppBY5WvStoCB0bBMqG3C0eVm_CG&authuser=daukes%40asu.edu&usp=drive_fs --> https://www.dropbox.com/s/62i7214y63ljucp/eone-1602a1.pdf?dl=0
https://drive.google.com/file/d/1wckV5ZjqKTbDDQgznJLvaOMorE3cvu03/view?usp=sharing --> https://www.dropbox.com/s/diwlmp9pu0mazga/BusinessModelGeneration.pdf?dl=0
https://drive.google.com/open?id=1Fxhh6hrndDBE93BL13CYIkMT2XWfruOv&authuser=daukes%40asu.edu&usp=drive_fs --> https://www.dropbox.com/s/6s7bbjd0oe8agww/Quiescent%20Current.pdf?dl=0
https://drive.google.com/file/d/1ekXHLUWSOYZDXDSqwH-KwiFCZYhGyTDs/view?usp=sharing --> https://www.dropbox.com/s/03bsgncmavl72bx/Block%20Diagram-304-BLE.drawio?dl=0
https://drive.google.com/file/d/1sOpu82-nU3rgnuajeR75AqMwPE21lWZa/view?usp=sharing --> https://www.dropbox.com/s/l0isntlxyjduvtj/Block%20Diagram-304-BLE.drawio.png?dl=0
https://drive.google.com/file/d/1rSXNcIMEyjkQjMWA1XpthHp4qrvySjuh/view?usp=sharing --> https://www.dropbox.com/s/bs90okyqkg6x926/pic-lcd-library-master.zip?dl=0
https://drive.google.com/file/d/1r-HzsfYRBKCmFp6u4VGM9qWPXIejGzfP/view?usp=sharing --> https://www.dropbox.com/s/ktxzxiipkfyypls/airoccysmart_1.3_Windows_x86-x64.exe?dl=0
https://drive.google.com/file/d/1WBu5swI6xXVlfhOO_qmv6YVkKIsHxBI0/view?usp=sharing --> https://www.dropbox.com/s/rfoy6kx59nhxx7e/UML%20Spec.pdf?dl=0
https://drive.google.com/file/d/1AwhKN-LynIqHGbKjotiLX8Eun6kLVHgf/view?usp=sharing --> https://www.dropbox.com/s/qbphzio2o5mcemx/Simple%20Activity%20Diagram%20Example.pdf?dl=0
https://drive.google.com/open?id=1cYWy41X1kXUQK7jNUCJZrYs2GBPibAY7&authuser=daukes@asu.edu&usp=drive_fs --> https://www.dropbox.com/s/70hfczjdyusv595/Activity%20Diagram%20Example.pdf?dl=0
https://drive.google.com/open?id=1cYWy41X1kXUQK7jNUCJZrYs2GBPibAY7&authuser=daukes%40asu.edu&usp=drive_fs --> https://www.dropbox.com/s/70hfczjdyusv595/Activity%20Diagram%20Example.pdf?dl=0
https://drive.google.com/file/d/1ClB_Kyx79LtvQRNUx2WPk-6tdB6Afhen/view?usp=sharing --> https://www.dropbox.com/s/1npw6b2gs0il92r/Water%20Heater%20State%20Chart.drawio?dl=0


https://docs.google.com/document/d/12erQoBJRSltsg35KBDPuPtxJDANjaS92uSBMP5RCzwA/edit?usp=sharing --> https://embedded-systems-design.bitbucket.io/course-sequence-requirements/
https://docs.google.com/spreadsheets/d/1A2EJCd919gQ-zUC5DFDDBjUcXUCBT0_SKDAOuZDLdfI/edit?usp=sharing --> https://www.dropbox.com/s/pdt82mkwr3oty3o/Team%20Topic%20Table%20%28template%29.xlsx?dl=0
https://docs.google.com/spreadsheets/d/13GKUpCpK7g7uLldWeW1uRnIeoFe30OxscdRXtfsdklU/edit?usp=sharing --> https://www.dropbox.com/s/b2g9anxlmh5emlj/Verification%20Table%20Example%20and%20Template.xlsx?dl=0
https://docs.google.com/document/d/1oiKwOQ0xvt14O_Bh0nONxvTRSYAj-ji6eLNhmsXVwZ4/edit?usp=sharing --> 
https://embedded-systems-design.github.io/curiosity-nano-mplab-tutorial-and-lab/
https://docs.google.com/spreadsheets/d/12XLkL3NnF9c4pEVrAhqmVce2DYIdOFYRdX3CXo9aHMI/edit?usp=sharing --> https://www.dropbox.com/s/urnlk2rn0xu6hih/Bill%20of%20Materials%20Example.xlsx?dl=0
https://docs.google.com/spreadsheets/d/1_sj596dMNqtZynGCfHHhiWT5VMXBgHOG72__CpjBLWM/edit?usp=sharing --> https://www.dropbox.com/s/ucr49ujowc9rkb2/Contact%20Information%20and%20Weekly%20Schedule.xlsx?dl=0

https://docs.google.com/spreadsheets/d/108QLsBaF4bRZzLdaiNOlyYD3NkJL-C0BW-xgk-Gn3o8/edit?usp=sharing --> https://www.dropbox.com/s/wyeqisp0uzyiics/Power%20Budget%20Example.xlsx?dl=0
https://docs.google.com/document/d/1bnSca6xFjkNRPmo-hv-5vRdehJhsQL9Yc0zYrqaGKH4/edit?usp=sharing --> https://embedded-systems-design.github.io/pcb-tutorial-notes/
https://docs.google.com/spreadsheets/d/1rYEArkUXjgUSXkwSk1AGPFiQeaq__NDn/edit?usp=sharing&ouid=107532393031596487141&rtpof=true&sd=true --> https://www.dropbox.com/s/k9sgrkeyk3cmc4o/New%20Purchasing%20Template.xlsx?dl=0 
https://docs.google.com/document/d/1zuP3TPbuAHetXfJZHQ2fmftuX9YmvopGKaqaQI-lRHQ/edit?usp=share_link --> https://embedded-systems-design.bitbucket.io/3x4/3x4-team-block-diagram/
https://docs.google.com/document/d/1JnH-hPB5EJ-9XNCHO-N6Apx2J5xsZ2olfwUamIxK93Q/edit?usp=share_link --> https://embedded-systems-design.bitbucket.io/3x4/3x4-team-software-proposal/

## Forms

https://docs.google.com/forms/d/e/1FAIpQLSfXwRix-A_lLkXe_abYj5O0E0CTbJLhkvnPk82VE7sSc-xPhA/viewform?usp=sf_link
https://docs.google.com/forms/d/e/1FAIpQLSdLPjsjYTLKdzX6nE3YK6D1LGTLpaDcm6da32jqQCGk8K9phA/viewform?usp=sf_link

## different for 304/314

https://docs.google.com/document/d/12JVVkhBFgWNKuxJ_Lgp1UWPju_RxGBU04aXYhIqPv4c/edit?usp=sharing --> https://embedded-systems-design.bitbucket.io/304/project-description/
--> https://embedded-systems-design.bitbucket.io/314/project-description/


https://docs.google.com/document/d/16jBEGrz0KabPsfGHUDYbI9S-JHZ1LmaTruC-Fj_2qgs/edit?usp=sharing --> https://embedded-systems-design.bitbucket.io/304/304-team-06-checkpoint-1/
--> https://embedded-systems-design.bitbucket.io/314/314-team-06-checkpoint-1/

https://docs.google.com/document/d/1urHfG_wmmpZVdFq1_NFFMdwVOnpQA_uD6vntyHCS2g8/edit?usp=sharing --> https://embedded-systems-design.bitbucket.io/304/304-team-03-user-needs-and-benchmarking/

https://docs.google.com/document/d/10_4TaTExZyyRWNWCGBf3wGtg00YkzITLQc5ivpk7uF8/edit?usp=sharing --> https://embedded-systems-design.bitbucket.io/304/304-team-11-checkpoint-2/
--> https://embedded-systems-design.bitbucket.io/314/314-team-11-checkpoint-2/
