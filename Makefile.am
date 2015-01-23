lib_LIBRARIES = libhts.a

libhts_a_SOURCES = \
kfunc.c \
knetfile.c \
kstring.c \
bgzf.c \
faidx.c \
hfile.c \
hfile_net.c \
hts.c \
regidx.c \
sam.c \
synced_bcf_reader.c \
vcf_sweep.c \
tbx.c \
vcf.c \
vcfutils.c \
cram/cram_codecs.c \
cram/cram_decode.c \
cram/cram_encode.c \
cram/cram_index.c \
cram/cram_io.c \
cram/cram_samtools.c \
cram/cram_stats.c \
cram/files.c \
cram/mFILE.c \
cram/md5.c \
cram/open_trace_file.c \
cram/pooled_alloc.c \
cram/rANS_static.c \
cram/sam_header.c \
cram/string_alloc.c \
cram/thread_pool.c \
cram/vlen.c \
cram/zfio.c

libhts_a_CPPFLAGS = -Ihtslib -Icram

bin_PROGRAMS = bgzip htsfile tabix

bgzip_CPPFLAGS = -Ihtslib
bgzip_LDADD = libhts.a
bgzip_SOURCES = bgzip.c

htsfile_CPPFLAGS = -Ihtslib
htsfile_LDADD = libhts.a
htsfile_SOURCES = htsfile.c

tabix_CPPFLAGS = -Ihtslib
tabix_LDADD = libhts.a
tabix_SOURCES = tabix.c

SUBDIRS = test

TESTS = run_tests.sh

# run_tests.sh:
# 	echo "\
# 	test/fieldarith test/fieldarith.sam ; \
# 	test/hfile ; \
# 	test/sam ; \
# 	test/test-regidx ; \
# 	cd test && ./test_view.pl ; \
# 	./test.pl ; \ " > run_tests.sh
# 	chmod +x run_tests.sh

# CLEANFILES = run_tests.sh

# noinst_SCRIPTS = version.sh

# version.sh:
# 	echo "#define HTS_VERSION \"`git describe --always --dirty`\" > version.h