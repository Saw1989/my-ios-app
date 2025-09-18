platform :ios, '13.0'
inhibit_all_warnings!
use_frameworks!

target 'DerNagelhof' do
  # Deine Pods hier, z. B.:
  # pod 'Alamofire', '~> 5.9'
end

post_install do |installer|
  installer.pods_project.targets.each do |t|
    t.build_configurations.each do |config|
      config.build_settings['EXCLUDED_ARCHS[sdk=iphonesimulator*]'] = 'arm64'
    end
  end
end
