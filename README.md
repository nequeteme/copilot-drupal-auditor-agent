# copilot-drupal-auditor-agent

This is a custom agent in Copilot and Visual Studio Code that uses PHPCS to verify code and make the necessary changes to comply with coding standards.

PHP_CodeSniffer (PHPCS) is a static code analysis tool that detects violations of coding standards in PHP files. It helps maintain code quality and consistency across all projects by comparing it to predefined sets of rules. The tool can analyze not only standard PHP files but also custom extensions used on CMS platforms like Drupal.


# Installation
In my installation I did it globally, but I think it could be done locally in the project.
```bash
# Install PHP_CodeSniffer and Drupal Coder (Drupal coding standards)
composer global require phpstan/phpstan drupal/coder:^8.3.10 --with-all-dependencies 

# Register Drupal standards with PHPCS (adjust path for your system)
phpcs --config-set installed_paths ~/.config/composer/vendor/drupal/coder/coder_sniffer
# Windows alternative path:
# phpcs --config-set installed_paths C:\Users\YOUR_USERNAME\AppData\Roaming\Composer\vendor\drupal\coder\coder_sniffer


# Verify installation
phpcs -i
# Expected output: The installed coding standards are MySource, PEAR, PSR1, PSR2, PSR12, Squiz, Zend, Drupal and DrupalPractice

```

# Quick Usage
- Open the file
- Press Ctrl+Shift+P → "Tasks: Run Task"
- Select: "PHPCS: Check current file"
- Copy the errors of the terminal
- Open Chat of copilot and select the agent "drupal-auditor-agent"
- Paste the error and continue

# Upgrade
By reading, watching courses, and experimenting, I created a harness engineer AI for Drupal; this is the URL.
https://github.com/nequeteme/agent-harness-drupal
