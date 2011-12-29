Android Market / Google Checkout Scraper
========================================

Introduction
============

This tool is designed to download CSV files for android market 
from google checkout site automatically.

It can download following CSV files.

* Sales report (monthly)
* Order list
* Payout report

Also, it can press all "ship" buttons on google checkout.


Requirements
============

* Ruby >=1.8.7 or >= 1.9.2
* RubyGems
* Mechanize 1.0.0

You need to install Mechanize as:

    $ gem install mechanize -v 1.0.0


Configuration
=============

Copy secrets.rb.sample to secrets.rb, and set up your
mail address and password.


How to use
==========

Get sales report
----------------

To download sales report for 2011/20:

    $ ./get-sales-report.rb 2011 10

Get order report
----------------

To download order report, specify start and end time as:

    $ ./get-orders.rb 2011-08-01T:00:00:00 2011-09-30T23:59:59

You can specify 3rd argument from:

* ALL
* CANCELLED
* CANCELLED_BY_GOOGLE
* CHARGEABLE
* CHARGED
* CHARGING 
* PAYMENT_DECLINED
* REVIEWING


Get payout report
-----------------

To download payout report, specify start / end date as:

    $ ./get-payouts.rb 2011-11-01 2011-12-01

You can specify 3rd argument from:

* PAYOUT_REPORT
* TRANSACTION_DETAIL_REPORT

Auto press ship buttons
-----------------------

Press all "ship" buttons on Orders - Inbox page of google checkout:

    $ ./auto-deliver.rb


License
=======

Public domain


Disclaimer
==========

* NO WARRANTY

---
'11/12/12
Takuya Murakami, E-mail: tmurakam at tmurakam.org
