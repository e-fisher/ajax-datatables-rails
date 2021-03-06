# CHANGELOG

## 0.1.1
* Fixes problem on `searchable_columns` where the corresponding model is
a composite model name, e.g. `UserData`, `BillingAddress`. 
Thanks to [iruca3](https://github.com/iruca3) for the fix.

## 0.1.0
* A fresh start. Sets base class name to: `AjaxDatatablesRails::Base`.
* Extracts pagination functions to mixable modules.
  * A user would have the option to stick to the base
    `AjaxDatatablesRails::Extensions::SimplePaginator` or replace it with
    `AjaxDatatablesRails::Extensions::Kaminari` or
    `AjaxDatatablesRails::Extensions::WillPaginate`, depending on what he/she is using to handle record pagination.
* Removes dependency to pass in a model name to the generator. This way,
  the developer has more flexibility to implement whatever datatable feature is required.
* Datatable constructor accepts an optional `options` hash to provide
  more flexibility. 
  See [README](https://github.com/antillas21/ajax-datatables-rails/blob/master/README.mds#options) for examples.
* Sets generator inside the `Rails` namespace. To generate an
  `AjaxDatatablesRails` child class, just execute the
  generator like this: `$ rails generate datatable NAME`.