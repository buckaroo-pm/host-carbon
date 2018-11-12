xcode_developer_dir = read_config('apple', 'xcode_developer_dir', '/Applications/Xcode.app/Contents/Developer')

genrule(
  name = 'carbon-framework', 
  out = 'Carbon.framework', 
  cmd = 'cp -r ' + xcode_developer_dir + '/Platforms/MacOSX.platform/Developer/SDKs/MacOSX.sdk/System/Library/Frameworks/Carbon.framework $OUT', 
)

prebuilt_apple_framework(
  name = 'carbon', 
  framework = ':carbon-framework', 
  preferred_linkage = 'static', 
  visibility = [
    'PUBLIC', 
  ], 
)
