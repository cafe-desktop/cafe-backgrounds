project('cafe-backgrounds',
  version : '1.25.0',
  meson_version: '>= 0.41.0'
  )

i18n = import('i18n')

prefix = get_option('prefix')
datadir = join_paths(prefix, get_option('datadir'))
backgrounddir = join_paths(datadir, 'backgrounds', 'cafe')
metadatadir = join_paths(datadir, 'cafe-background-properties')

conf = configuration_data()
conf.set('datadir', datadir)

subdir('abstract')
subdir('desktop')
subdir('nature')
subdir('po')
