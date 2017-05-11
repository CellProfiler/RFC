**Summary**

Add the ability to assess pipeline's current module and move to a different module in TestMode 

**Background and rationale**

CP 2.X had a slider that in test mode allowed you to a) see what module the pipeline had processed up to and b) allowed you to move backward or forward to any other module to execute it.  

The slider was removed sometime in the batch of GUI commits between 0dddf4f and 9cad7ea, but the functionality has never been replaced.

Both these functionalities are important for efficent use of CP in test mode, as evidenced by the fact that there are 4 issues related to the slider's disappearance or replacing its functionality (2032, 2531, 2711, 2712).

Per Allen's request, I made [a forum thread](http://forum.cellprofiler.org/t/poll-testmode-interface-options/4676) detailing a couple of options for replacement and soliciting other ideas.

**Proposal**

The poll was a tie between just restoring the slider as-was or to add a red outline box around the last-processed module and allow the user to right click on a module (as they can currently to duplicate, etc) and provide a "Jump back to here" option in the right click menu.

**Implementation**

The slider code has previously been implemented and can be harvested presumably from commit 0dddf4f or before.  If the consensus of the group is to go the "red box" way, I'll try to find some implementation for that.
