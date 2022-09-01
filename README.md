# phpcs-debug

1. Run `composer install`
2. Navigate to `test.php`. Note that there are no errors from using `_e()` function.
3. Navigate to `/vendor/automattic/phpcs-neutron-ruleset/NeutronRuleset/ruleset.xml`. Comment out lines 86-88.
4. Navigate back to `test.php`. Note that `phpcs` shows the error: `All output should be run through an escaping function (like esc_html_e() or esc_attr_e()), found '_e'.`.
5. Note that lines 17-20 in `phpcs.xml` have the same rule and nested tags that I would expect would override the parent ruleset.
