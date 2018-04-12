# Change Log

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
