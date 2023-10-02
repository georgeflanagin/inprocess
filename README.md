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
