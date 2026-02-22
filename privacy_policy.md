# Ariane Privacy Policy

**Last Updated:** February 2026

This privacy policy describes how Ariane ("the Application"), developed by Ariane's Line, collects, uses, stores, and protects your information. We are committed to transparency about our data practices and to protecting your privacy.

## 1. Information We Collect

### 1.1 Information You Provide

- **Email Address**: Required during trial license registration on first launch. Your email is used for license management and is transmitted to our licensing server on each application launch.

### 1.2 Information Collected Automatically

- **Device Identifier (Install Token)**: A unique identifier generated from your operating system name and user home directory path, encrypted before storage and transmission. This is used to associate your license with your device.
- **Operating System Information**: Your OS name, version, and architecture (e.g., "Windows 11", "10.0", "amd64") are transmitted during license validation.
- **Application Version**: The version of Ariane you are running is sent during license checks.
- **Session Identifier**: A randomly generated UUID is created for each application session and sent during license validation. This identifier is not persistent and changes every time you launch the application.

### 1.3 Information You Create

- **Cave Survey Data**: Project files (`.tml`, `.tmlu`, `.json`) containing survey data, station coordinates, GPS positions, and annotations are stored locally wherever you choose to save them. This data is not transmitted to us.
- **Settings and Preferences**: Your display settings, map provider selection, and UI preferences are stored locally in `~/.ariane/displaysettings`.
- **Recent Projects List**: Paths to recently opened project files are stored locally in `~/.ariane/recentprojects`.

## 2. How We Use Your Information

| Data | Purpose |
|------|---------|
| Email address | License validation and management |
| Install token | Device identification for license enforcement |
| OS information | Compatibility tracking and license validation |
| Application version | License validation and update notifications |
| Session ID | License session management |

We do **not** use your data for advertising, profiling, or any purpose beyond application licensing and functionality.

## 3. Third-Party Services

Ariane interacts with the following third-party services. Data is only transmitted when the corresponding feature is used.

### 3.1 Ariane Licensing Server

- **Purpose**: License validation, trial registration, and version checking.
- **Data Transmitted**: Email address, encrypted install token, session ID, application version, OS name/version/architecture.
- **When**: On every application launch.

### 3.2 GitHub API

- **Purpose**: Checking for application updates.
- **Data Transmitted**: None (anonymous read of public release information).
- **When**: On application launch.

### 3.3 Map Tile Providers (User-Selected)

When you enable the satellite imagery view, Ariane fetches map tiles from your chosen provider. The following data is transmitted to the selected provider:

| Provider | Data Transmitted |
|----------|-----------------|
| Google Maps | Latitude/longitude, zoom level, image size |
| Google Maps Hybrid | Latitude/longitude, zoom level, image size |
| Azure Maps (Microsoft) | Latitude/longitude, zoom level, image dimensions |
| HERE Maps | Latitude/longitude, zoom level, image size |
| Mapbox | Latitude/longitude, zoom level, image size |

These requests transmit the geographic coordinates of the area you are viewing. Fetched tiles are cached locally in `~/.ariane/Cache/`. Each provider is subject to its own privacy policy.

### 3.4 Google Maps Geocoding API

- **Purpose**: Converting geographic coordinates to human-readable place names (reverse geocoding).
- **Data Transmitted**: Latitude and longitude.
- **When**: When reverse geocoding is triggered by the user.

## 4. Data Storage

### 4.1 Local Storage

All application data is stored locally on your computer. Key storage locations include:

| Location | Contents |
|----------|----------|
| `~/.ariane/displaysettings` | Display preferences and settings (XML) |
| `~/.ariane/recentprojects` | List of recently opened project files (XML) |
| `~/.ariane/cachedeclination.txt` | Cached magnetic declination values |
| `~/.ariane/Cache/` | Encrypted license data and cached map tiles |
| `~/.ariane/Plugins/` | Plugin JAR files |
| System preferences (OS-specific) | Encrypted license data |

### 4.2 No Cloud Storage

Ariane does not store your cave survey data, project files, or personal data in any cloud service. All project data remains on your local machine unless you choose to share it.

## 5. Data We Do NOT Collect

- **No Telemetry**: We do not collect usage analytics or telemetry data.
- **No Crash Reporting**: We do not automatically transmit crash reports or diagnostic data.
- **No Location Tracking**: We do not access your device's GPS or location services. Geographic coordinates come exclusively from cave survey data you enter or import.
- **No Payment Information**: The application does not collect or process payment data.
- **No Browsing or Activity Tracking**: We do not track your behavior within the application.

## 6. Serial Device Communication

When connected to a Mnemo cave surveying device via USB/serial port, all communication occurs locally between your computer and the device. No survey data from the device is transmitted over the internet.

## 7. Data Sharing

We do not sell, rent, or share your personal information with third parties, except:

- **License Validation**: Your email and device identifier are transmitted to our licensing server as described in Section 3.1.
- **Map Tile Requests**: Geographic coordinates are transmitted to your selected map tile provider as described in Section 3.3.
- **Reverse Geocoding**: Geographic coordinates may be transmitted to Google as described in Section 3.4.

## 8. Data Security

- Your install token and license data are encrypted before storage and transmission.
- License communication with our server uses HTTPS.
- Map tile cache files are stored using SHA-256 hashed filenames that do not directly reveal the geographic locations.

## 9. Your Rights and Choices

- **Map Provider Selection**: You can choose which map tile provider to use, or disable satellite imagery entirely to prevent geographic data transmission to third parties.
- **Offline Use**: After initial license activation, core survey functionality works without an internet connection (license validation will be attempted but the application can function in offline mode).
- **Data Deletion**: You can delete all locally stored data by removing the `~/.ariane/` directory. License data stored in system preferences can be cleared through your operating system's preference management tools.
- **Data Portability**: Your cave survey data is stored in standard XML and JSON formats that you control entirely.

## 10. Children's Privacy

Ariane is not directed at children under 13. We do not knowingly collect personal information from children under 13.

## 11. Changes to This Policy

We may update this privacy policy from time to time. Changes will be documented in this file and in the application's release notes. We encourage you to review this policy periodically.

## 12. Contact

If you have questions about this privacy policy or our data practices, please contact us at:

- **Website**: [https://www.arianesline.com](https://www.arianesline.com)
- **Email**: <sebastien@arianesline.com>
