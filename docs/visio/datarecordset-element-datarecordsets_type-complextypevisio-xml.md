---
title: Élément DataRecordSet (DataRecordSets_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: aa182f04-0899-ee0e-79e1-b74832933e83
description: Stocke, met en forme, actualise et expose dans Microsoft Visio les données qui ont fait l’objet d’une requête dans une base de données.
ms.openlocfilehash: 99f59e9c58f23f40ba18adc2928651b3115a763b
ms.sourcegitcommit: f8dc13ccaadfbd6d3783c3b291d998d5255a5f38
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2022
ms.locfileid: "63404937"
---
# <a name="datarecordset-element-datarecordsets_type-complextype-visio-xml"></a>Élément DataRecordSet (DataRecordSets_Type complexType) (Visio XML)

Stocke, met en forme, actualise et expose dans Microsoft Visio les données qui ont fait l’objet d’une requête dans une base de données.
  
## <a name="element-information"></a>Informations sur l'élément

||Valeur |
|:-----|:-----|
|**Type d’élément** <br/> |[DataRecordSet_Type](datarecordset_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Fichier de schéma** <br/> |VisioSchema15.xsd  <br/> |
|**Composants de document** <br/> |recordsets.xml  <br/> |
   
## <a name="definition"></a>Définition

```XML
< xs:element name="DataRecordSet" type="DataRecordSet_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Éléments et attributs

Si le schéma définit des exigences spécifiques, telles que **séquence**, **minOccurs**, **maxOccurs** et **choix**, consultez la section définition. 
  
### <a name="parent-elements"></a>Éléments parents

|**Élément**|**Type**|**Description**|
|:-----|:-----|:-----|
|[DataRecordSets](datarecordsets-elementvisio-xml.md) <br/> |[DataRecordSets_Type](datarecordsets_type-complextypevisio-xml.md) <br/> |Contient tous les **éléments DataRecordset** du document. |
   
### <a name="child-elements"></a>Éléments enfants

|**Élément**|**Type**|**Description**|
|:-----|:-----|:-----|
|[ADOData](autolinkcomparison-element-datarecordset_type-complextypevisio-xml.md) <br/> |[ADOData_Type](autolinkcomparison_type-complextypevisio-xml.md) <br/> |Contient du XML conforme au schéma XML classique ADO pour un jeu d’enregistrements ADO et qui décrit les données du jeu d’enregistrements de données. |
|[AutoLinkComparison](autolinkcomparison-element-datarecordset_type-complextypevisio-xml.md) <br/> |[AutoLinkComparison_Type](autolinkcomparison_type-complextypevisio-xml.md) <br/> |Définit une règle qui compare une colonne de l’élément **DataRecordset** parent à un élément de données de forme de la dernière action de liaison automatique réussie effectuée dans l’interface utilisateur. |
|[DataColumn](datacolumns-element-datarecordset_type-complextypevisio-xml.md) <br/> |[DataColumns_Type](datacolumns_type-complextypevisio-xml.md) <br/> |Définit l’apparition d’une colonne de  données dans la fenêtre Données externes de l’interface utilisateur Visio et qualifie les données de la colonne en définissant son type de données et sa mise en forme. |
|[DataColumns](datacolumns-element-datarecordset_type-complextypevisio-xml.md) <br/> |[DataColumns_Type](datacolumns_type-complextypevisio-xml.md) <br/> |Contient tous les **éléments DataColumn** d’un ensemble d’enregistrements de données. |
|[PrimaryKey](primarykey-element-datarecordset_type-complextypevisio-xml.md) <br/> |[PrimaryKey_Type](primarykey_type-complextypevisio-xml.md) <br/> |Identifie une ou plusieurs colonnes de clé primaire dans le recordset de données. |
|[RefreshConflict](refreshconflict-element-datarecordset_type-complextypevisio-xml.md) <br/> |[RefreshConflict_Type](refreshconflict_type-complextypevisio-xml.md) <br/> |Indique une ligne du recordset de données liée à une forme en conflit après l’actualisation du recordset de données. |
|[RowMap](rowmap-element-datarecordset_type-complextypevisio-xml.md) <br/> |[RowMap_Type](rowmap_type-complextypevisio-xml.md) <br/> |Cartes ligne d’un recordset de données à une forme. |
   
### <a name="attributes"></a>Attributs

|**Attribut**|**Type**|**Obligatoire**|**Description**|**Valeurs possibles**|
|:-----|:-----|:-----|:-----|:-----|
|Somme de contrôle  <br/> |xsd:unsignedInt  <br/> |facultatif  <br/> |Valeur de la base de contrôle, générée par Visio, et basée sur les propriétés du data-recordset. Définissez cette attirbute sur 0 ; Visio recalcule cette valeur au moment de l’runtime. |Valeurs du type xsd:unsignedInt. |
|Commande  <br/> |xsd:string  <br/> |facultatif  <br/> |Chaîne de commande utilisée pour interroger des données à partir de la source de données. |Valeurs du type xsd:string. |
|ConnectionID  <br/> |xsd:unsignedInt  <br/> |facultatif  <br/> |ID de connexion de **l’objet DataConnection** associé. N’existe pas pour les sources de données XML. |Valeurs du type xsd:unsignedInt. |
|ID  <br/> |xsd:unsignedInt  <br/> |obligatoire  <br/> |ID du recordset de données, unique dans le document. |Valeurs du type xsd:unsignedInt. |
|Nom  <br/> |xsd:string  <br/> |facultatif  <br/> |Nom d’affichage (ou « convivial ») du recordset de données. |Valeurs du type xsd:string. |
|NextRowID  <br/> |xsd:unsignedInt  <br/> |facultatif  <br/> |L’ID Visio ligne suivant. |Valeurs du type xsd:unsignedInt. |
|Options  <br/> |xsd:unsignedInt  <br/> |facultatif  <br/> |Options à appliquer au recordset de données. Les valeurs possibles peuvent être n’importe quelle combinaison d’une ou de plusieurs de celles indiquées dans le tableau suivant. |Valeurs du type xsd:unsignedInt. |
|RefreshInterval  <br/> |xsd:unsignedInt  <br/> |facultatif  <br/> |Fréquence (en minutes) Visio le jeu d’enregistrements de données automatiquement. Cette valeur doit être supérieure ou supérieure à 1. |Valeurs du type xsd:unsignedInt. |
|RefreshNoRecontermtionUI  <br/> |xsd:boolean  <br/> |facultatif  <br/> |Indique si l’interface utilisateur de rapprochement des données doit être désactivée. True (1) pour désactiver l’interface utilisateur. False (0) pour activer l’interface utilisateur. |Valeurs du type xsd:boolean. |
|RefreshOverwriteAll  <br/> |xsd:boolean  <br/> |facultatif  <br/> |Indique s’il faut modifier les modifications apportées par l’utilisateur aux éléments de données de forme dans les formes liées aux données lors de l’actualisation du recordset de données. |Valeurs du type xsd:boolean. |
|ReplaceLinks  <br/> |xsd:unsignedInt  <br/> |facultatif  <br/> |Définit la façon dont les liaisons de données de forme sont traitées lorsque les formes sont copiées ou coupées. 1 pour remplacer les liens existants dans la forme cible. 0 pour conserver les liaisons existantes dans la forme cible. |Valeurs du type xsd:unsignedInt. |
|RowOrder  <br/> |xsd:boolean  <br/> |facultatif  <br/> |Indique s’il faut utiliser l’ordre des lignes dans le recordset de données comme clé primaire. True (1) si les ID de ligne sont déterminés par ordre de ligne. False (0) si les ID de ligne sont déterminés par des valeurs dans la ou les colonnes de clé primaire du recordset de données. |Valeurs du type xsd:boolean. |
|TimeRefreshed  <br/> |xsd:dateTime  <br/> |facultatif  <br/> |Date et heure de la dernière actualisation du jeu d’enregistrements de données. |Valeurs du type xsd:dateTime. |
   

