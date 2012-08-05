
### CARTA DE DATOS
ttlp_mt_local_file( './ttl-gen/configEverest.xml.ttl', '', 'http://data.bci.cl/configEverest.xml' );
rdf_obj_ft_rule_add(null, null, 'All');
vt_inc_index_db_dba_rdf_obj();
urilbl_ac_init_db();
registry_set('fct_desc_value_labels', '1');

#### CONSULTAS
prefix v: <http://linktegration.com/v/wls81/>
prefix rdfs: <http://www.w3.org/2000/01/rdf-schema#>
select
   ?component_label
   ?domain_label
where {
   ?component
     v:hasJNDIName 'wcorp.jms.alertas.AlertasSMS9' ;
     v:hasDomain [ rdfs:label ?domain_label ] ;
     rdfs:label ?component_label
} limit 1

sparql select count(*) from <http://data.bci.cl/configEverest.xml> where { ?s ?p ?o } ;
sparql select * from <http://data.bci.cl/configEverest.xml> where { ?s ?p ?o } ;