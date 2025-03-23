
liblcdf_static = static_library('lcdf', 
	['clp.c', 'fmalloc.c',
	'giffunc.c', 'gifread.c', 'gifx.c',
	'permstr.cc', 'straccum.cc', 'string.cc', 'vectorv.cc'],
	include_directories: '../include',
	install : false)

giftoc_exec = executable('giftoc',
  'giftoc.c',
  include_directories: '../include',
  install: false)

