---
title: SchemaEnum (référence de base de données de bureau Access)
TOCTitle: SchemaEnum
ms:assetid: 6147b682-3c4f-ea91-fff6-ac73107d206d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249359(v=office.15)
ms:contentKeyID: 48545208
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: aa70f275de164716b5b3975b56588e9dc4aec1a5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32308862"
---
# <a name="schemaenum"></a>SchemaEnum

**S’applique à** : Access 2013, Office 2013

Spécifie le type de **Recordset** de schéma extrait par la méthode [OpenSchema](openschema-method-ado.md).

## <a name="remarks"></a>Remarques

D'autres informations sur la fonction et les colonnes renvoyées pour chaque constante ADO sont présentes dans les rubriques de l'Annexe B du manuel *OLE DB Programmers Reference*. Le nom de chaque rubrique est mentionné entre parenthèses dans la section Description du tableau suivant.

D'autres informations sur la fonction et les colonnes renvoyées pour chaque constante ADO MD sont présentes dans les rubriques du chapitre 23 du manuel *OLE DB Programmers Reference*. Le nom de chaque rubrique est indiqué entre parenthèses et marqué d'un astérisque (\*) dans la colonne Description du tableau suivant.

Convertissez les types de données des colonnes de la documentation OLE DB en types de données ADO en vous reportant à la colonne de la rubrique [DataTypeEnum](datatypeenum.md) ADO. Par exemple, un type de données OLE DB **de\_DbType WSTR** équivaut à un type de données ADO **adWChar**.

ADO génère des résultats de type schéma pour les constantes **adSchemaDBInfoKeywords** et **adSchemaDBInfoLiterals**. ADO crée un **objet Recordset**, puis remplit chaque ligne avec les valeurs renvoyées par les méthodes **IDBInfo:: GetKeywords** et **IDBInfo:: GetLiteralInfo** . Vous trouverez des informations supplémentaires sur ces méthodes dans la section IDBInfo du *Guide OLE DB Programmer's Reference*(en anglais).

