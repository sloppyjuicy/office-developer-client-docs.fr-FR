---
title: DataColumn, élément (DataColumns_Type, complexType) (« Visio XML »)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 92469c2f-f809-dff2-d0ee-b3b8f75083d2
description: Définit comment une colonne de données apparaît dans la fenêtre données externes dans l’interface utilisateur Visio et qualifiant les données dans la colonne en définissant son type de données et de la mise en forme.
ms.openlocfilehash: f74061b9f3b8f4b93d8aa0e97e4e7c1e45131cbd
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19788426"
---
# <a name="datacolumn-element-datacolumnstype-complextype-visio-xml"></a>DataColumn, élément (DataColumns_Type, complexType) (« Visio XML »)

Définit comment une colonne de données apparaît dans la fenêtre **Données externes** dans l’interface utilisateur Visio et qualifiant les données dans la colonne en définissant son type de données et de la mise en forme. 
  
## <a name="element-information"></a>Informations sur l'élément

|||
|:-----|:-----|
|**Type d’élément** <br/> |[DataColumn_Type](datacolumn_type-complextypevisio-xml.md) <br/> |
|**Espace de noms** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Fichier de schéma** <br/> |VisioSchema15.xsd  <br/> |
|**Parties de document** <br/> |recordsets.Xml  <br/> |
   
## <a name="definition"></a>Définition

```XML
< xs:element name="DataColumn" type="DataColumn_Type" minOccurs="1" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Éléments et attributs

Si le schéma définit des exigences spécifiques, telles que **sequence**, **minOccurs**, **maxOccurs**et **choice**, voir la section Définition. 
  
### <a name="parent-elements"></a>Éléments parents

|**Élément**|**Type**|**Description**|
|:-----|:-----|:-----|
|[DataColumns](datacolumns-element-datarecordset_type-complextypevisio-xml.md) <br/> |[DataColumns_Type](datacolumns_type-complextypevisio-xml.md) <br/> |Contient tous les éléments dans un jeu d’enregistrements de données **DataColumn** .  <br/> |
   
### <a name="child-elements"></a>Éléments enfants

Aucun.
  
### <a name="attributes"></a>Attributs

|**Attribut**|**Type**|**Obligatoire**|**Description**|**Valeurs possibles**|
|:-----|:-----|:-----|:-----|:-----|
|Calendrier  <br/> |XSD:unsignedShort  <br/> |facultatif  <br/> |ID de la colonne de données de calendrier.  <br/> |Valeurs du type xsd:unsignedShort.  <br/> |
|ColumnNameID  <br/> |XSD : String  <br/> |obligatoire  <br/> |Nom externe de la colonne de données. S’affiche dans les en-têtes dans la fenêtre **Données externes** et des étiquettes dans les graphiques de données.  <br/> |Valeurs du type xsd : String.  <br/> |
|Monnaie  <br/> |XSD:unsignedShort  <br/> |facultatif  <br/> |CODE devise de la colonne de données.  <br/> |Valeurs du type xsd:unsignedShort.  <br/> |
|Type de données  <br/> |XSD:unsignedShort  <br/> |facultatif  <br/> |Type de données dans la colonne de données.  <br/> |Valeurs du type xsd:unsignedShort.  <br/> |
|Degré  <br/> |XSD:unsignedInt  <br/> |facultatif  <br/> |Spécifie le degré (power) des unités, par exemple au carré ou au cube. La valeur par défaut (attribut absent) est 1.  <br/> |Valeurs du type xsd:unsignedInt.  <br/> |
|DisplayOrder  <br/> |XSD:unsignedInt  <br/> |facultatif  <br/> |Définit la position d’affichage de la colonne de données dans la fenêtre **Données externes** , dans la colonne la plus à gauche (0) à la colonne la plus à droite (valeur la plus élevée).  <br/> |Valeurs du type xsd:unsignedInt.  <br/> |
|DisplayWidth  <br/> |XSD:unsignedInt  <br/> |facultatif  <br/> |Largeur de la colonne de données dans la fenêtre **Données externes** .  <br/> |Valeurs du type xsd:unsignedInt.  <br/> |
|Lien hypertexte  <br/> |type xsd : Boolean  <br/> |facultatif  <br/> |Si la colonne de données crée un lien hypertexte dans une forme lorsque la forme est liée aux données.  <br/> |Valeurs du type de type xsd : Boolean.  <br/> |
|Étiquette  <br/> |XSD : String  <br/> |obligatoire  <br/> |Étiquette de la colonne de données.  <br/> |Valeurs du type xsd : String.  <br/> |
|ID de langue  <br/> |XSD:unsignedInt  <br/> |facultatif  <br/> |L’ID de langue de la colonne de données.  <br/> |Valeurs du type xsd:unsignedInt.  <br/> |
|Mappées  <br/> |type xsd : Boolean  <br/> |facultatif  <br/> |Spécifie si la colonne est visible dans la fenêtre **Données externes** . Valeur True (1) pour la colonne soit visible ; False (0) pour la colonne reste visible. La valeur par défaut (attribut absent) est pour la colonne soit visible.  <br/> |Valeurs du type de type xsd : Boolean.  <br/> |
|Nom  <br/> |XSD : String  <br/> |obligatoire  <br/> |Nom interne de la colonne de données. Utilisé comme le nom de la ligne ajouté à une forme lorsque la forme est liée à une ligne de données pour l’élément de données de forme (propriété personnalisée).  <br/> |Valeurs du type xsd : String.  <br/> |
|OrigLabel  <br/> |XSD : String  <br/> |facultatif  <br/> |Étiquette de colonne renvoyé vers Visio par l’interface ADO sous-jacent.  <br/> |Valeurs du type xsd : String.  <br/> |
|Type_d  <br/> |XSD : String  <br/> |facultatif  <br/> |Type d’unité des données dans la colonne de données.  <br/> |Valeurs du type xsd : String.  <br/> |
   

