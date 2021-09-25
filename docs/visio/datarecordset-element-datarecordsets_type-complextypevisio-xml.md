---
title: Élément DataRecordSet (DataRecordSets_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: aa182f04-0899-ee0e-79e1-b74832933e83
description: Stocke, met en forme, actualise et expose dans Microsoft Visio les données qui ont fait l’objet d’une requête dans une base de données.
ms.openlocfilehash: 41390699788b9606bf72473c17683c32b5a3744e
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59608269"
---
# <a name="datarecordset-element-datarecordsets_type-complextype-visio-xml"></a>Élément DataRecordSet (DataRecordSets_Type complexType) (Visio XML)

Stocke, met en forme, actualise et expose dans Microsoft Visio les données qui ont fait l’objet d’une requête dans une base de données.
  
## <a name="element-information"></a>Informations sur l’élément

|||
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

Si le schéma définit des exigences spécifiques, telles que **séquence**, **minOccurs**, **maxOccurs** et **choix**, voir la section de définition. 
  
### <a name="parent-elements"></a>Éléments parents

|**Élément**|**Type (Type)**|**Description**|
|:-----|:-----|:-----|
|[DataRecordSets](datarecordsets-elementvisio-xml.md) <br/> |[DataRecordSets_Type](datarecordsets_type-complextypevisio-xml.md) <br/> |Contient tous les **éléments DataRecordset** du document.  <br/> |
   
### <a name="child-elements"></a>Éléments enfants

|**Élément**|**Type (Type)**|**Description**|
|:-----|:-----|:-----|
|[ADOData](autolinkcomparison-element-datarecordset_type-complextypevisio-xml.md) <br/> |[ADOData_Type](autolinkcomparison_type-complextypevisio-xml.md) <br/> |Contient du XML conforme au schéma XML classique ADO pour un jeu d’enregistrements ADO et qui décrit les données du jeu d’enregistrements de données.  <br/> |
|[AutoLinkComparison](autolinkcomparison-element-datarecordset_type-complextypevisio-xml.md) <br/> |[AutoLinkComparison_Type](autolinkcomparison_type-complextypevisio-xml.md) <br/> |Définit une règle qui compare une colonne de l’élément **DataRecordset** parent à un élément de données de forme de la dernière action de liaison automatique réussie effectuée dans l’interface utilisateur.  <br/> |
|[DataColumn](datacolumns-element-datarecordset_type-complextypevisio-xml.md) <br/> |[DataColumns_Type](datacolumns_type-complextypevisio-xml.md) <br/> |Définit l’apparition d’une  colonne de données dans la fenêtre Données externes de l’interface utilisateur Visio et qualifie les données de la colonne en définissant son type de données et sa mise en forme.  <br/> |
|[DataColumns](datacolumns-element-datarecordset_type-complextypevisio-xml.md) <br/> |[DataColumns_Type](datacolumns_type-complextypevisio-xml.md) <br/> |Contient tous les **éléments DataColumn** d’un ensemble d’enregistrements de données.  <br/> |
|[PrimaryKey](primarykey-element-datarecordset_type-complextypevisio-xml.md) <br/> |[PrimaryKey_Type](primarykey_type-complextypevisio-xml.md) <br/> |Identifie une ou plusieurs colonnes de clé primaire dans le recordset de données.  <br/> |
|[RefreshConflict](refreshconflict-element-datarecordset_type-complextypevisio-xml.md) <br/> |[RefreshConflict_Type](refreshconflict_type-complextypevisio-xml.md) <br/> |Indique une ligne du recordset de données liée à une forme en conflit après l’actualisation du recordset de données.  <br/> |
|[RowMap](rowmap-element-datarecordset_type-complextypevisio-xml.md) <br/> |[RowMap_Type](rowmap_type-complextypevisio-xml.md) <br/> |Cartes ligne d’un recordset de données à une forme.  <br/> |
   
### <a name="attributes"></a>Attributs

|**Attribut**|**Type**|**Obligatoire**|**Description**|**Valeurs possibles**|
|:-----|:-----|:-----|:-----|:-----|
|Somme de contrôle  <br/> |xsd:unsignedInt  <br/> |facultatif  <br/> |Valeur de la base de contrôle, générée par Visio, et basée sur les propriétés du data-recordset. Définissez cette attirbute sur 0 ; Visio recalcule cette valeur au moment de l’runtime.  <br/> |Valeurs du type xsd:unsignedInt.  <br/> |
|Commande  <br/> |xsd:string  <br/> |facultatif  <br/> |Chaîne de commande utilisée pour interroger des données à partir de la source de données.  <br/> |Valeurs du type xsd:string.  <br/> |
|ConnectionID  <br/> |xsd:unsignedInt  <br/> |facultatif  <br/> |ID de connexion de **l’objet DataConnection** associé. N’existe pas pour les sources de données XML.  <br/> |Valeurs du type xsd:unsignedInt.  <br/> |
|ID  <br/> |xsd:unsignedInt  <br/> |obligatoire  <br/> |ID du recordset de données, unique dans le document.  <br/> |Valeurs du type xsd:unsignedInt.  <br/> |
|Nom  <br/> |xsd:string  <br/> |facultatif  <br/> |Nom d’affichage (ou « convivial ») du groupe d’enregistrements de données.  <br/> |Valeurs du type xsd:string.  <br/> |
|NextRowID  <br/> |xsd:unsignedInt  <br/> |facultatif  <br/> |L’ID Visio ligne suivant.  <br/> |Valeurs du type xsd:unsignedInt.  <br/> |
|Options  <br/> |xsd:unsignedInt  <br/> |facultatif  <br/> |Options à appliquer au recordset de données. Les valeurs possibles peuvent être n’importe quelle combinaison d’une ou de plusieurs de celles indiquées dans le tableau suivant.  <br/> |Valeurs du type xsd:unsignedInt.  <br/> |
|RefreshInterval  <br/> |xsd:unsignedInt  <br/> |facultatif  <br/> |Fréquence (en minutes) Visio le jeu d’enregistrements de données automatiquement. Cette valeur doit être supérieure ou supérieure à 1.  <br/> |Valeurs du type xsd:unsignedInt.  <br/> |
|RefreshNoRecon conférencetionUI  <br/> |xsd:boolean  <br/> |facultatif  <br/> |Indique si l’interface utilisateur de rapprochement des données doit être désactivée. True (1) pour désactiver l’interface utilisateur . False (0) pour activer l’interface utilisateur.  <br/> |Valeurs du type xsd:boolean.  <br/> |
|RefreshOverwriteAll  <br/> |xsd:boolean  <br/> |facultatif  <br/> |Indique s’il faut modifier les modifications apportées par l’utilisateur aux éléments de données de forme dans les formes liées aux données lorsque le recordset de données est actualisé.  <br/> |Valeurs du type xsd:boolean.  <br/> |
|ReplaceLinks  <br/> |xsd:unsignedInt  <br/> |facultatif  <br/> |Définit la façon dont les liaisons de données de forme sont traitées lorsque les formes sont copiées ou coupées. 1 pour remplacer les liens existants dans la forme cible. 0 pour conserver les liaisons existantes dans la forme cible.  <br/> |Valeurs du type xsd:unsignedInt.  <br/> |
|RowOrder  <br/> |xsd:boolean  <br/> |facultatif  <br/> |Indique s’il faut utiliser l’ordre des lignes dans le recordset de données comme clé primaire. True (1) si les ID de ligne sont déterminés par ordre de ligne. False (0) si les ID de ligne sont déterminés par des valeurs dans les colonnes de clé primaire du ou des recordset de données.  <br/> |Valeurs du type xsd:boolean.  <br/> |
|TimeRefreshed  <br/> |xsd:dateTime  <br/> |facultatif  <br/> |Date et heure de la dernière actualisation du jeu d’enregistrements de données.  <br/> |Valeurs du type xsd:dateTime.  <br/> |
   

