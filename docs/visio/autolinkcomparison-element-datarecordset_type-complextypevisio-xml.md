---
title: Élément AutoLinkComparison (DataRecordSet_Type, complexType) (« Visio XML »)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: af5eb7fd-89c6-49bf-4e45-431b63d6cd6a
description: Définit une règle qui compare une colonne dans l’élément DataRecordset parent avec un élément de données de forme à partir de la dernière réussite automatique liaison action effectuée dans l’interface utilisateur.
ms.openlocfilehash: 38970a84676f769c36c9bdc3f8334652f7d9ec21
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19788046"
---
# <a name="autolinkcomparison-element-datarecordsettype-complextype-visio-xml"></a>Élément AutoLinkComparison (DataRecordSet_Type, complexType) (« Visio XML »)

Définit une règle qui compare une colonne dans l’élément **DataRecordset** parent avec un élément de données de forme à partir de la dernière réussite automatique liaison action effectuée dans l’interface utilisateur. 
  
## <a name="element-information"></a>Informations sur l'élément

|||
|:-----|:-----|
|**Type d’élément** <br/> |[AutoLinkComparison_Type](autolinkcomparison_type-complextypevisio-xml.md) <br/> |
|**Espace de noms** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Fichier de schéma** <br/> |VisioSchema15.xsd  <br/> |
|**Parties de document** <br/> |recordsets.Xml  <br/> |
   
## <a name="definition"></a>Définition

```XML
<xs:element name="AutoLinkComparison" type="AutoLinkComparison_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Éléments et attributs

Si le schéma définit des exigences spécifiques, telles que **sequence**, **minOccurs**, **maxOccurs**et **choice**, voir la section Définition. 
  
### <a name="parent-elements"></a>Éléments parents

|**Élément**|**Type**|**Description**|
|:-----|:-----|:-----|
|[DataRecordSet](datarecordset-element-datarecordsets_type-complextypevisio-xml.md) <br/> |[DataRecordSet_Type](datarecordset_type-complextypevisio-xml.md) <br/> |Spécifie un jeu d’enregistrements et la liaison de données entre ce jeu d’enregistrements et les formes dans les pages de dessin.  <br/> |
   
### <a name="child-elements"></a>Éléments enfants

Aucun.
  
### <a name="attributes"></a>Attributs

|**Attribut**|**Type**|**Obligatoire**|**Description**|**Valeurs possibles**|
|:-----|:-----|:-----|:-----|:-----|
|ColumnName  <br/> |XSD : String  <br/> |obligatoire  <br/> |Correspond à un nom de colonne dans le jeu d’enregistrements ADO.  <br/> |Valeurs du type xsd : String.  <br/> |
|ContextType  <br/> |XSD:unsignedInt  <br/> |obligatoire  <br/> |Spécifie les propriétés de la forme ou un groupe à utiliser pour la comparaison. Les valeurs sont présentées dans le tableau suivant.  <br/> |Valeurs du type xsd:unsignedInt.  <br/> |
|ContextTypeLabel  <br/> |XSD : String  <br/> |facultatif  <br/> |Si la valeur ContextType est 2 ou 3, cet attribut est requis pour définir une comparaison. Pour ContextType = 2, ContextTypeLabel doit être l’étiquette d’élément de données de forme et si **ContextType** = 3, ContextTypeLabel doit être le nom de ligne locale.  <br/> |Valeurs du type xsd : String.  <br/> |
   

