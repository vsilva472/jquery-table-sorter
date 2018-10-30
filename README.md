# jQuery Table Sorter
jQuery Table Sorter is a simple easy to use plugin to sorte tables by columns.
See [DEMO](http://vsilva472.github.io/jquery-table-sorter) in action.

## Basic usage
* Add jquery table sorter file to your page **after jquery core**:
```
    <script src="path_to_jquery/jquery.min.js"></script>
    <script src="path_to_plugin/jquery-table-sorter.js"></script>
 ```
2. After import jquery table sorter just call the plugin api:
 ```
    /**
     * This will make all tables sortable by it headers (th)
     */
    <script type="text/javascript">
        (function ( $ ) {
            $( 'table' ).TableSorter();
        } ( jQuery ));
    </script>
 ```
 ## Default options
 The default pluigin options are:
  ```
    <script type="text/javascript">
        (function ( $ ) {
            // this is the same of $( 'table' ).TableSorter();
            $( 'table' ).TableSorter({
		        columns		: 'th',
		        icon_class	: 'ts-sort-indicator',
		        arrows		: { 
		            up : '&#x25B4;', 
		            down : '&#x25BE;' 
		        }
            });
        } ( jQuery ));
    </script>
 ```
 
### Specifying columns to be sortable
jQuery Table Sorter plugin can make be configured to make some (not all) columns sortable, just pass the column(s) selector to plugin.
 ```
    /**
     * This will make all tables sortable by it headers only columns with the class '.sortable' sortable.
     */
    <script type="text/javascript">
        (function ( $ ) {
            $( 'table' ).TableSorter({
                columns: '.sortable'
            });
        } ( jQuery ));
    </script>
 ```
 ### Changing sort icon indicator
 You can tell to jQuery Table Sorter plugin wich sort icon you like to use, just pass the `arrows` param on the plugin call.
 with html code. See example:
 ```
    /**
     * Changing sort indicator icon
     * To double arrows
     */
    <script type="text/javascript">
        (function ( $ ) {
            $( 'table' ).TableSorter({
                arrows: { 
                    up:  '&uArr;', 
                    down: '&dArr;' 
                }
            });
        } ( jQuery ));
    </script>
 ```
 ### Changing sorting icon css class
 By default this plugin wraps sort indicator icon with a `<span></span>` with css class `ts-sort-indicator`.
 To change default css class just pass the option `icon_class` to the plugin call. See example:
 ```
    /**
     * Changing sort indicator css clas
     */
    <script type="text/javascript">
        (function ( $ ) {
            $( 'table' ).TableSorter({
                icon_class: 'my-icon-css-class'
            });
        } ( jQuery ));
    </script>
 ```
 
 ### Multiple instance in one page
 You can have multiple call of this plugin in one page with diferents configuratios. See Examples:
 ```
    <script type="text/javascript">
        (function ( $ ) {
            // all columns are sortable
            $( '#mytable1' ).TableSorter();
            
            // second column is now sortable
            $( '#mytable2' ).TableSorter({ columns: '.sortable' });
            
            // all columns are sortable with custom sort indicator
            $( '#mytable3' ).TableSorter(
                arrows: { 
                    up:  '&uArr;', 
                    down: '&dArr;' 
                }
            });
        } ( jQuery ));
    </script>
 ```
 
 ### Changelog

1.0.0 - 2018-10-30
* Commit Inicial
 
 #### License
 MIT

