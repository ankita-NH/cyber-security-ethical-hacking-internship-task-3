sqli_report.md

Date: 2025-11-04
Tester: Ankita Mondal

Summary - Simple SQL Injection check found a critical issue allowing login bypass and a medium issue leaking DB errors via search.

Scope -

  Target: http://example.com
  Pages: /login (POST), /search (GET)
Findings -

  1. High — /login (parameter: username)
     Type: Boolean-based SQLi (auth bypass)
     PoC (POST):
