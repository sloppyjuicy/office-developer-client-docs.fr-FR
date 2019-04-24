---
title: DataColumn, élément (DataColumns_Type complexType) ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 92469c2f-f809-dff2-d0ee-b3b8f75083d2
description: Définit le mode d'affichage d'une colonne de données dans la fenêtre données externes de l'interface utilisateur de Visio et qualifie les données dans la colonne en définissant le type de données et la mise en forme.
ms.openlocfilehash: 453ff44131575bd3d6927fdddb81db5f3f431a3b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32344820"
---
# <a name="datacolumn-element-datacolumnstype-complextype-visio-xml"></a>DataColumn, élément (DataColumns_Type complexType) ('Visio XML')

Définit le mode d'affichage d'une colonne de données dans la fenêtre **données externes** de l'interface utilisateur de Visio et qualifie les données dans la colonne en définissant le type de données et la mise en forme. 
  
## <a name="element-information"></a>Informations sur l’élément

|||
|:-----|:-----|
|**Type d’élément** <br/> |[DataColumn_Type](datacolumn_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Fichier de schéma** <br/> |VisioSchema15. xsd  <br/> |
|**Parties de document** <br/> |recordsets. Xml  <br/> |
   
## <a name="definition"></a>Définition

```XML
< xs:element name="DataColumn" type="DataColumn_Type" minOccurs="1" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Éléments et attributs

Si le schéma définit des exigences spécifiques, telles que **Sequence**, **minOccurs**, **maxOccurs**et **Choice**, reportez-vous à la section définition. 
  
### <a name="parent-elements"></a>Éléments parents

|**Élément**|**Type**|**Description**|
|:-----|:-----|:-----|
|[DataColumns](datacolumns-element-datarecordset_type-complextypevisio-xml.md) <br/> |[DataColumns_Type](datacolumns_type-complextypevisio-xml.md) <br/> |Contient tous les éléments **DataColumn** d'un jeu d'enregistrements de données.  <br/> |
   
### <a name="child-elements"></a>Éléments enfants

Aucun.
  
### <a name="attributes"></a>Attributs

|**Attribut**|**Type**|**Obligatoire**|**Description**|**Valeurs possibles**|
|:-----|:-----|:-----|:-----|:-----|
|Calendrier  <br/> |xsd: unsignedShort  <br/> |facultatif  <br/> |ID de calendrier de la colonne de données.  <br/> |Valeurs du type xsd: unsignedShort.  <br/> |
|ColumnNameID  <br/> |xsd: String  <br/> |obligatoire  <br/> |Nom externe de la colonne de données. S'affiche dans les titres de la fenêtre **données externes** et dans les étiquettes des graphiques de données.  <br/> |Valeurs du type xsd: String.  <br/> |
|Devise  <br/> |xsd: unsignedShort  <br/> |facultatif  <br/> |ID de la colonne de données.  <br/> |Valeurs du type xsd: unsignedShort.  <br/> |
|DataType  <br/> |xsd: unsignedShort  <br/> |facultatif  <br/> |Type de données dans la colonne de données.  <br/> |Valeurs du type xsd: unsignedShort.  <br/> |
|Degree  <br/> |xsd: unsignedInt  <br/> |facultatif  <br/> |Spécifie le degré (puissance) des unités, par exemple carré ou cube. La valeur par défaut (attribut absent) est 1.  <br/> |Valeurs du type xsd: unsignedInt.  <br/> |
|DisplayOrder  <br/> |xsd: unsignedInt  <br/> |facultatif  <br/> |Définit la position d'affichage de la colonne de données dans la fenêtre **données externes** , à partir de la colonne la plus à gauche (0) vers la colonne la plus à droite (valeur la plus élevée).  <br/> |Valeurs du type xsd: unsignedInt.  <br/> |
|DisplayWidth  <br/> |xsd: unsignedInt  <br/> |facultatif  <br/> |Largeur de la colonne de données dans la fenêtre **données externes** .  <br/> |Valeurs du type xsd: unsignedInt.  <br/> |
|Lien hypertexte  <br/> |xsd: Boolean  <br/> |facultatif  <br/> |Indique si la colonne de données crée un lien hypertexte dans une forme lorsque la forme est liée à des données.  <br/> |Valeurs du type xsd: Boolean.  <br/> |
|Étiquette  <br/> |xsd: String  <br/> |obligatoire  <br/> |Étiquette de la colonne de données.  <br/> |Valeurs du type xsd: String.  <br/> |
|ID  <br/> |xsd: unsignedInt  <br/> |facultatif  <br/> |ID de langue de la colonne de données.  <br/> |Valeurs du type xsd: unsignedInt.  <br/> |
|Mappé  <br/> |xsd: Boolean  <br/> |facultatif  <br/> |Indique si la colonne est visible dans la fenêtre **données externes** . True (1) pour que la colonne soit visible; False (0) pour que la colonne ne soit pas visible. La valeur par défaut (attribut absent) correspond à l'affichage de la colonne.  <br/> |Valeurs du type xsd: Boolean.  <br/> |
|Nom  <br/> |xsd: String  <br/> |obligatoire  <br/> |Nom interne de la colonne de données. Utilisé comme nom de ligne pour l'élément de données de forme (propriété personnalisée) ajouté à une forme lorsque la forme est liée à une ligne de données.  <br/> |Valeurs du type xsd: String.  <br/> |
|OrigLabel  <br/> |xsd: String  <br/> |facultatif  <br/> |Étiquette de colonne renvoyée à Visio par l'interface ADO sous-jacente.  <br/> |Valeurs du type xsd: String.  <br/> |
|Type_d'unité  <br/> |xsd: String  <br/> |facultatif  <br/> |Type d'unité des données dans la colonne de données.  <br/> |Valeurs du type xsd: String.  <br/> |
   

