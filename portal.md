##  Error Message

1. {ErrCode=1, ErrMsg="Voucher Error"}=Voucher is not existing.
2. {ErrCode=2, ErrMsg="Topic Error"}=It's not standard topic.
3. {ErrCode=3, ErrMsg="odoo Fail"}=odoo API or host error.

##  Payload

1. voucher

voucher code of model.
> "voucher":"PPB" (for ppblog)
> "voucher":"MBK" (for mbook)
> "voucher":"DAY" (for daily)

2. act

cc to tg(format: tg://-)
> "act" : "tg://-123456789"
> "act" : ["tg://-123456789","tg://-987654321"]

3. data

field name of model.
> "data":{"name" : "ABC","message" : "Hello"}