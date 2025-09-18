# Podfile
platform :ios, '13.0'

# optional, macht Logs ruhiger
inhibit_all_warnings!

# häufig sinnvoll
use_frameworks!

# >>> HIER deinen App-Target-Namen eintragen (mit ' ' ) <<<
target 'DerNagelhof' do
  # Pods for MyApp (Beispiele)
  # pod 'Alamofire', '~> 5.9'
  # pod 'Kingfisher', '~> 7.0'
end

# >>> Optional: Falls du ein Test-Target hast, Namen anpassen oder Block löschen <<<
target 'DerNagelhof' do
  inherit! :search_paths
  # Pods for tests (falls nötig)
end

# Nützliche Post-Install-Anpassungen für CI
post_install do |installer|
  installer.pods_project.targets.each do |t|
    t.build_configurations.each do |config|
      # Simulator-ARM64 ausschließen (vermeidet häufige CI-Probleme, schadet hier nicht)
      config.build_settings['EXCLUDED_ARCHS[sdk=iphonesimulator*]'] = 'arm64'
    end
  end
end
