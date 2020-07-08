project('blink', 'c')

include_path = include_directories(
  ['include',
   'src',
   '/opt/riscv/include/gd32vf103'])

sources = [
  'src' / 'main.c',
  'src' / 'systick.c'
]

args = ['-D HXTAL_VALUE=8000000',
	'-march=rv32imac',
	'-mabi=ilp32']

sdk_lib = dependency('gd32vf103_sdk')
  
executable('blink.bin',
	   sources,
	   c_args : args,
	   dependencies : sdk_lib,
	   include_directories: include_path)
