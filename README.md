# Finance Tracker Performance & Security Tests

Automated Security and Performance testing suite for the Finance Tracker application.

## Overview
This project integrates OWASP ZAP with Selenium, TestNG, and Gauge to perform automated security scans and performance tests as part of a DevSecOps pipeline.

### Tech Stack
- **Testing Framework**: Gauge, TestNG
- **Security Tool**: OWASP ZAP (Zed Attack Proxy)
- **Automation**: Selenium WebDriver (Java)
- **Build Tool**: Maven

## Prerequisites
- **Java 8+**
- **Maven**
- **OWASP ZAP**: Installed and running (Default: `localhost:8089`)
- **Chrome Browser**: Latest version

## Configuration
Configuration parameters can be found in:
- `src/test/java/net/oktaliem/utils/driver/Driver.java`: ZAP Proxy settings and Driver paths.
- `env/default/default.properties`: Gauge environment settings.

## Getting Started

### 1. Run OWASP ZAP
Ensure OWASP ZAP is running in the background with the API enabled. Update the `ZAP_PROXYPORT` and `ZAP_APIKEY` in `Driver.java` if necessary.

### 2. Execution

#### Run via TestNG
```bash
mvn clean test -DsuitXmlFile=TestNG.xml
```

#### Run via Gauge
```bash
mvn gauge:execute
```

## Reports
- **Security Reports**: Generated in `target/html/` after execution.
- **Execution Reports**: Gauge HTML reports are available in the `reports/` directory.

## Contributing
Feel free to fork this repository and submit pull requests for any improvements or additional test cases.

## License
MIT License