<br/>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Constante</p></th>
<th><p>Valeur</p></th>
<th><p>Description</p></th>
<th><p>Colonnes de contrainte</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>adSchemaAsserts</strong></p></td>
<td><p>0</p></td>
<td><p>Renvoie les assertions définies dans le catalogue et dont est propriétaire un utilisateur donné. (ASSERTIONS Rowset)</p></td>
<td><p>CONSTRAINT_CATALOG<br />
CONSTRAINT_SCHEMA<br />
CONSTRAINT_NAME</p></td>
</tr>
<tr class="even">
<td><p><strong>adSchemaCatalogs</strong></p></td>
<td><p>0,1</p></td>
<td><p>Renvoie les attributs physiques associés aux catalogues accessibles depuis le DBMS. (CATALOGS Rowset)</p></td>
<td><p>CATALOG_NAME</p></td>
</tr>
<tr class="odd">
<td><p><strong>adSchemaCharacterSets</strong></p></td>
<td><p>n°2</p></td>
<td><p>Renvoie les jeux de caractères définis dans le catalogue et accessibles par un utilisateur donné. (CHARACTER_SETS Rowset)</p></td>
<td><p>CHARACTER_SET_CATALOG<br />
CHARACTER_SET_SCHEMA<br />
CHARACTER_SET_NAME</p></td>
</tr>
<tr class="even">
<td><p><strong>adSchemaCheckConstraints</strong></p></td>
<td><p>disque</p></td>
<td><p>Renvoie les contraintes de contrôle définies dans le catalogue et dont est propriétaire un utilisateur donné. (CHECK_CONSTRAINTS Rowset)</p></td>
<td><p>CONSTRAINT_CATALOG<br />
CONSTRAINT_SCHEMA<br />
CONSTRAINT_NAME</p></td>
</tr>
<tr class="odd">
<td><p><strong>adSchemaCollations</strong></p></td>
<td><p>3</p></td>
<td><p>Renvoie les collations de caractères définies dans le catalogue et accessibles par un utilisateur donné. (COLLATIONS Rowset)</p></td>
<td><p>COLLATION_CATALOG<br />
COLLATION_SCHEMA<br />
COLLATION_NAME</p></td>
</tr>
<tr class="even">
<td><p><strong>adSchemaColumnPrivileges</strong></p></td>
<td><p>kg</p></td>
<td><p>Renvoie les privilèges des colonnes des tables définies dans le catalogue,  accordés à un utilisateur donné, ou accordés par ce dernier. (COLUMN_PRIVILEGES Rowset)</p></td>
<td><p>TABLE_CATALOG<br />
TABLE_SCHEMA<br />
NOM_DE_TABLE<br />
COMPORTE<br />
ACCORDEROU<br />
BÉNÉFICIAIRE</p></td>
</tr>
<tr class="odd">
<td><p><strong>adSchemaColumns</strong></p></td>
<td><p>4</p></td>
<td><p>Renvoie les colonnes des tables (vues comprises) définies dans le catalogue et accessibles à un utilisateur donné. (COLUMNS Rowset)</p></td>
<td><p>TABLE_CATALOG<br />
TABLE_SCHEMA<br />
NOM_DE_TABLE<br />
COMPORTE</p></td>
</tr>
<tr class="even">
<td><p><strong>adSchemaColumnsDomainUsage</strong></p></td>
<td><p>a4</p></td>
<td><p>Renvoie les colonnes définies dans le catalogue et qui dépendent d'un domaine défini dans le catalogue et dont est propriétaire un utilisateur donné. (COLUMN_DOMAIN_USAGE Rowset)</p></td>
<td><p>DOMAIN_CATALOG<br />
DOMAIN_SCHEMA<br />
NOM_DOMAINE<br />
COMPORTE</p></td>
</tr>
<tr class="odd">
<td><p><strong>adSchemaConstraintColumnUsage</strong></p></td>
<td><p>6.x</p></td>
<td><p>Renvoie les colonnes utilisées par les contraintes référentielles, uniques et de contrôle, ainsi que par les assertions définies dans le catalogue et dont est propriétaire un utilisateur donné. (CONSTRAINT_COLUMN_USAGE Rowset)</p></td>
<td><p>TABLE_CATALOG<br />
TABLE_SCHEMA<br />
NOM_DE_TABLE<br />
COMPORTE</p></td>
</tr>
<tr class="even">
<td><p><strong>adSchemaConstraintTableUsage</strong></p></td>
<td><p>7j/7</p></td>
<td><p>Renvoie les tables utilisées par les contraintes référentielles, uniques et de contrôle, ainsi que par les assertions définies dans le catalogue et dont est propriétaire un utilisateur donné. (CONSTRAINT_TABLE_USAGE Rowset)</p></td>
<td><p>TABLE_CATALOG<br />
TABLE_SCHEMA<br />
NOM_DE_TABLE</p></td>
</tr>
<tr class="odd">
<td><p><strong>adSchemaCubes</strong></p></td>
<td><p>32</p></td>
<td><p>Renvoie des informations sur les cubes disponibles dans un schéma (ou catalogue, si le fournisseur ne prend pas en charge les schémas). (CUBES Rowset*)</p></td>
<td><p>CATALOG_NAME<br />
SCHEMA_NAME<br />
CUBE_NAME</p></td>
</tr>
<tr class="even">
<td><p><strong>adSchemaDBInfoKeywords</strong></p></td>
<td><p>0,30</p></td>
<td><p>Renvoie la liste des mots réservés spécifiques aux fournisseur. (IDBInfo:: GetKeywords *)</p></td>
<td><p>&lt;Nul&gt;</p></td>
</tr>
<tr class="odd">
<td><p><strong>adSchemaDBInfoLiterals</strong></p></td>
<td><p>31</p></td>
<td><p>Renvoie la liste des chaînes littérales spécifiques aux fournisseurs et utilisées dans les commandes texte. (IDBInfo:: GetLiteralInfo *)</p></td>
<td><p>&lt;Nul&gt;</p></td>
</tr>
<tr class="even">
<td><p><strong>adSchemaDimensions</strong></p></td>
<td><p>33</p></td>
<td><p>Renvoie des informations sur les dimensions d'un cube donné. Chaque dimension possède sa ligne propre. (DIMENSIONS Rowset *)</p></td>
<td><p>CATALOG_NAME<br />
SCHEMA_NAME<br />
CUBE_NAME<br />
DIMENSION_NAME<br />
DIMENSION_UNIQUE_NAME</p></td>
</tr>
<tr class="odd">
<td><p><strong>adSchemaForeignKeys</strong></p></td>
<td><p>vingt</p></td>
<td><p>Renvoie les colonnes de clés étrangères définies dans le catalogue par un utilisateur donné. (FOREIGN_KEYS Rowset)</p></td>
<td><p>PK_TABLE_CATALOG<br />
PK_TABLE_SCHEMA<br />
PK_TABLE_NAME<br />
FK_TABLE_CATALOG<br />
FK_TABLE_SCHEMA<br />
FK_TABLE_NAME</p></td>
</tr>
<tr class="even">
<td><p><strong>adSchemaHierarchies</strong></p></td>
<td><p>34</p></td>
<td><p>Renvoie des informations sur les hiérarchies disponibles dans une dimension. (HIERARCHIES Rowset *)</p></td>
<td><p>CATALOG_NAME<br />
SCHEMA_NAME<br />
CUBE_NAME<br />
DIMENSION_UNIQUE_NAME<br />
HIERARCHY_NAME<br />
HIERARCHY_UNIQUE_NAME</p></td>
</tr>
<tr class="odd">
<td><p><strong>adSchemaIndexes</strong></p></td>
<td><p>an</p></td>
<td><p>Renvoie les index définis dans le catalogue et dont est propriétaire un utilisateur donné. (INDEXES Rowset)</p></td>
<td><p>TABLE_CATALOG<br />
TABLE_SCHEMA<br />
INDEX_NAME<br />
ENTRER<br />
NOM_DE_TABLE</p></td>
</tr>
<tr class="even">
<td><p><strong>adSchemaKeyColumnUsage</strong></p></td>
<td><p>8bits</p></td>
<td><p>Renvoie les colonnes définies dans le catalogue et qui sont contraintes sous forme de clés par un utilisateur donné. (KEY_COLUMN_USAGE Rowset)</p></td>
<td><p>CONSTRAINT_CATALOG<br />
CONSTRAINT_SCHEMA<br />
CONSTRAINT_NAME<br />
TABLE_CATALOG<br />
TABLE_SCHEMA<br />
NOM_DE_TABLE<br />
COMPORTE</p></td>
</tr>
<tr class="odd">
<td><p><strong>adSchemaLevels</strong></p></td>
<td><p>35</p></td>
<td><p>Renvoie des informations sur les niveaux disponibles dans une dimension. (LEVELS Rowset*)</p></td>
<td><p>CATALOG_NAME<br />
SCHEMA_NAME<br />
CUBE_NAME<br />
DIMENSION_UNIQUE_NAME<br />
HIERARCHY_UNIQUE_NAME<br />
LEVEL_NAME<br />
LEVEL_UNIQUE_NAME</p></td>
</tr>
<tr class="even">
<td><p><strong>adSchemaMeasures</strong></p></td>
<td><p>36</p></td>
<td><p>Renvoie des informations sur les mesures disponibles. (MEASURES Rowset *)</p></td>
<td><p>CATALOG_NAME<br />
SCHEMA_NAME<br />
CUBE_NAME<br />
MEASURE_NAME<br />
MEASURE_UNIQUE_NAME</p></td>
</tr>
<tr class="odd">
<td><p><strong>adSchemaMembers</strong></p></td>
<td><p>38</p></td>
<td><p>Renvoie des informations sur les membres disponibles. (MEMBERS Rowset *)</p></td>
<td><p>CATALOG_NAME<br />
SCHEMA_NAME<br />
CUBE_NAME<br />
DIMENSION_UNIQUE_NAME<br />
HIERARCHY_UNIQUE_NAME<br />
LEVEL_UNIQUE_NAME<br />
LEVEL_NUMBER<br />
MEMBER_NAME<br />
MEMBER_UNIQUE_NAME<br />
MEMBER_CAPTION<br />
MEMBER_TYPE<br />
Opérateur d'arborescence (pour plus d'informations, reportez-vous à la documentation OLE DB pour OLAP.)</p></td>
</tr>
<tr class="even">
<td><p><strong>adSchemaPrimaryKeys</strong></p></td>
<td><p>vingt</p></td>
<td><p>Renvoie les colonnes de clés primaires définies dans le catalogue par un utilisateur donné. (PRIMARY_KEYS Rowset)</p></td>
<td><p>PK_TABLE_CATALOG<br />
PK_TABLE_SCHEMA<br />
PK_TABLE_NAME</p></td>
</tr>
<tr class="odd">
<td><p><strong>adSchemaProcedureColumns</strong></p></td>
<td><p>29</p></td>
<td><p>Renvoie des informations sur les colonnes de jeux de lignes renvoyées par des procédures. (PROCEDURE_COLUMNS Rowset)</p></td>
<td><p>PROCEDURE_CATALOG<br />
PROCEDURE_SCHEMA<br />
PROCEDURE_NAME<br />
COMPORTE</p></td>
</tr>
<tr class="even">
<td><p><strong>adSchemaProcedureParameters</strong></p></td>
<td><p>27</p></td>
<td><p>Renvoie des informations sur les paramètres et les codes de retour des procédures. (PROCEDURE_PARAMETERS Rowset)</p></td>
<td><p>PROCEDURE_CATALOG<br />
PROCEDURE_SCHEMA<br />
PROCEDURE_NAME<br />
NOM_DE_PARAMÈTRE</p></td>
</tr>
<tr class="odd">
<td><p><strong>adSchemaProcedures</strong></p></td>
<td><p>Seiz</p></td>
<td><p>Renvoie les procédures définies dans le catalogue et dont est propriétaire un utilisateur donné. (PROCEDURES Rowset)</p></td>
<td><p>PROCEDURE_CATALOG<br />
PROCEDURE_SCHEMA<br />
PROCEDURE_NAME<br />
PROCEDURE_TYPE</p></td>
</tr>
<tr class="even">
<td><p><strong>adSchemaProperties</strong></p></td>
<td><p>37</p></td>
<td><p>Renvoie des informations sur les propriétés disponibles pour chaque niveau de la dimension. (PROPERTIES Rowset *)</p></td>
<td><p>CATALOG_NAME<br />
SCHEMA_NAME<br />
CUBE_NAME<br />
DIMENSION_UNIQUE_NAME<br />
HIERARCHY_UNIQUE_NAME<br />
LEVEL_UNIQUE_NAME<br />
MEMBER_UNIQUE_NAME<br />
PROPERTY_TYPE<br />
PROPERTY_NAME</p></td>
</tr>
<tr class="odd">
<td><p><strong>adSchemaProviderSpecific</strong></p></td>
<td><p>-1</p></td>
<td><p>Utilisé si le fournisseur définit ses propres requêtes de schéma non standard.</p></td>
<td><p>&lt;Spécifique au fournisseur&gt;</p></td>
</tr>
<tr class="even">
<td><p><strong>adSchemaProviderTypes</strong></p></td>
<td><p>22,5</p></td>
<td><p>Renvoie les types de données (primaires) pris en charge par le fournisseur de données. (PROVIDER_TYPES Rowset)</p></td>
<td><p>TYPE_DE_DONNÉES<br />
BEST_MATCH</p></td>
</tr>
<tr class="odd">
<td><p><strong>AdSchemaReferentialConstraints</strong></p></td>
<td><p>4,9</p></td>
<td><p>Renvoie les contraintes référentielles définies dans le catalogie et dont est propriétaire un utilisateur donné. (REFERENTIAL_CONSTRAINTS Rowset)</p></td>
<td><p>CONSTRAINT_CATALOG<br />
CONSTRAINT_SCHEMA<br />
CONSTRAINT_NAME</p></td>
</tr>
<tr class="even">
<td><p><strong>adSchemaSchemata</strong></p></td>
<td><p>cm</p></td>
<td><p>Renvoie les schémas (objets de la base de données) dont est propriétaire un utilisateur donné. (SCHEMATA Rowset)</p></td>
<td><p>CATALOG_NAME<br />
SCHEMA_NAME<br />
SCHEMA_OWNER</p></td>
</tr>
<tr class="odd">
<td><p><strong>adSchemaSQLLanguages</strong></p></td>
<td><p>18</p></td>
<td><p>Renvoie les niveaux de conformité, les options et les dialectes pris en charge par les données de traitement d'implémentation SQL définies dans le catalogue. (SQL_LANGUAGES Rowset)</p></td>
<td><p>&lt;Nul&gt;</p></td>
</tr>
<tr class="even">
<td><p><strong>adSchemaStatistics</strong></p></td>
<td><p>neuf</p></td>
<td><p>Renvoie les statistiques définies dans le catalogue et dont est propriétaire un utilisateur donné. (STATISTICS Rowset)</p></td>
<td><p>TABLE_CATALOG<br />
TABLE_SCHEMA<br />
NOM_DE_TABLE</p></td>
</tr>
<tr class="odd">
<td><p><strong>adSchemaTableConstraints</strong></p></td>
<td><p>10</p></td>
<td><p>Renvoie les contraintes de table définies dans le catalogue et dont est propriétaire un utilisateur donné. (TABLE_CONSTRAINTS Rowset)</p></td>
<td><p>CONSTRAINT_CATALOG<br />
CONSTRAINT_SCHEMA<br />
CONSTRAINT_NAME<br />
TABLE_CATALOG<br />
TABLE_SCHEMA<br />
NOM_DE_TABLE<br />
CONSTRAINT_TYPE</p></td>
</tr>
<tr class="even">
<td><p><strong>adSchemaTablePrivileges</strong></p></td>
<td><p>13</p></td>
<td><p>Renvoie les privilèges sur les tables définies dans le catalogue et qui sont disponibles pour un utilisateur donné, ou accordés par ce dernier. (TABLE_PRIVILEGES Rowset)</p></td>
<td><p>TABLE_CATALOG<br />
TABLE_SCHEMA<br />
NOM_DE_TABLE<br />
ACCORDEROU<br />
BÉNÉFICIAIRE</p></td>
</tr>
<tr class="odd">
<td><p><strong>adSchemaTables</strong></p></td>
<td><p>vingtaine</p></td>
<td><p>Renvoie les tables (notamment les vues) définies dans le catalogue et accessibles par un utilisateur donné. (TABLES Rowset)</p></td>
<td><p>TABLE_CATALOG<br />
TABLE_SCHEMA<br />
NOM_DE_TABLE<br />
TABLE_TYPE</p></td>
</tr>
<tr class="even">
<td><p><strong>adSchemaTranslations</strong></p></td>
<td><p>21</p></td>
<td><p>Renvoie les conversions de caractères définies dans le catalogue et auxquelles un utilisateur donné a accès. (TRANSLATIONS Rowset)</p></td>
<td><p>TRANSLATION_CATALOG<br />
TRANSLATION_SCHEMA<br />
TRANSLATION_NAME</p></td>
</tr>
<tr class="odd">
<td><p><strong>adSchemaTrustees</strong></p></td>
<td><p>39</p></td>
<td><p>Réservé pour usage ultérieur.</p></td>
<td><p><br />
</p></td>
</tr>
<tr class="even">
<td><p><strong>adSchemaUsagePrivileges</strong></p></td>
<td><p>0,15</p></td>
<td><p>Renvoie les privilèges USAGE sur les objets définis dans le catalogue et qui sont disponibles pour un utilisateur donné, ou accordés par ce dernier. (USAGE_PRIVILEGES Rowset)</p></td>
<td><p>OBJECT_CATALOG<br />
OBJECT_SCHEMA<br />
OBJECT_NAME<br />
TYPE_OBJET<br />
ACCORDEROU<br />
BÉNÉFICIAIRE</p></td>
</tr>
<tr class="odd">
<td><p><strong>adSchemaViewColumnUsage</strong></p></td>
<td><p>heures/24</p></td>
<td><p>Renvoie les colonnes desquelles dépendent les tables vues, définies dans le catalogue et dont est propriétaire un utilisateur donné. (VIEW_COLUMN_USAGE Rowset)</p></td>
<td><p>VIEW_CATALOG<br />
VIEW_SCHEMA<br />
NOM_DE_VUE</p></td>
</tr>
<tr class="even">
<td><p><strong>adSchemaViews</strong></p></td>
<td><p>23</p></td>
<td><p>Renvoie les vues définies dans le catalogue et accessibles par un utilisateur donné. (VIEWS Rowset)</p></td>
<td><p>TABLE_CATALOG<br />
TABLE_SCHEMA<br />
NOM_DE_TABLE</p></td>
</tr>
<tr class="odd">
<td><p><strong>adSchemaViewTableUsage</strong></p></td>
<td><p>25</p></td>
<td><p>Renvoie les tables desquelles dépendent les tables vues, définies dans le catalogue et dont est propriétaire un utilisateur donné. (VIEW_TABLE_USAGE Rowset)</p></td>
<td><p>VIEW_CATALOG<br />
VIEW_SCHEMA<br />
NOM_DE_VUE</p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a>Équivalent ADO/WFC

