---
title: DataRecordSet, élément (DataRecordSets_Type, complexType) (« Visio XML »)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: aa182f04-0899-ee0e-79e1-b74832933e83
description: Stocke, met en forme, actualise et expose dans Microsoft Visio les données qui ont fait l’objet d’une requête dans une base de données.
ms.openlocfilehash: 157213476214c736367b724dd6ca944060c53467
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19788416"
---
# <a name="datarecordset-element-datarecordsetstype-complextype-visio-xml"></a>DataRecordSet, élément (DataRecordSets_Type, complexType) (« Visio XML »)

Stocke, met en forme, actualise et expose dans Microsoft Visio les données qui ont fait l’objet d’une requête dans une base de données.
  
## <a name="element-information"></a>Informations sur l'élément

|||
|:-----|:-----|
|**Type d’élément** <br/> |[DataRecordSet_Type](datarecordset_type-complextypevisio-xml.md) <br/> |
|**Espace de noms** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Fichier de schéma** <br/> |VisioSchema15.xsd  <br/> |
|**Parties de document** <br/> |recordsets.Xml  <br/> |
   
## <a name="definition"></a>Définition

```XML
< xs:element name="DataRecordSet" type="DataRecordSet_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Éléments et attributs

Si le schéma définit des exigences spécifiques, telles que **sequence**, **minOccurs**, **maxOccurs**et **choice**, voir la section Définition. 
  
### <a name="parent-elements"></a>Éléments parents

|**Élément**|**Type**|**Description**|
|:-----|:-----|:-----|
|[DataRecordSets](datarecordsets-elementvisio-xml.md) <br/> |[DataRecordSets_Type](datarecordsets_type-complextypevisio-xml.md) <br/> |Contient tous les éléments **DataRecordset** dans le document.  <br/> |
   
### <a name="child-elements"></a>Éléments enfants

|**Élément**|**Type**|**Description**|
|:-----|:-----|:-----|
|[ADOData](autolinkcomparison-element-datarecordset_type-complextypevisio-xml.md) <br/> |[ADOData_Type](autolinkcomparison_type-complextypevisio-xml.md) <br/> |Contient du code XML conforme au schéma XML classique ADO pour un objet recordset ADO et qui décrit les données du jeu d’enregistrements de données.  <br/> |
|[AutoLinkComparison](autolinkcomparison-element-datarecordset_type-complextypevisio-xml.md) <br/> |[AutoLinkComparison_Type](autolinkcomparison_type-complextypevisio-xml.md) <br/> |Définit une règle qui compare une colonne dans l’élément **DataRecordset** parent avec un élément de données de forme à partir de la dernière réussite automatique liaison action effectuée dans l’interface utilisateur.  <br/> |
|[DataColumn](datacolumns-element-datarecordset_type-complextypevisio-xml.md) <br/> |[DataColumns_Type](datacolumns_type-complextypevisio-xml.md) <br/> |Définit comment une colonne de données apparaît dans la fenêtre **Données externes** dans l’interface utilisateur Visio et qualifiant les données dans la colonne en définissant son type de données et de la mise en forme.  <br/> |
|[DataColumns](datacolumns-element-datarecordset_type-complextypevisio-xml.md) <br/> |[DataColumns_Type](datacolumns_type-complextypevisio-xml.md) <br/> |Contient tous les éléments dans un jeu d’enregistrements de données **DataColumn** .  <br/> |
|[PrimaryKey](primarykey-element-datarecordset_type-complextypevisio-xml.md) <br/> |[PrimaryKey_Type](primarykey_type-complextypevisio-xml.md) <br/> |Identifie une ou plusieurs colonnes de clé primaire du jeu d’enregistrements de données.  <br/> |
|[RefreshConflict](refreshconflict-element-datarecordset_type-complextypevisio-xml.md) <br/> |[RefreshConflict_Type](refreshconflict_type-complextypevisio-xml.md) <br/> |Indique une ligne dans le jeu d’enregistrements de données liée à une forme qui est en conflit après l’actualisation du jeu d’enregistrements.  <br/> |
|[RowMap](rowmap-element-datarecordset_type-complextypevisio-xml.md) <br/> |[RowMap_Type](rowmap_type-complextypevisio-xml.md) <br/> |Mappe une ligne du jeu d’enregistrements de données à une forme.  <br/> |
   
### <a name="attributes"></a>Attributs

|**Attribut**|**Type**|**Obligatoire**|**Description**|**Valeurs possibles**|
|:-----|:-----|:-----|:-----|:-----|
|Somme de contrôle  <br/> |XSD:unsignedInt  <br/> |facultatif  <br/> |Une valeur de somme de contrôle généré par Visio et en fonction des propriétés de jeu d’enregistrements de données. Cette attirbute la valeur 0 ; Visio recalcule cette valeur lors de l’exécution.  <br/> |Valeurs du type xsd:unsignedInt.  <br/> |
|Commande  <br/> |XSD : String  <br/> |facultatif  <br/> |La chaîne de commande utilisée pour interroger les données à partir de la source de données.  <br/> |Valeurs du type xsd : String.  <br/> |
|ID de connexion  <br/> |XSD:unsignedInt  <br/> |facultatif  <br/> |L’identificateur de connexion pour l’objet **DataConnection** associé. N’existe pas pour les sources de données XML.  <br/> |Valeurs du type xsd:unsignedInt.  <br/> |
|ID  <br/> |XSD:unsignedInt  <br/> |obligatoire  <br/> |L’ID de jeu d’enregistrements données, unique dans le document.  <br/> |Valeurs du type xsd:unsignedInt.  <br/> |
|Nom  <br/> |XSD : String  <br/> |facultatif  <br/> |Affichage (ou « conviviales ») nom du jeu d’enregistrements.  <br/> |Valeurs du type xsd : String.  <br/> |
|NextRowID  <br/> |XSD:unsignedInt  <br/> |facultatif  <br/> |Le code suivant disponible Visio ligne.  <br/> |Valeurs du type xsd:unsignedInt.  <br/> |
|Options  <br/> |XSD:unsignedInt  <br/> |facultatif  <br/> |Options à appliquer au jeu d’enregistrements de données. Les valeurs possibles peuvent être n’importe quelle combinaison d’une ou plusieurs de ces indiqué dans le tableau suivant.  <br/> |Valeurs du type xsd:unsignedInt.  <br/> |
|RefreshInterval  <br/> |XSD:unsignedInt  <br/> |facultatif  <br/> |La fréquence (en minutes) Visio actualise le jeu d’enregistrements de données automatiquement. Cette valeur doit être 1 ou plus.  <br/> |Valeurs du type xsd:unsignedInt.  <br/> |
|RefreshNoReconciliationUI  <br/> |type xsd : Boolean  <br/> |facultatif  <br/> |Si l’interface utilisateur de données-rapprochement doit être désactivé. La valeur True (1) pour désactiver l’interface utilisateur (IU). False (0) pour activer l’interface utilisateur.  <br/> |Valeurs du type de type xsd : Boolean.  <br/> |
|RefreshOverwriteAll  <br/> |type xsd : Boolean  <br/> |facultatif  <br/> |S’il faut remplacer les modifications de l’utilisateur aux éléments de données de forme des formes liées aux données lors de l’actualisation du jeu d’enregistrements.  <br/> |Valeurs du type de type xsd : Boolean.  <br/> |
|ReplaceLinks  <br/> |XSD:unsignedInt  <br/> |facultatif  <br/> |Définit la façon dont les liaisons de données de forme sont traités lorsque les formes sont copiées ou coupées. 1 pour remplacer les liens existants dans la forme cible. 0 pour mettre à jour les liens existants dans la forme cible.  <br/> |Valeurs du type xsd:unsignedInt.  <br/> |
|RowOrder  <br/> |type xsd : Boolean  <br/> |facultatif  <br/> |S’il faut utiliser l’ordre des lignes dans le jeu d’enregistrements de données comme clé primaire. La valeur True (1) si l’ID de ligne est déterminées par ordre de ligne. False (0) si l’ID de ligne est déterminées par les valeurs dans les colonnes de clé primaires du jeu d’enregistrements données.  <br/> |Valeurs du type de type xsd : Boolean.  <br/> |
|TimeRefreshed  <br/> |XSD : DateTime  <br/> |facultatif  <br/> |Date et heure de que dernière actualisation du jeu d’enregistrements.  <br/> |Valeurs du type xsd : DateTime.  <br/> |
   

