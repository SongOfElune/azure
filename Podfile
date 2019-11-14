source 'https://github.com/CocoaPods/Specs.git'

post_install do |installer_representation|
  installer_representation.pods_project.targets.each do |target|
    target.build_configurations.each do |config|
      config.build_settings['SWIFT_VERSION'] = '5.0'
      if config.name.include?('Debug') 
        config.build_settings['ONLY_ACTIVE_ARCH'] = 'YES'
        config.build_settings['DEBUG_INFORMATION_FORMAT'] = 'DWARF'
        config.build_settings['OTHER_SWIFT_FLAGS'] = '-DDEBUG'
      end
    end
  end
end

target 'V' do
  # Comment the next line if you're not using Swift and don't want to use dynamic frameworks
  use_frameworks!

  pod 'PhoneNumberKit'
  pod 'Mapbox-iOS-SDK', '~> 5.1'
  pod 'CryptoSwift'
  pod 'Firebase/Analytics'
  pod 'Firebase/Performance'
  pod 'Crashlytics'
  pod 'Fabric'

  target 'VT' do
    inherit! :search_paths
    pod 'OHHTTPStubs/Swift'
  end
end

target 'VUT' do
  use_frameworks!

end
