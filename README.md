# Mailstrom

An AWS SES no-bells-and-whistles mass-mailing tool. It just takes a static
(HTML) email end gets it to a list of recipients.

## Usage

```sh
export AWS_ACCESS_KEY_ID='xxx'
export AWS_SECRET_ACCESS_KEY='xxx'
bin/mailstrom --from 'me@example.com' --subject 'My Subject' --recipients recipients.txt --email email.html
```

## Things to consider

When sending a lot of emails, there is the risk of getting flagged as a spammer
by Google, which can be mitigated by adding your domain at
[https://postmaster.google.com/](https://postmaster.google.com/).

AWS will put you on probation if there is a certain share of bounces. From the email we got:
> We expect our senders' bounce rates to remain below 5%. Senders with a bounce rate exceeding 10% risk suspension.

## TODOs

* Validate the command line arguments
