This is a simple Perl script for parsing DMARC aggregate reports from
a set of email messages and summarizing them in a somewhat useful
fashion.


Example output from `dmarc-aggregate-parse -d umich.edu Maildir/.dmarc-reports/new/*`:


```
-----------------------------------------------------------------------------
|*********************************umich.edu*********************************|
-----------------------------------------------------------------------------

                   Earliest timestamp:                   2020-08-13 18:50:46
                     Latest timestamp:                   2020-08-17 13:00:05
                       Total messages:                                190287
               DMARC disposition none:                                190287

Aligned DKIM results:
                                 fail:                                 66906
                                 pass:                                123381

Aligned DKIM successes:
                            umich.edu:                                123354

Aligned SPF results:
                                 fail:                                 22577
                                 pass:                                167710

Domain for aligned SPF successes:
            bounce.c.alumni.umich.edu:                                  2697
                      icpsr.umich.edu:                                    21
                   slate-mx.umich.edu:                                   188
                            umich.edu:                                164794

Recipient orgs:
                           google.com:                                178753
                          Yahoo! Inc.:                                  9857
                          comcast.net:                                  1497
                        emailsrvr.com:                                   144
               ZEROSPAM Security Inc.:                                     8

Mail sources (>2000 messages):
                                   IP:                         209.85.220.41
                             Hostname:              mail-sor-f41.google.com.
                             Messages:                                 22175
                            DKIM fail:                                  1643
                            DKIM pass:                                 20532
                             SPF fail:                                  1793
                             SPF pass:                                 20382

                                   IP:                          35.162.59.88
                             Hostname:         egress-host.a.mail.umich.edu.
                             Messages:                                 19408
                            DKIM fail:                                  7826
                            DKIM pass:                                 11582
                             SPF fail:                                   338
                             SPF pass:                                 19070

                                   IP:                         52.37.117.118
                             Hostname:         egress-host.a.mail.umich.edu.
                             Messages:                                 19065
                            DKIM fail:                                  7711
                            DKIM pass:                                 11354
                             SPF fail:                                   305
                             SPF pass:                                 18760

```
