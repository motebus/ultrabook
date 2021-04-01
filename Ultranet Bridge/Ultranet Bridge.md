# Ultranet Bridge

* create(model, data)
    <br>Function Description: Create records
    <br>Call Example:

        var data = {
            name: 'Test',
            email: 'test@example.com'
        };
        var result = await xrpc.call("h1/bridge/odoo", "create", ["res.partner", data], 10, 8, 10);


* call(model, method, params)
    <br>Function Description: Call execute_kw RPC function
    <br>Call Example:

        var params = ["read", false];
        var result = await xrpc.call("h1/bridge/odoo", "call", ["res.partner", "check_access_rights", params], 10, 8, 10);


* read(model, ids, fields = [])
    <br>Function Description: Read records
    <br>Call Example: 

        var result = await xrpc.call("h1/bridge/odoo", "read", ['res.partner', 1, ["name","city","email"]], 10, 8, 10);
        console.log('read result=', result);    


* browse(model, ids, fields = [])
    <br>Function Description: Read records (same as read Function)
    <br>Call Example: 

        var result = await xrpc.call("h1/bridge/odoo", "browse", ['res.partner', 1, ["name","city","email"]], 10, 8, 10);
        // or
        // result = await xrpc.call("h1/bridge/odoo", "browse", ['res.partner', [1,2,3], ["name","city","email"]], 10, 8, 10);
        console.log('browse result=', result);    


* write(model, ids, data)
    <br>Function Description: Update records
    <br>Call Example: 

        var data = {
            name: 'Test',
            email: 'test@example.com'
        };
        var result = await xrpc.call("h1/bridge/odoo", "write", ["res.partner", 1, data], 10, 8, 10);


* unlink(model, ids)
    <br>Function Description: Delete records
    <br>Call Example: 

        var result = await xrpc.call("h1/bridge/odoo", "unlink", ["res.partner", 1], 10, 8, 10);


* search(model, params)
    <br>Function Description: List records
    <br>Call Example:

        var params = [['name', '=', 'Test']];
        var result = await xrpc.call("h1/bridge/odoo", "search", ["res.partner", params], 10, 8, 10)


* search_read(model, domain = [], fields = [], limit = 0, offset = 0, sort = "")
    <br>Function Description: Search and read
    <br>Call Example: 

        var params = [['name', '=', 'Test']];
        var fields = ['name', 'email'];
        var result = await xrpc.call("h1/bridge/odoo", "search_read", ["res.partner", params, fields], 10, 8, 10)


* search_count(model, params)
    <br>Function Description: Count records
    <br>Call Example:

        var params = [['name', '=', 'Test']];
        var total = await xrpc.call("h1/bridge/odoo", "search_count", ["res.partner", params], 10, 8, 10)


* fields_get(model, fields = [], attributes = {})
    <br>Function Description: Listing record fields
    <br>Call Example:

        var fields = [];
        var attributes = {'attributes': ['string', 'help', 'type']}
        var result = await xrpc.call("h1/bridge/odoo", "fields_get", ["res.partner", fields, attributes], 10, 8, 10)
