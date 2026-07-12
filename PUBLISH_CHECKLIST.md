# Fondant Queue Craft - Publish Checklist

## 1. Project Configuration
- [x] Bundle ID: com.rosewood.fondantqueuecraft.game (contains 'rosewood')
- [x] TARGETED_DEVICE_FAMILY: "1" (iPhone only, set at project + target level)
- [x] MARKETING_VERSION: "1.0"
- [x] CURRENT_PROJECT_VERSION: "1"
- [x] ASSETCATALOG_COMPILER_APPICON_NAME: AppIcon
- [x] GENERATE_INFOPLIST_FILE: NO
- [x] No CODE_SIGNING_* settings in project.yml

## 2. Info.plist
- [x] CFBundleDisplayName: Fondant Queue Craft
- [x] CFBundleIconName: AppIcon
- [x] ITSAppUsesNonExemptEncryption: false
- [x] UIRequiredDeviceCapabilities: arm64
- [x] UISupportedInterfaceOrientations: UIInterfaceOrientationPortrait
- [x] UILaunchStoryboardName: LaunchScreen

## 3. LaunchScreen.storyboard
- [x] Root tag is `<document>` (lowercase)
- [x] No references to non-existent images
- [x] Valid layout with title and subtitle

## 4. App Icon
- [x] AppIcon.appiconset with Icon-1024.png (marketing icon)
- [x] No alpha channel on icons
- [x] CFBundleIconName set to AppIcon

## 5. Debug UI
- [x] showsFPS = NO (ViewController.m)
- [x] showsNodeCount = NO (ViewController.m)
- [x] prefersStatusBarHidden = YES

## 6. Screenshots
- [x] screenshots_65/: 4 JPEG images, 1284x2778, RGB
- [x] screenshots_55/: 4 JPEG images, 1242x2208, RGB
- [x] No alpha channel on screenshots

## 7. Publish Files
- [x] index.html (landing page)
- [x] privacy.html (privacy policy)
- [x] keywords.txt (92 chars, under 100 limit)
- [x] appstore-review-text.html (Format 3, 20 fields, 5 sections)
- [x] GAMEPLAY_FACT_CARD.md
- [x] PUBLISH_CHECKLIST.md
- [x] README.md
- [x] vercel.json (cleanUrls: false, trailingSlash: false)
- [x] .gitignore (.vercel)

## 8. Template Residue
- [x] No tw_*, game_01_*, Template residue

## 9. Archive Build
- [x] xcodebuild archive with CODE_SIGNING_ALLOWED=NO
- [x] .app UIDeviceFamily = [1]
- [x] .app CFBundleIdentifier = com.rosewood.fondantqueuecraft.game
- [x] .app CFBundleIconName = AppIcon
- [x] .app ITSAppUsesNonExemptEncryption = false
- [x] .app UIRequiredDeviceCapabilities = [arm64]
- [x] .app contains Assets.car
- [x] .app contains Base.lproj/LaunchScreen.storyboardc

## 10. GitHub
- [x] Repository: https://github.com/a254791905522/fondant-queue-craft
- [x] All publish files pushed

## 11. Vercel
- [x] Project: fondant-queue-craft
- [x] URL: https://fondant-queue-craft.vercel.app
- [x] /privacy.html accessible (HTTP 200)
- [x] vercel.json with cleanUrls=false

## 12. Reviewer Information
- [x] Last Name: Omondi
- [x] First Name: Evans
- [x] Phone: +1 2096550297
- [x] Email: croitorzamkov@gmail.com
- [x] Sign-in Required: No
