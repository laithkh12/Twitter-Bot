# 🌐 Internet Speed Twitter Bot

A Python script that checks your internet speed using **Speedtest.net** and tweets a complaint to your Internet Service Provider (ISP) if the speed is slower than promised.

---

## 📋 Features

- Measures **download** and **upload** speeds using Speedtest.net.
- Tweets an automatically generated complaint to your ISP via your Twitter account.

---

## ⚙️ Prerequisites

Before you start, ensure you have the following:

1. **Python 3.7+**
2. **Google Chrome Browser**
3. **ChromeDriver** compatible with your Chrome version.
4. Install required Python libraries:
   ```bash
   pip install selenium
    ```
---
## 🚀 How to Use
1. Clone this repository or copy the script into your working directory.
2. Update the following variables in the script:
```python
PROMISED_DOWN = 150  # Your promised download speed in Mbps
PROMISED_UP = 10     # Your promised upload speed in Mbps
TWITTER_EMAIL = "your_email@example.com"
TWITTER_PASSWORD = "your_password"
```
3. Run the script
--- 
## 📂 Script Workflow
1. Internet Speed Test
  - Navigates to Speedtest.net.
  - Measures download and upload speeds.
  - Extracts and stores the results.
2. Twitter Login and Complaint
  - Logs in to your Twitter account.
  - Composes a tweet tagging your ISP and including the speed test results.
  - Posts the tweet.
--- 
## 🖋️ Example Output Tweet
```plaintext
Hey Internet Provider, why is my internet speed 50down/5up when I pay for 150down/10up?
```
---
## ⚠️ Important Notes
- Account Security: Use a throwaway Twitter account if you’re concerned about sharing your login credentials in the script.
- Dynamic XPATHs: Twitter's UI can change, which might break the script. Update the XPATHs if elements cannot be located.
- Speedtest GDPR Pop-up: If a pop-up appears, uncomment the relevant lines in get_internet_speed() to handle it:
```python
# accept_button = self.driver.find_element(By.ID, value="_evidon-banner-acceptbutton")
# accept_button.click()
```
---
## 🛠 Troubleshooting
- **Browser Not Opening**? Ensure the chromedriver executable is installed and added to your system's PATH.
- **Login Issues**? Double-check your Twitter credentials and try again.
- **Tweet Not Posting**? Ensure that the tweet element’s XPATH matches Twitter’s current layout. Update the script if needed.
--- 
## 🤝 Contributing
Contributions are welcome! Feel free to submit a pull request or suggest improvements.
---
## 📄 License
This project is licensed under the MIT License. See the LICENSE file for details.
---
## 🌟 Acknowledgments
- Powered by Selenium WebDriver.
- Speed tests courtesy of Speedtest.net.
- Inspired by the need for better internet service.
---
