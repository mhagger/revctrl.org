A scalar merge algorithm, related to CodevilleMerge.  Generally referred to as "mark-merge" or "*-merge" (but never StarMerge, which is something else entirely).

Detailed writeup of original version: [http://thread.gmane.org/gmane.comp.version-control.monotone.devel/4297] ("unique-*-merge")

Detailed writeup of updated version (handles accidental clean merges): http://article.gmane.org/gmane.comp.version-control.revctrl/93 ("multi-*-merge")

Other links: [http://article.gmane.org/gmane.comp.version-control.revctrl/92], [http://article.gmane.org/gmane.comp.version-control.revctrl/197] ("deterministic-*-merge")

The most interesting things about *-merge are:
  * has a UserModel
  * has a formal analysis showing that it is fully well-defined, and implements the UserModel

= Strengths =

  * best formal analysis of any current merge algorithm
  * believed to never clean merge without justification (conservative)
  * "deterministic *-merge" (basically multi-*-merge but easier to make formal statements about) is commutative and associative (i.e., satisfies OperationalTransformation theory's properties TP1 and TP2).

= Weaknesses =

  * unique-*-merge does not handle accidental clean merges; multi-*-merge does
  * does not handle StaircaseMerge
  * does not attempt convergence
  * does not attempt implicit rollback

= Used by =

["Monotone"]

= Related =

CodevilleMerge

----

CategoryMergeAlgorithm CategoryScalarMerge