# Change Log

## [2.0.1] 2022-06-30

- Update dependencies
- Migration to React 18
- Migration to sass from node-sass

## [2.0.0] 2020-01-20

### IMPORTANT

- We have updated this product from Bootstrap 3 to Bootstrap 4, so in essence, this is a new product
- For this, we have followed the guidelines from [here](https://react-bootstrap.github.io/migrating/) and [here](https://getbootstrap.com/docs/4.0/migration/)
- We also did not add Bootstrap variables as part of our styles (we will do so in one of our next updates, probably in version 3.0.0 when we'll add Bootstrap 5)

### Bug fixing

- The `Navar.Collapse` component now opens like the default `Bootstrap` / `React-Bootstrap` ones, so we've dropped the support for `Navar.Collapse` opening on the `left` / `right` of a page as some sort of a `Sidebar`
- https://github.com/creativetimofficial/ct-light-bootstrap-dashboard-pro-react/issues/54
- https://github.com/creativetimofficial/ct-light-bootstrap-dashboard-pro-react/issues/53
- https://github.com/creativetimofficial/ct-light-bootstrap-dashboard-pro-react/issues/50
- https://github.com/creativetimofficial/ct-light-bootstrap-dashboard-pro-react/issues/48
- https://github.com/creativetimofficial/ct-light-bootstrap-dashboard-pro-react/issues/43
- https://github.com/creativetimofficial/ct-light-bootstrap-dashboard-pro-react/issues/41
- https://github.com/creativetimofficial/ct-light-bootstrap-dashboard-pro-react/issues/40
- https://github.com/creativetimofficial/light-bootstrap-dashboard-react/issues/62

### Major style changes

- Since the update from Bootstrap 3 to Bootstrap 4, all styles have been changed

### Deleted components

- Droped the usage of Pixeden Icons, and added Nucleo Icons instead
- `src/components/Card/Card.jsx` - now it is simple React and HTML code
- `src/components/Card/MapCard.jsx` - now it is simple React and HTML code
- `src/components/Card/StatsCard.jsx` - now it is simple React and HTML code
- `src/components/Card/UserCard.jsx` - now it is simple React and HTML code
- `src/components/CustomButton/CustomButton.jsx` - now it is simple React and HTML code
- `src/components/CustomButton/CustomButton.jsx` - now it is simple React and HTML code
- `src/components/CustomCheckbox/CustomCheckbox.jsx` - now it is simple React and HTML code
- `src/components/CustomRadio/CustomRadio.jsx` - now it is simple React and HTML code
- `src/components/FormInputs/FormInputs.jsx` - now it is simple React and HTML code
- `src/components/Tasks/Tasks.jsx` - now it is simple React and HTML code
- `src/variables/Variables.jsx` - moved these variables inside the components that were using them
- `src/variables/chartsVariables.jsx` - moved these variables inside the components that were using them
- `src/variables/faVariables.jsx` - we've delete the usage of this as well

### Added components

- `src/components/TagsInput/TagsInput.js` (and dropped the usage of `react-tagsinput` plugin - but the props from this new component are the exact same as `react-tagsinput`, so please refer to its docs for props etc.)

### Deleted dependencies

- react-syntax-highlighter
- react-notification-system
- @types/googlemaps (will use Google Maps API with Vanilla JS)
- @types/react (will use Google Maps API with Vanilla JS)
- @types/markerclustererplus (will use Google Maps API with Vanilla JS)
- react-google-maps (will use Google Maps API with Vanilla JS)
- wnumb (we haven't used it in the last versions)
- react-tagsinput (we'll use ReactTagsInput component from inside `src/components/TagsInput/TagsInput.js`)
- react-bootstrap-switch (we'll use custom forms as switches from react-bootstrap instead: https://react-bootstrap.github.io/components/forms/#forms-custom-switch)
- react-stepzilla (since it does not work with hooks)

### Added dependencies

- @fortawesome/fontawesome-free@5.15.2 (which means that we have updated from fontawesome v4 to v5 as well)
- prop-types@15.7.2
- reactstrap@8.8.1 (Only as optional dependencies, since the React Notification Alert needs it)
- react-notification-alert@0.0.13
- react-bootstrap-wizard@0.0.9 (instead of react-stepzilla)
- match-sorter@6.1.0 (for the new react-table api)

### Updated dependencies

```
bootstrap                      3.3.7   →    4.5.3
history                        4.9.0   →    5.0.0
moment                        2.24.0   →   2.29.1
node-sass                     4.12.0   →    4.14.1
nouislider                    13.1.5   →   14.6.3
perfect-scrollbar              1.4.0   →    1.5.0
react                         16.8.6   →   17.0.1
react-big-calendar            0.20.4   →   0.30.0
react-bootstrap               0.32.4   →    1.4.3
react-bootstrap-sweetalert     4.4.1   →    5.2.0
react-chartist                0.13.3   →   0.14.3
react-datetime                2.16.3   →    3.0.4
react-dom                     16.8.6   →   17.0.1
react-jvectormap               0.0.9   →   0.0.16
react-router                   5.0.0   →    5.2.0
react-router-dom               5.0.0   →    5.2.0
react-scripts                  3.0.0   →    4.0.1
react-select                   2.4.3   →    3.2.0
react-table                   6.10.0   →    7.6.3
typescript                     3.4.5   →    4.1.3
```

### Warning

**The TypeScript dependencies are installed only to stop console warnings on install. They are not actually used in our product. So the product is not on TypeScript!**
_The following warnings will appear when running the installation command, but they do not affect the UI or the functionality of the product (they will be solved in our next update):_

```
npm WARN react-big-calendar@0.30.0 requires a peer of react@^16.6.1 but none is installed. You must install peer dependencies yourself.
npm WARN react-big-calendar@0.30.0 requires a peer of react-dom@^16.6.1 but none is installed. You must install peer dependencies yourself.
npm WARN react-datetime@3.0.4 requires a peer of react@^16.5.0 but none is installed. You must install peer dependencies yourself.
npm WARN react-chartist@0.14.3 requires a peer of react@^0.14.9 || ^15.0.0 || ^16.0.0 but none is installed. You must install peer dependencies yourself.
npm WARN react-popper@1.3.7 requires a peer of react@0.14.x || ^15.0.0 || ^16.0.0 but none is installed. You must install peer dependencies yourself.
npm WARN create-react-context@0.3.0 requires a peer of react@^0.14.0 || ^15.0.0 || ^16.0.0 but none is installed. You must install peer dependencies yourself.
```

_If they will persist in our 2.4.\* version, we will drop their usages and replace them with other plugins._
_In development mode, some of the above plugins will throw a warning because they still use React v16 syntax. If the error will persist in our 2.4.\* version, we will drop their usage and replace them with other plugins._

### Upgrade details

- Updated all packages from `package.json` using `npm-upgrade`, link here: https://www.npmjs.com/package/npm-upgrade
- Renamed all `ControlLabel` components to `FormLabel` (this refers to the react-bootstrap components)
- Renamed all `Grid` components to `Container` (this refers to the react-bootstrap components)
- Rename all `HelpBlock` components to `FormText`
- Rename all `MenuItem` components to `Dropdown.Item` and `NavDropdown.Item`
- Rename all Panel components to Card
- Deleted variables folder
- Change the usage of `React Big Calendar` to the new API, so instead of

```
import BigCalendar from "react-big-calendar";
```

- And

```
const localizer = BigCalendar.momentLocalizer(moment);
```

- We will have:

```
import { Calendar as BigCalendar, momentLocalizer } from "react-big-calendar";
```

- And

```
const localizer = momentLocalizer(moment);
```

- Change Panels with new react-bootstrap components
- For Col componets, replaced `size={number1} sizeOffest={number2}` with `size={{span: number1, offset: number2}}` where size can be `xs`, `sm`, `md`, `lg`
- Changed `bsStyle` to `variant`
- Changed `bsSize` to `size`
- Replace `<Navbar.Header>` with `<div className=“navbar-header”>`
- Replace `<Navbar.Form>` with `<div className="navbar-search-form navbar-form navbar-left">`
- Replace `<FormGroup>` with `<Form.Group>`
- Replace `<InputGroup.Addon>` with `<InputGroup.Prepend><InputGroup.Text>` and `<InputGroup.Append><InputGroup.Text>`
- All required images have a default prop at the end now, example: `const us_flag = require("../assets/img/flags/US.png");` was changed to `const us_flag = require("../assets/img/flags/US.png");`
- Rename all .jsx files to .js
- Added Row and Col inside StatsCard
- Delete eventKey from NavDropdown components
- Deleted noCaret from NavDropdown components
- Replace Navbar fluid with Navbar → Container fluid
- Add fontawesome as dependencie instead of font link insde public/index.html, it is now imported insde src/index.js
- In addition to these changes, we’ve chaned the structure of the pages and components as well to match those from the HTML version of the product: https://www.creative-tim.com/product/light-bootstrap-dashboard-pro

## [1.2.0] 2019-05-03

### Bug fixing

- Renamed `src/layouts/Dashboard/Dashboard.jsx` to `src/layouts/Admin.jsx`
- Renamed `src/layouts/Pages/Pages.jsx` to `src/layouts/Auth.jsx`
- Renamed `src/views/Calendar/Calendar.jsx` to `src/views/Calendar.jsx`
- Renamed `src/views/Charts/Charts.jsx` to `src/views/Charts.jsx`
- Renamed `src/views/Dashboard/Dashboard.jsx` to `src/views/Dashboard.jsx`
- Renamed `src/components/Header` to `src/components/Navbars`
- Renamed `src/components/Navbars/Header.jsx` to `src/components/Navbars/AdminNavbar.jsx`
- Renamed `src/components/Navbars/PagesHeader.jsx` to `src/components/Navbars/AuthNavbar.jsx`
- Renamed `src/components/Navbars/HeaderLinks.jsx` to `src/components/Navbars/AdminNavbarLinks.jsx`
- Changes caused by running [the prettier command](https://prettier.io/docs/en/install.html) for _.jsx_, _.js_, _.html_ and _.css_ files
- Changed our buggy routing system, now it should work flawlessly, for more info, please refer to our [live docs here](https://demos.creative-tim.com/light-bootstrap-dashboard-pro-react/#/documentation/routing-system)
- Solved
  - https://github.com/creativetimofficial/ct-light-bootstrap-dashboard-pro-react/issues/37
  - https://github.com/creativetimofficial/ct-light-bootstrap-dashboard-pro-react/issues/35
- Removed `.env` file and replaced it with `jsconfig.json`
- Small bug fixes

### Removed dependencies/components

- Deleted `src/routes/*` folder
- node-sass-chokidar
- npm-run-all

### Added dependencies/components

- Added `src/routes.js` file (instead of the three files from `src/routes/*`)
- @types/markerclustererplus@2.1.33 (to stop install warnings)
- @types/googlemaps@3.30.19 (to stop install warnings)
- @types/react@16.8.15 (to stop install warnings)
- typescript@3.4.5 (to stop install warnings)
- react-router@5.0.0 (react-router-dom auto-installs this package, but it is better to have them both inside package.json)

### Update dependencies

- history 4.7.2 → 4.9.0
- moment 2.21.0 → 2.24.0
- node-sass 4.6.1 → 4.12.0
- nouislider 11.0.3 → 13.1.5
- perfect-scrollbar 1.3.0 → 1.4.0
- react 16.2.0 → 16.8.6
- react-big-calendar 0.19.0 → 0.20.4
- react-bootstrap 0.32.1 → 0.32.4
- react-bootstrap-sweetalert 4.2.3 → 4.4.1
- react-chartist 0.13.1 → 0.13.3
- react-datetime 2.14.0 → 2.16.3
- react-dom 16.2.0 → 16.8.6
- react-jvectormap 0.0.2 → 0.0.9
- react-router-dom 4.2.2 → 5.0.0
- react-scripts 1.1.1 → 3.0.0
- react-select 1.2.1 → 2.4.3
- react-stepzilla 4.7.0 → 6.0.0
- react-syntax-highlighter 7.0.2 → 10.2.1
- react-table 6.8.0 → 6.10.0

## [1.1.1] 2018-05-22

### Bug fixing

- Changed links for live preview, live documentation and issues
- Changed links from `http` to `https`

## [1.1.0] 2018-04-12

### Bug fixing

- Moved all the contents of `elements` folder to `components` folder and delete it
- Renamed `containers` folder to `layouts`
- Renamed `Dash/Dash.jsx` to `Dashboard/Dashboard.jsx`
- Deleted `App/App.jsx` and moved it's contents in `index.js`
- Changed `Pagination` components (changes cause by the upgrade of `react-bootstrap`)
- Changed `Accordion` and `Panel` components (changes cause by the upgrade of `react-bootstrap`)
- Deleted DataTables view and added ReactTables view (scss for dataTable is still in this dashboard)
- Small bug fixes

### Removed dependencies/components

- `react-simple-maps`
- `d3-scale`
- `google-maps-react`
- `datatables.net-bs@1.10.16`
- `datatables.net-responsive@2.2.0`
- `jquery@3.2.1`

### Added dependencies/components

- `react-jvectormap@0.0.2` (instead of `react-simple-maps` and `d3-scale`)
- `react-google-maps@9.4.5` (instead of `google-maps-react`)
- `node-sass@4.6.1` (for compiling scss)
- `bootstrap@3.3.7` (and deleted `src/assets/bootstrap.min.css?v=3.3.5`)
- `react-table@6.8.0` (instead of `datatables.net-bs@1.10.16`, `datatables.net-responsive@2.2.0` and `jquery@3.2.1`)

### Update dependencies

- `react-bootstrap@0.31.3 (bootstrap@3.3.5)` to `react-bootstrap@0.32.1 (bootstrap@3.3.7)`
- `moment@2.18.1` to `moment@2.21.0`
- `nouislider@10.1.0` to `nouislider@11.0.3`
- `npm-run-all@4.1.1` to `npm-run-all@4.1.2`
- `perfect-scrollbar@0.8.1` to `perfect-scrollbar@1.3.0`
- `react@15.6.1` to `react@16.2.0`
- `react-big-calendar@0.16.1` to `react-big-calendar@0.19.0`
- `react-bootstrap-sweetalert@4.0.0` to `react-bootstrap-sweetalert@4.2.3`
- `react-bootstrap-switch@15.5.1` to `react-bootstrap-switch@15.5.3`
- `react-chartist@0.13.0` to `react-chartist@0.13.1`
- `react-datetime@2.10.2` to `react-datetime@2.14.0`
- `react-dom@15.6.1` to `react-dom@16.2.0`
- `react-notification-system@0.2.15` to `react-notification-system@0.2.17`
- `react-router-dom@4.1.2` to `react-router-dom@4.2.2`
- `react-scripts@1.0.10` to `react-scripts@1.1.1`
- `react-select@1.0.0-rc.10` to `react-select@1.2.1`
- `react-stepzilla@4.6.3` to `react-stepzilla@4.7.0`
- `react-syntax-highlighter@5.7.0` to `react-syntax-highlighter@7.0.2`
- `react-tagsinput@3.18.0` to `react-tagsinput@3.19.0`

## [1.0.1] 2017-10-31

### Bug fixing

- Variable `$default-color` was changed from `#888888` to `#444`
- ClassName `.navbar-fixed-top` was replaced with `.navbar-fixed`
- Small bug fixes

## [1.0.0] 2017-10-25

### Original Release

- Added React-Bootstrap as base framework
- Added design from Light Bootstrap Dashboard Pro by Creative Tim
