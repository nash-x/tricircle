Glance-Cascading Patch
================


Introduction
-----------------------------

*For glance cascading, we have to create the relationship bewteen one cascading-glance and some cascaded-glances.  In order to achieve this goal, we using glance's multi-location feature, the relationshiop can be as a location with the special format.  Besides, we modify the image status changing-rule:  The image's active toggle into 'active' only if the cascaded have been synced.  Because of these two reasons, a few existing source files were modified for adapting the cascading:

   glance/api/v2/image.py
   glance/gateway.py
   glance/common/utils.py
   glance/common/config.py
   glance/common/exception.py

**Because in Juno, the code of glance store part is move out of the glance as an independent python project, the modification in Juno about the glance store is moved to the glance_store in Juno. **

 Install
 ------------------------------


 *To implement this patch just replacing the original files to these files, or run the install.sh in glancesync/installation/ directory.
