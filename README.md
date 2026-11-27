# Block The Junk by SiteKings public phone feed

Choose a live CSV for your integration. Both downloads are available over HTTPS without a key.

| Download | Includes | Intended use |
| --- | --- | --- |
| [Community-only CSV](https://junk.sitekings.net/v1/public/blocklist.csv) | Approved Block The Junk community numbers and counts | A curated community signal |
| [Combined screening CSV](https://junk.sitekings.net/v1/public/screening.csv) | Approved community numbers plus recent FCC and FTC complaint signals | Call labeling and screening with source-specific counts |

The [community snapshot in GitHub](blocklist.csv) is a point-in-time copy. Poll the live CSV links for current data.

## Community-only columns

| Column | Description |
| --- | --- |
| phone_number | US phone number in E.164 format |
| report_count | Number of accepted reports |
| distinct_installations | Number of different app installations that reported the number |

## Combined screening columns

| Column | Description |
| --- | --- |
| phone_number | US phone number in E.164 format |
| community_report_count | Accepted Block The Junk reports for a number eligible for the community feed |
| community_distinct_installations | Distinct app installations for that community entry |
| fcc_report_count | Recent report records counted in the FCC snapshot |
| ftc_report_count | Recent report records counted in the FTC snapshot |

Each number appears once. A zero means that source has no published signal for the row. Agency records may describe the same call, so adding the columns cannot establish a unique complaint or person count. The agency columns use the [FCC Unwanted Calls dataset](https://opendata.fcc.gov/Consumer/Consumer-Complaints-Data-Unwanted-Calls/vakf-fz8e) and the [FTC Do Not Call Reported Calls dataset](https://www.ftc.gov/policy-notices/open-government/data-sets/do-not-call-data). The live download contains aggregate phone-number data. Keep the phone column as text when importing into a spreadsheet.

Use each download as a full replacement. A number can leave the feed after a correction, withdrawal, expiration, or change in corroboration. Caller ID can be spoofed and the agency complaints are unverified. Use the combined feed for screening signals and check context before blocking. For a correction or removal request, [contact SiteKings](https://sitekings.net/contact/) with the affected number.
