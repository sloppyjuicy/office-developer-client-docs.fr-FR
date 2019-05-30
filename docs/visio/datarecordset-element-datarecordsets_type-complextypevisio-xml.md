---
title: Élément DataRecordSet (DataRecordSets_Type complexType) (XML Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: aa182f04-0899-ee0e-79e1-b74832933e83
description: Stocke, met en forme, actualise et expose dans Microsoft Visio les données qui ont fait l’objet d’une requête dans une base de données.
ms.openlocfilehash: e478593f370968db5fe9a65329cb1928c0f7c6ea
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/29/2019
ms.locfileid: "34539676"
---
# <a name="datarecordset-element-datarecordsetstype-complextype-visio-xml"></a>Élément DataRecordSet (DataRecordSets_Type complexType) (XML Visio)

Stocke, met en forme, actualise et expose dans Microsoft Visio les données qui ont fait l’objet d’une requête dans une base de données.
  
## <a name="element-information"></a>Informations sur l’élément

|||
|:-----|:-----|
|**Type d’élément** <br/> |[DataRecordSet_Type](datarecordset_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Fichier de schéma** <br/> |VisioSchema15. xsd  <br/> |
|**Parties de document** <br/> |recordsets. Xml  <br/> |
   
## <a name="definition"></a>Définition

```XML
< xs:element name="DataRecordSet" type="DataRecordSet_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Éléments et attributs

Si le schéma définit des exigences spécifiques, telles que **Sequence**, **minOccurs**, **maxOccurs**et **Choice**, reportez-vous à la section définition. 
  
### <a name="parent-elements"></a>Éléments parents

|**Élément**|**Type**|**Description**|
|:-----|:-----|:-----|
|[DataRecordSets](datarecordsets-elementvisio-xml.md) <br/> |[DataRecordSets_Type](datarecordsets_type-complextypevisio-xml.md) <br/> |Contient tous les éléments **DataRecordset** dans le document.  <br/> |
   
### <a name="child-elements"></a>Éléments enfants

|**Élément**|**Type**|**Description**|
|:-----|:-----|:-----|
|[ADOData](autolinkcomparison-element-datarecordset_type-complextypevisio-xml.md) <br/> |[ADOData_Type](autolinkcomparison_type-complextypevisio-xml.md) <br/> |Contient le code XML conforme au schéma XML ADO classique pour un jeu d’enregistrements ADO et qui décrit les données du jeu d’enregistrements de données.  <br/> |
|[AutoLinkComparison](autolinkcomparison-element-datarecordset_type-complextypevisio-xml.md) <br/> |[AutoLinkComparison_Type](autolinkcomparison_type-complextypevisio-xml.md) <br/> |Définit une règle qui compare une colonne de l’élément **DataRecordset** parent à un élément de données de forme à partir de la dernière action de liaison automatique réussie effectuée dans l’interface utilisateur.  <br/> |
|[Nommée](datacolumns-element-datarecordset_type-complextypevisio-xml.md) <br/> |[DataColumns_Type](datacolumns_type-complextypevisio-xml.md) <br/> |Définit le mode d’affichage d’une colonne de données dans la fenêtre **données externes** de l’interface utilisateur de Visio et qualifie les données dans la colonne en définissant le type de données et la mise en forme.  <br/> |
|[DataColumns](datacolumns-element-datarecordset_type-complextypevisio-xml.md) <br/> |[DataColumns_Type](datacolumns_type-complextypevisio-xml.md) <br/> |Contient tous les éléments **DataColumn** d’un jeu d’enregistrements de données.  <br/> |
|[Primaire](primarykey-element-datarecordset_type-complextypevisio-xml.md) <br/> |[PrimaryKey_Type](primarykey_type-complextypevisio-xml.md) <br/> |Identifie une ou plusieurs colonnes de clé primaire dans le jeu d’enregistrements de données.  <br/> |
|[RefreshConflict](refreshconflict-element-datarecordset_type-complextypevisio-xml.md) <br/> |[RefreshConflict_Type](refreshconflict_type-complextypevisio-xml.md) <br/> |Indique une ligne du jeu d’enregistrements de données qui est liée à une forme en conflit après l’actualisation du jeu d’enregistrements de données.  <br/> |
|[RowMap](rowmap-element-datarecordset_type-complextypevisio-xml.md) <br/> |[RowMap_Type](rowmap_type-complextypevisio-xml.md) <br/> |Mappe une ligne de jeu d’enregistrements de données à une forme.  <br/> |
   
### <a name="attributes"></a>Attributs

|**Attribut**|**Type**|**Obligatoire**|**Description**|**Valeurs possibles**|
|:-----|:-----|:-----|:-----|:-----|
|Somme de contrôle  <br/> |xsd: unsignedInt  <br/> |facultatif  <br/> |Valeur de checksum, générée par Visio et basée sur les propriétés du jeu d’enregistrements de données. Définissez cette attirbute sur 0; Visio recalcule cette valeur lors de l’exécution.  <br/> |Valeurs du type xsd: unsignedInt.  <br/> |
|Command  <br/> |xsd: String  <br/> |facultatif  <br/> |Chaîne de commande utilisée pour interroger les données de la source de données.  <br/> |Valeurs du type xsd: String.  <br/> |
|ID  <br/> |xsd: unsignedInt  <br/> |facultatif  <br/> |ID de connexion de l’objet **DataConnection** associé. N’existe pas pour les sources de données XML.  <br/> |Valeurs du type xsd: unsignedInt.  <br/> |
|ID  <br/> |xsd: unsignedInt  <br/> |obligatoire  <br/> |ID du jeu d’enregistrements de données, unique dans le document.  <br/> |Valeurs du type xsd: unsignedInt.  <br/> |
|Nom  <br/> |xsd: String  <br/> |facultatif  <br/> |Nom d’affichage (ou «convivial») du jeu d’enregistrements de données.  <br/> |Valeurs du type xsd: String.  <br/> |
|NextRowID  <br/> |xsd: unsignedInt  <br/> |facultatif  <br/> |Prochain ID de ligne Visio disponible.  <br/> |Valeurs du type xsd: unsignedInt.  <br/> |
|Options  <br/> |xsd: unsignedInt  <br/> |facultatif  <br/> |Options à appliquer au jeu d’enregistrements de données. Les valeurs possibles peuvent être n’importe quelle combinaison d’une ou de plusieurs de celles indiquées dans le tableau suivant.  <br/> |Valeurs du type xsd: unsignedInt.  <br/> |
|RefreshInterval  <br/> |xsd: unsignedInt  <br/> |facultatif  <br/> |Fréquence (en minutes) de Visio actualise automatiquement le jeu d’enregistrements de données. Cette valeur doit être supérieure ou égale à 1.  <br/> |Valeurs du type xsd: unsignedInt.  <br/> |
|RefreshNoReconciliationUI  <br/> |xsd: Boolean  <br/> |facultatif  <br/> |Indique si l’interface utilisateur de rapprochement des données doit être désactivée. True (1) pour désactiver l’interface utilisateur. False (0) pour activer l’interface utilisateur.  <br/> |Valeurs du type xsd: Boolean.  <br/> |
|RefreshOverwriteAll  <br/> |xsd: Boolean  <br/> |facultatif  <br/> |S’il faut remplacer les modifications apportées par l’utilisateur aux éléments de données de forme dans les formes liées aux données lors de l’actualisation du jeu d’enregistrements de données.  <br/> |Valeurs du type xsd: Boolean.  <br/> |
|ReplaceLinks  <br/> |xsd: unsignedInt  <br/> |facultatif  <br/> |Définit comment les liaisons de données de forme sont traitées lorsque les formes sont copiées ou coupées. 1 pour remplacer les liens existants dans la forme cible. 0 pour conserver les liens existants dans la forme cible.  <br/> |Valeurs du type xsd: unsignedInt.  <br/> |
|RowOrder  <br/> |xsd: Boolean  <br/> |facultatif  <br/> |Indique s’il faut utiliser l’ordre des lignes dans le jeu d’enregistrements de données en tant que clé primaire. True (1) si les ID de ligne sont déterminés par l’ordre des lignes. False (0) si les ID de ligne sont déterminés par les valeurs dans les colonnes de clé primaire du jeu d’enregistrements de données.  <br/> |Valeurs du type xsd: Boolean.  <br/> |
|TimeRefreshed  <br/> |xsd: dateTime  <br/> |facultatif  <br/> |Date et heure de la dernière actualisation du jeu d’enregistrements de données.  <br/> |Valeurs du type xsd: dateTime.  <br/> |
   

