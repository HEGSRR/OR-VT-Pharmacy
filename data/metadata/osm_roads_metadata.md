- `Title`: OpenStreetMap Roads for Vermont and Surroundings
- `Abstract`: This is a graph data structure representing roads and streets in Vermont and surrounding areas. The data is derived from OpenStreetMap via the Overpass API and OSMnx python package.
- `Spatial Coverage`: The state of Vermont and a 64373.8 meter (40 mile) buffer around the state.
- `Spatial Resolution`: The spatial resolution varies by region and feature. Distances are calculated with the full spatial resolution of the dataset, but the graph model is simplified to vertices at intersections and dead ends only.
- `Spatial Reference System`: WGS 1984 geographic coordinate system (EPSG:4326)
- `Temporal Coverage`: Data was queried on 24-1-2024
- `Temporal Resolution`: Data represents a snapshot of the OpenStreetMap database at a moment in time. Data currency varies by region and feature, depending on how recently any OpenStreetMap users have digitized or updated the map.
- `Lineage`: See code for creation at procedure/code/00_road_network.ipynb. OpenStreetMap data is volunteered by users, and lineage varies on a feature-by-feature basis. OSMnx software version 1.8.1 was used to query the data from OpenStreetMap using the Overpass API with the query `ox.graph_from_place('Vermont', network_type='drive', buffer_dist=64373.8)`. By default, this saves data in the WGS 1984 geographic coordinate system (EPSG:4326), calculates the distance of all lines, and simplifies the road network by combining road segments between intersections into a single edge. The road network is then saved as a NetworkX graph data structure in a .graphml file.
- `Distribution`: This graph dataset is stored on OSF at https://osf.io/n2q73 while the original data is stored on OpenStreetMap and distributed via the Overpass API <https://wiki.openstreetmap.org/wiki/Overpass_API>
- `Constraints`: The graph dataset is published with a BSD 3-Clause license, while the original OpenStreetMap data is published with the Open Data Commons Open Database License (<https://opendatacommons.org/licenses/odbl/>). The data is (c) OpenStreetMap Contributors, and this copyright and license information must be attached to any public uses or distributions of the data.
- `Data Quality`: Data has been checked for speed attribute completeness. Routing errors and resulting service areas calculated on the graph from hospitals were checked for topological errors and consistency, resulting in discovery of four erroneous "dead-ends" where one-way access roads terminated in parking areas. These four dead-end nodes are removed from the analysis code so that routes start on the correct one-way exit from parking areas.
- `Variables`:


| Label | Alias | Definition | Type | Accuracy | Domain | Missing Data Value(s) | Missing Data Frequency |
| :--: | :--: | :--: | :--: | :--: | :--: | :--: | :--: |
| osmid | osmid | unique OpenStreetMap identifier | long integer | n/a | n/a | none | none |
| highway | highway | highway key from OpenStreetMap with values indicating highway type | text | unknown | residential, tertiary, secondary, primary, unclassified, trunk, etc. See <https://wiki.openstreetmap.org/wiki/Key:highway> | no value recorded | 194,089 of 577,399 edges missing highway type |
| oneway | oneway | road is for one-way travel only | text representing boolean | unknown | {true, false} | n/a | n/a |
| reversed | reversed | road direction is opposite the sequence of coordinates | text representing boolean | unknown | {true, false} | n/a | n/a |
| length | length | length in meters | decimal | geodesic calculation with epsg 4326 | unknown | n/a | none |
| maxspeed | maximum speed limit | maximum speed limit (assumed kph unless other units are written) | text composed of an integer, integer with speed limit, or list of speeds | unknown | one  | no value recorded | 411,768 of 577,399 edges missing speed limit
 |
