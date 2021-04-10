inhibit_all_warnings!
platform :ios, '10.3'
use_frameworks!
workspace 'demo-temporario'

source 'https://github.com/CocoaPods/Specs.git'

target 'demo-temporario' do

	#pod 'RxSwift',    '5.1.1'
	#pod 'RxCocoa',    '5.1.1'
	#pod 'RxSwiftExt', '5.2.0'
	#pod 'RxRelay', '5.1.1'
	#pod 'SwiftyJSON', '5.0.0'
	#pod 'Zip', '~> 1.1.0'
	
	#pod 'R.swift', '5.0.3'
	#pod 'JTAppleCalendar', '7.1.7'
	#pod 'AnimatedCollectionViewLayout', '1.0.1'
	
	#pod 'pop', :git => 'https://github.com/facebook/pop.git', :commit => 'b4ff2db'
	#pod 'lottie-ios' , '3.1.5'
	#pod 'PhoneNumberKit', '3.1.0'
	#pod 'Fakery', '4.1.1'
	##pod 'Quick', '2.2.0'
	##pod 'Nimble', '8.0.4'

	## Maps | # Analytics
	#pod 'Firebase', '6.34.0'
	#pod 'FirebaseCrashlytics', '4.6.2'
	#pod 'FirebaseAnalytics', '6.9.0'
	#pod 'FirebaseCore', '6.10.4'
	#pod 'FirebaseMessaging', '4.7.1'
	##pod 'GoogleMLKit/TextRecognition', '0.64.0'
	#pod 'GoogleTagManager', '7.1.2'
	#pod 'GoogleMaps', '3.0.3'
	#pod 'GooglePlaces', '3.0.3'
	#pod 'GoogleIDFASupport', '3.14.0'

	##Dynatrace
	#pod 'Dynatrace', '8.191.1.1003'
	#pod 'AppsFlyerFramework',  '5.0.0'

	## Instance ID provides a unique ID per instance of your apps
	## This pod will provide the app an unique ID for the push notification infrastructure
	## based on Firebase Cloud Message
	#pod 'GGLInstanceID', '1.2.1'

	## Salesforce SDK
	## Specs: https://github.com/CocoaPods/Specs/tree/master/Specs/5/c/7/MarketingCloudSDK
	##pod 'MarketingCloudSDK', '~> 7.2.1' 

	## TouchID
	#pod 'Valet',  '3.2.6'

	## Data storage
	#pod 'RealmSwift', '3.17.3'
	#pod 'RxDataSources', '4.0.1'
	#pod 'CryptoSwift', '1.2.0'
	#pod 'SwiftLint', '0.38.0'
	pod 'SDWebImageWebPCoder', '0.6.1'
end


post_install do |installer|
    installer.pods_project.targets.each do |target|

        target.build_configurations.each do |config|
            
            config.build_settings['SWIFT_VERSION'] = '5.0'
            
            # enable tracing resources
            if target.name == 'RxSwift'
                if config.name == 'Debug'
                    config.build_settings['OTHER_SWIFT_FLAGS'] ||= ['-D',
                    'TRACE_RESOURCES']
                end
            end
            
            # enabling WMO - improve compiling time
            if config.name == 'Debug'
                config.build_settings['OTHER_SWIFT_FLAGS'] = ['$(inherited)', '-Onone']
                config.build_settings['SWIFT_OPTIMIZATION_LEVEL'] = '-Owholemodule'
            end
        end
    end
end