project('xmahjongg', ['c', 'cpp'], license: 'GPL3+', version : '3.7.4')
  
datadir = get_option('datadir')
appdatadir = join_paths(datadir, meson.project_name())

subdir('liblcdf')
subdir('src')

if host_machine.system() == 'linux'
  # Icon and Desktop files
  install_data('images/xmahjongg.png', install_dir: join_paths(datadir, 'pixmaps'))
  install_data('xmahjongg.desktop', install_dir: join_paths(datadir, 'applications'))
  
  # Man page
  install_data('xmahjongg.6', install_dir: join_paths(datadir, 'man/man6'))
 
  # Project Data
  install_subdir('share/backgrounds', install_dir: appdatadir)
  install_subdir('share/layouts', install_dir: appdatadir)
  install_subdir('share/tiles', install_dir: appdatadir)
endif

