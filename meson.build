project('xmahjongg', ['c', 'cpp'], license: 'GPL3+', version : '3.7.4')

subdir('liblcdf')
subdir('src')

if host_machine.system() == 'linux'
  # Icon and Desktop files
  datadir = get_option('datadir')

  install_data('images/xmahjongg.png', install_dir: join_paths(datadir, 'pixmaps'))

  install_data('xmahjongg.desktop', install_dir: join_paths(datadir, 'applications'))
endif

