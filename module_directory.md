# Module Directory

- Api
> php interfaces for business logic use cases
- Api/Data
> data interfaces for the data transfer objects that are used with the Api interfaces, both Api and Api/Data are called "service contract"
- Block
> view logic
- Console
> Commands excuteds for magento
- Controller
> for request process logic
- Cron
> code for tasks that are excuted by cron
- CustomerData
> server side data available to the store front javascript
- etc
> configration, with areas `frontend` and `adminhtml`
- Helper
> lengthy namespace, it doesn't really have specific meaning, so it should be avoided in new module.
- i18n
> internationalization folder, contains the source csv files translation basically.
- Model
> implementations of Api interfaces
- Observer
> event dispatch
- Plugin
> contains classes for modifies the behavior of Magento2 extension 
- Pricing
> an example for module specific class
- Setup
> data magration
- Test
> unit / integration / functionality tests
- Ui
> classes use by admin UI
- view
> css / javascript / template files, contains `base`, `frontend`, `adminhtml`
- ViewModel
> new home for the view logic, works for the blocks



