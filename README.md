# Wordpress-Cms-Testing-Methodlogy

# CMS WordPress Testing Checklist

## 1. Information Gathering & Enumeration
- [ ] Identify CMS and CMS version
- [ ] Identify users, plugins, and themes
- [ ] Perform directory and file enumeration
- [ ] Port scanning and service enumeration (Web Server, Database, etc.)
- [ ] Identify the version of WordPress running
- [ ] Enumerate/identify the list of themes and plugins installed on the WordPress site as well as their respective versions
- [ ] Perform file & directory enumeration to identify hidden or sensitive resources
- [ ] **Manual Username Enumeration**
  - [ ] Username ID brute force
  - [ ] Query the WordPress API on wp-json
  - [ ] Analyze login page responses for user existence
- [ ] **Manual Plugin & Theme Enumeration**
  - [ ] Plugin Enumeration
  - [ ] Theme Enumeration
- [ ] **Automated Tools for Enumeration**
  - [ ] WPScan
  - [ ] CMSmap

## 2. Vulnerability Scanning
- [ ] Identify common WordPress misconfigurations and vulnerabilities
- [ ] Perform automated vulnerability scanning with tools like WPScan
- [ ] Test for common misconfigurations and vulnerabilities
- [ ] Perform vulnerability scanning/analysis to identify potential vulnerabilities/misconfigurations in plugins and themes

## 3. Authentication Testing
- [ ] Perform brute-force attacks on /wp-admin.php or /wp-login.php to obtain valid credentials
- [ ] Test WordPress for session management vulnerabilities
- [ ] Perform username enumeration and brute force attacks on login pages
- [ ] Assess session handling for weaknesses and potential session fixation vulnerabilities

## 4. Exploitation
- [ ] Identify and exploit publicly known vulnerabilities in WordPress themes and plugins (XSS, SQLi, etc.)
- [ ] Identify and exploit vulnerabilities in the CMS core
- [ ] Identify and exploit vulnerabilities in plugins/extensions and themes

## 5. Post-Exploitation
- [ ] Establish persistence on WordPress site/Web Server via web shells or backdoors to maintain access
- [ ] Exfiltrate sensitive data from the WordPress site or underlying server
- [ ] Identify ways to maintain access to CMS after exploitation in the form of a backdoor or web shell
- [ ] Attempt to extract data from the CMS or the underlying server

## 6. General Checks
- [ ] Check WordPress Meta Generator Tag
- [ ] Check the WordPress readme.html/license.txt file
- [ ] Inspect HTTP response headers for version information (X-Powered-By)
- [ ] Check the login page for the WordPress version as it is usually displayed
- [ ] Check the WordPress REST API and look for the version field in the JSON response
  - [ ] http://example.com/wp-json/
- [ ] Analyze JS and CSS files for version information
- [ ] Examine the WordPress changelog files with information on version updates. Look for files like changelog.txt or readme.txt in the WordPress directory

## 7. Tools for Automation
- [ ] WPScan
- [ ] CMSmap
- [ ] Other relevant tools for WordPress version enumeration and vulnerability assessment
