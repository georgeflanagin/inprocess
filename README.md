# inprocess
Tasks that are actively worked by me.

## Sept 29
- Thinking over how to configure space and hardware for the SAL, TLC, QRC.
- Free up disc space on spydur:/home. Do we need to impose quotas?
- Moved Priscilla's ~/backedup folder to /scratch
- Moved Arryn's ~/shared folder to /scratch
- routing ssl traffic on another port for Arryn
- look into how JATOS moves data in and out of its container.
- trial installation of qchem 6.1
- schedule Linux 8 update of cooper
- first see what happens with real power failure on cooper.
- getting a ChromeBook to see what students are up against.
- Scheduled a time for Sasko to change the IP address of the internal switch; need to suspend jobs. We are going to do it next Friday.
- wrote a quick script to get the amount of disc space any one user is using.
- Fixed a couple of things for Art with his students' `submit` command for their assignments.
- Fixed a permissions problem for Kelling. His student had set his own umask to 0002, and that prevented group write to the working directory.
- Debugged a problem with a container not accepting forwarded https traffic.
- Carlos Hurtado Martilletti wants help "executing some code on Spydur."
- Changed the permissions on Kelling's student's $HOME so that he can browse them with some kind of windows program.
- wrote a short note for Kelling and Carol summarizing the use of Linux groups on Spydur.

## October 2
- received the intern recruiting brochure from National Geo Intel Agency, and passed them along to Saif and Lauren w/ a bit of explanation.
- cleaned up Arryn's and Tolya's 300+G of test data, and moved it to /scratch. /home/arobbins/shared is now a symlink.
- dealt with Hiago Lopes Carvalho's inability to login. I punted him to the Help Desk and Mariama (his faculty sponsor).
- Installed qchem on Sarah to test the mounted version of the software. The BrianQC package for GPU enabled calculations takes a while to download. It requires a separate library for each computational class of GPU.
- Catherine wants some backup options for her dataset. She says it is "big," but I am unsure how big. Sent her an email outlining some choices.
- Imposed a 10G soft quota on all members of the Linux group "managed" on the /home mountpoint.
- Jory Brinkerhoff dropped a 1TB gzipped tarball on spydur:/home. Sent him an email, and I'm moving his file to /scratch.
- Briefly read about https://www.cilogon.org/. Some members of CLAC are using it instead of guest logins.
- Fully backedup cooper. Sent Khanh a message to ask it were OK to begin Linux 8 migration/upgrade.
- Spent an hour with Alina talking over her recent experience at the Women in Computing conference in Orlando, her program, and the job prospects.
- Cloned Alina's program onto Quark for testing. Ran into an interesting roadblock with the `pam_slurm_adopt` module. Need to read about that one.
- Sent Gladys and message about meeting in Charlottesville next week to discuss WHPC.
- Got the license file from QChem for Sarah.

## October 3
- Enlisted Sasko's help to test Alina's program as the root user on quark. This is a bit of a bomb; the pam_slurm_adopt module prevents even the SlurmUser from logging into compute nodes. That seems like an ill conceived idea.
- Wrote short message about Linux software as the topic is related to the QRC.
- Continued the move of Jory Brinkerhoff's files to /scratch. Space on /scratch is not "tight," but I am realizing the need to work on the duplicate file identification for the old Parish Lab data recovery effort.
- I submitted ticket #20581366 to install `fdupes` on Spydur. With 87T of files to examine, it is worth a few hours of analysis to determine the best course of action. I think this problem will recur over the next few years, and we likely need to build a Merkle tree for the files so that we have a record of files we have already examined for duplicates.
- I wrote a description of several ongoing projects for Joao to help him know what he is getting into --- file dedup-ing, Linux 7 to 8 migration, need to create a repo of documents for the "how to" operations.
- Sasko installed `fdupes`. I cloned the git repo of the source. A little analysis has convinced me that it may not be much faster than `undeux`. Same for jdupes. Almost all the latency is going to be in reading the files and calculating the hashes. One of the optimizations in `undeux` is doing a stochastic analysis of files that are the same size rather than directly calculating the MD5 or SHA1 of the entire file. The 6350R processor has special instructions for the SHA-256 algorithm. AMD processors have instructions for the AES operations. Interesting competitive choice.
- Jory's files are still rsync-ing over to /scratch. I'm using ionice on it to be kind to everyone else.

## October 4
- Distributed the NGA materials to Carol for further distro to DADS.
- Had a 30 minute powwow with Carol.
- Quite a bit of back and forth with MARIA members about the pam_slurm_adpot problems. I have thought of a way around it; it will be interesting to get Sasko's reaction. 
- Rescheduled the spydur switch work for Monday at 3pm. I put a job in the cron to suspend all the running jobs at 14:55 on Monday.
- Finished the clean up of Jory Brinkerhoff's files. Curiously, he has not responded to my email informing him about my changes.
- I have a workable design for a duplicate file identifier.
- I restored newton onto alexis.