Module : **com.ms.wfc.data**

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Constante</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>AdoEnums. Schema. asSERTs</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums. Schema. CATALOGs</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums. Schema. CHARACTERSETS</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums. Schema. CHECKCONSTRAINTS</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums. Schema. COLLATIONs</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums. Schema. COLUMNPRIVILEGES</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums. Schema. COLUMNs</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums. Schema. COLUMNSDOMAINUSAGE</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums. Schema. CONSTRAINTCOLUMNUSAGE</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums. Schema. CONSTRAINTTABLEUSAGE</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums. Schema. CUBEs</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums. Schema. DBINFOKEYWORDS</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums. Schema. DBINFOLITERALS</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums. Schema. DIMENSIONS</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums. Schema. FOREIGNKEYS</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums. Schema. HIERARCHIES</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums. Schema. INDEXes</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums. Schema. KEYCOLUMNUSAGE</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums. Schema. LEVELs</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums. Schema. MEASURes</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums. Schema. MEMBERs</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums. Schema. PRIMARYKEYS</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums. Schema. PROCEDURECOLUMNS</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums. Schema. PROCEDUREPARAMETERS</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums. Schema. PROCEDUREs</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums. Schema. PROPERTIES</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums. Schema. PROVIDERSPECIFIC</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums. Schema. PROVIDERTYPES</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums. Schema. REFERENTIALCONTRAINTS</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums. Schema. SCHEMATA</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums. Schema. SQLLANGUAGES</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums. Schema. STATISTICs</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums. Schema. TABLECONSTRAINTS</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums. Schema. TABLEPRIVILEGES</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums. Schema. TABLES</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums. Schema. TRANSLATIONs</p></td>
</tr>
<tr class="odd">
<td><p>Énumération AdoEnums. Schema. TRUSTed</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums. Schema. USAGEPRIVILEGES</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums. Schema. VIEWCOLUMNUSAGE</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums. Schema. VIEWS</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums. Schema. VIEWTABLEUSAGE</p></td>
</tr>
</tbody>
</table>

