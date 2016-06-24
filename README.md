# TYPO3 Namespace Converter

You have old TYPO3 extensions that returned from their grave and want to use them in new TYPO3 6 or 7 projects?
To bad, because you have to namespace all your classes by hand...

*Really*?
**NO**! Now you can use this little but pretty handy node tool to migrate all your TYPO3 PHP junks into sexy PSR4 compliant classes.

# Install

1. Pull from git
2. Run `npm install`

# How to use

    node main.js <old-namespace> <new-namespace> <namespace-root-folder>
    
    Example:
    node main.js Tx_PackageName "Vendor\PackageName" "H:\Code\Project\some\sub\folder\Classes"
    
# How it Works

- Replaces Tx_PackageName_Controllers_MainController with Vendor\PackageName\Controllers\MainController.
- Replaces Tx_Extbase... with TYPO3\CMS\Extbase.
- Adds a `namespace` line below the opening tag.