project('vulkan-snippets',
	['c', 'cpp'],
	version : '0.1.0',
	license : 'MIT',
	meson_version : '>= 0.49',
  	default_options : [
		'buildtype=release', 
		'c_std=c18', 
		'cpp_std=c++17', 
		'warning_level=3', 
		'werror=true',
		'layout=mirror'
	]
)

c_compiler = meson.get_compiler('c')
cpp_compiler = meson.get_compiler('cpp')

add_project_arguments('-Wno-unused-parameter', language: ['c', 'cpp'])
add_project_arguments('-Wno-unused-function', language: ['c', 'cpp'])
add_project_arguments('-Wno-unused-result', language: ['c', 'cpp'])

glsllang = find_program('glslangValidator')

glfw_dep   = dependency('glfw3', version: '>= 3')
vulkan_dep   = dependency('vulkan')

m_dep = cpp_compiler.find_library('m', required : false)

gl_deps = [glfw_dep, vulkan_dep, m_dep]

subdir('src')
