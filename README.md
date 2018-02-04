LineageOS 14.1 for Jelly Pro
------------------------------------

Create directories

	$ mkdir cm-14.1
	$ cd cm-14.1

the local manifests:

	$ repo init -u git://github.com/LineageOS/android.git -b cm-14.1
	$ git clone https://github.com/deadman96385/local_manifest -b cm-14.1 .repo/local_manifests

Then sync up with this command:

	$ repo sync --force-sync -q

-------------
 
_Building from source_
---------------

	$ cd device/jelly/jellypro/patches
	$ ./check-patches.sh
	$ ./apply-patches.sh
	$ . build/envsetup.sh
	$ lunch lineage_jellypro-userdebug
	$ make bacon
