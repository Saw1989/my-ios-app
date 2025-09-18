# Podfile (funktionierendes Grundgerüst)
platform :ios, '13.0'

# Optional, macht Logs ruhiger
inhibit_all_warnings!

# Falls du dynamische Frameworks brauchst (häufig):
use_frameworks!

target 'DerNagelhof' do
  # Pods for DerNagelhof
  # Beispiel:
  # pod 'Alamofire', '~> 5.9'

  # Falls du Swift Packages nutzt, stören die Pods nicht.
end

# Optional: Test-Target – passe den Namen an oder lösche den Block
target 'DerNagelhof' do
  inherit! :search_paths
  # Pods for tests (falls nötig)
end

# Optional: Post-Install Fixes (hilfreich auf CI)
post_install do |installer|
  installer.pods_project.targets.each do |t|
    t.build_configurations.each do |config|
      # Simulator-ARM64 ausschließen ist häufig praktisch – schadet hier nicht
      config.build_settings['EXCLUDED_ARCHS[sdk=iphonesimulator*]'] = 'arm64'
    end
  end
end
