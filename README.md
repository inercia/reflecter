Reflecter
=========

[![status](https://sourcegraph.com/api/repos/github.com/inercia/reflecter/.badges/status.png)](https://sourcegraph.com/github.com/inercia/reflecter)

A library for setting an arbitrary value in a structure by reflection.

It only provides one function:

    Set(cfg interface{}, sect, sub, name string, blank bool, value string)

where you can pass an arbitrary structure `cfg`, and `sect`, `sub` will be substructures
and `name` an attribute that will be assigned a `value`.

Example
-------

    type Config structure {
        type Global structure {
            Host string
        }
    }

    cfg := Config{}
    
    Set(cfg, "Global", "", "Host", false, "somehost.com")


Credits
-------

The code of this library comes from [Gcfg](https://github.com/shizeeg/gcfg)
