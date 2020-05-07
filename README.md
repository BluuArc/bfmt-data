# bfmt-data

## Description

Holds extracted data for the game Brave Frontier. Currently heavily based on [this datamine](https://github.com/cheahjs/bravefrontier_data), but it is not an exact copy. The shape of the data found in here can be found in the datamine type definitions in [`bfmt-utilities`](https://github.com/BluuArc/bfmt-utilities/blob/master/docs/modules/_datamine_types_.md).

## Structure

General structure is as follows:

* `[server folder]/`
	* `[data type]/` - typically only `unit` and `item` for most servers; Global also supports `burst`, `dictionary`, `extra-skill`, `leader-skill`, and `missions`
		* `_update-stats.json` - a mini datamine of that data type consisting of the last update time for a given entry and one or two extra properties for needed for basic name/description searching.
		* `_all-entries.json [item only]` - a single file that has all the full entries for the given data type; only applies to the `item` data type at the time of writing.
		* `_all-entries-[1-6].json [unit only]` - set of files that when combined have all the full entries for the given data type; only applies to the `unit` data type at the time of writing.
		* `[id].json` - The full entry of a given ID for the given data type. For example, `10011.json` would be the full entry of 2\* Vargas.
* `server-urls.json` - JSON file containing the CDN URLs
