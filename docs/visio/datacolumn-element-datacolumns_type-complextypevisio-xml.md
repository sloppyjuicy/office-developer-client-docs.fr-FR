---
title: Élément DataColumn (DataColumns_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 92469c2f-f809-dff2-d0ee-b3b8f75083d2
description: Définit l’apparition d’une colonne de données dans la fenêtre Données externes de l’interface utilisateur Visio et qualifie les données de la colonne en définissant son type de données et sa mise en forme.
ms.openlocfilehash: 021e7ffd154f1e124b9eb163acc27260b90c23eb
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/29/2019
ms.locfileid: "34541224"
---
# <a name="datacolumn-element-datacolumns_type-complextype-visio-xml"></a>Élément DataColumn (DataColumns_Type complexType) (Visio XML)

Définit l’apparition d’une  colonne de données dans la fenêtre Données externes de l’interface utilisateur Visio et qualifie les données de la colonne en définissant son type de données et sa mise en forme. 
  
## <a name="element-information"></a>Informations sur l’élément

|||
|:-----|:-----|
|**Type d’élément** <br/> |[DataColumn_Type](datacolumn_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Fichier de schéma** <br/> |VisioSchema15.xsd  <br/> |
|**Composants de document** <br/> |recordsets.xml  <br/> |
   
## <a name="definition"></a>Définition

```XML
< xs:element name="DataColumn" type="DataColumn_Type" minOccurs="1" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Éléments et attributs

Si le schéma définit des exigences spécifiques, telles que **séquence**, **minOccurs**, **maxOccurs** et **choix**, voir la section de définition. 
  
### <a name="parent-elements"></a>Éléments parents

|**Élément**|**Type (Type)**|**Description**|
|:-----|:-----|:-----|
|[DataColumns](datacolumns-element-datarecordset_type-complextypevisio-xml.md) <br/> |[DataColumns_Type](datacolumns_type-complextypevisio-xml.md) <br/> |Contient tous les **éléments DataColumn** d’un ensemble d’enregistrements de données.  <br/> |
   
### <a name="child-elements"></a>Éléments enfants

Aucun.
  
### <a name="attributes"></a>Attributs

|**Attribut**|**Type**|**Obligatoire**|**Description**|**Valeurs possibles**|
|:-----|:-----|:-----|:-----|:-----|
|Calendrier  <br/> |xsd:unsignedShort  <br/> |facultatif  <br/> |ID de calendrier de la colonne de données.  <br/> |Valeurs du type xsd:unsignedShort.  <br/> |
|ColumnNameID  <br/> |xsd:string  <br/> |obligatoire  <br/> |Nom externe de la colonne de données. Apparaît dans les en-tête de la fenêtre **Données** externes et dans les étiquettes des graphiques de données.  <br/> |Valeurs du type xsd:string.  <br/> |
|Monétaire  <br/> |xsd:unsignedShort  <br/> |facultatif  <br/> |ID monétaire de la colonne de données.  <br/> |Valeurs du type xsd:unsignedShort.  <br/> |
|DataType  <br/> |xsd:unsignedShort  <br/> |facultatif  <br/> |Type des données dans la colonne de données.  <br/> |Valeurs du type xsd:unsignedShort.  <br/> |
|Degree  <br/> |xsd:unsignedInt  <br/> |facultatif  <br/> |Spécifie le degré (puissance) des unités, par exemple un carré ou un cube. La valeur par défaut (attribut absent) est 1.  <br/> |Valeurs du type xsd:unsignedInt.  <br/> |
|DisplayOrder  <br/> |xsd:unsignedInt  <br/> |facultatif  <br/> |Définit la position d’affichage de  la colonne de données dans la fenêtre Données externes, de la colonne la plus à gauche (0) à la colonne la plus à droite (valeur la plus grande).  <br/> |Valeurs du type xsd:unsignedInt.  <br/> |
|DisplayWidth  <br/> |xsd:unsignedInt  <br/> |facultatif  <br/> |Largeur de la colonne de données dans la **fenêtre Données** externes.  <br/> |Valeurs du type xsd:unsignedInt.  <br/> |
|Hyperlink  <br/> |xsd:boolean  <br/> |facultatif  <br/> |Indique si la colonne de données crée un lien hypertexte dans une forme lorsque la forme est liée à des données.  <br/> |Valeurs du type xsd:boolean.  <br/> |
|Étiquette  <br/> |xsd:string  <br/> |obligatoire  <br/> |Étiquette de la colonne de données.  <br/> |Valeurs du type xsd:string.  <br/> |
|LangID  <br/> |xsd:unsignedInt  <br/> |facultatif  <br/> |ID de langue de la colonne de données.  <br/> |Valeurs du type xsd:unsignedInt.  <br/> |
|Mappée  <br/> |xsd:boolean  <br/> |facultatif  <br/> |Spécifie si la colonne est visible dans la **fenêtre Données** externes. True (1) pour que la colonne soit visible ; False (0) pour que la colonne ne soit pas visible. La valeur par défaut (attribut absent) est que la colonne soit visible.  <br/> |Valeurs du type xsd:boolean.  <br/> |
|Nom  <br/> |xsd:string  <br/> |obligatoire  <br/> |Nom interne de la colonne de données. Utilisé comme nom de ligne pour l’élément de données de forme (propriété personnalisée) ajouté à une forme lorsque la forme est liée à une ligne de données.  <br/> |Valeurs du type xsd:string.  <br/> |
|OrigLabel  <br/> |xsd:string  <br/> |facultatif  <br/> |Étiquette de colonne renvoyée à Visio par l’interface ADO sous-jacente.  <br/> |Valeurs du type xsd:string.  <br/> |
|UnitType  <br/> |xsd:string  <br/> |facultatif  <br/> |Type d’unité des données dans la colonne de données.  <br/> |Valeurs du type xsd:string.  <br/> |
   

