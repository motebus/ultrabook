# Ultranet Gateway

* create(model, data)
    <br>Function Description功能說明: Create records
    <br>Call Example呼叫範例:

        var data = {
            name: 'Test',
            email: 'test@example.com'
        };
        var result = await xrpc.call("h1/bridge/odoo", "create", ["res.partner", data], 10, 8, 10);


* call(model, method, params)
    功能說明: Call execute_kw RPC function
    呼叫範例:

        var params = ["read", false];
        var result = await xrpc.call("h1/bridge/odoo", "call", ["res.partner", "check_access_rights", params], 10, 8, 10);


* read(model, ids, fields = [])
    功能說明: Read records
    呼叫範例: 

        var result = await xrpc.call("h1/bridge/odoo", "read", ['res.partner', 1, ["name","city","email"]], 10, 8, 10);
        console.log('read result=', result);    


* browse(model, ids, fields = [])
    功能說明: Read records (同read函數)
    呼叫範例: 

        var result = await xrpc.call("h1/bridge/odoo", "browse", ['res.partner', 1, ["name","city","email"]], 10, 8, 10);
        // or
        // result = await xrpc.call("h1/bridge/odoo", "browse", ['res.partner', [1,2,3], ["name","city","email"]], 10, 8, 10);
        console.log('browse result=', result);    


* write(model, ids, data)
    功能說明: Update records
    呼叫範例: 

        var data = {
            name: 'Test',
            email: 'test@example.com'
        };
        var result = await xrpc.call("h1/bridge/odoo", "write", ["res.partner", 1, data], 10, 8, 10);


* unlink(model, ids)
    功能說明: Delete records
    呼叫範例: 

        var result = await xrpc.call("h1/bridge/odoo", "unlink", ["res.partner", 1], 10, 8, 10);


* search(model, params)
    功能說明: List records
    呼叫範例:

        var params = [['name', '=', 'Test']];
        var result = await xrpc.call("h1/bridge/odoo", "search", ["res.partner", params], 10, 8, 10)


* search_read(model, domain = [], fields = [], limit = 0, offset = 0, sort = "")
    功能說明: Search and read
    呼叫範例: 

        var params = [['name', '=', 'Test']];
        var fields = ['name', 'email'];
        var result = await xrpc.call("h1/bridge/odoo", "search_read", ["res.partner", params, fields], 10, 8, 10)


* search_count(model, params)
    功能說明: Count records
    呼叫範例:

        var params = [['name', '=', 'Test']];
        var total = await xrpc.call("h1/bridge/odoo", "search_count", ["res.partner", params], 10, 8, 10)


* fields_get(model, fields = [], attributes = {})
    功能說明: Listing record fields
    呼叫範例:

        var fields = [];
        var attributes = {'attributes': ['string', 'help', 'type']}
        var result = await xrpc.call("h1/bridge/odoo", "fields_get", ["res.partner", fields, attributes], 10, 8, 10)
