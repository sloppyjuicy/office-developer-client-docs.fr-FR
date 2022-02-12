---
title: Élément AutoLinkComparison (DataRecordSet_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: af5eb7fd-89c6-49bf-4e45-431b63d6cd6a
description: Définit une règle qui compare une colonne de l’élément DataRecordset parent à un élément de données de forme de la dernière action de liaison automatique réussie effectuée dans l’interface utilisateur.
ms.openlocfilehash: 20823c242df3bf2354b39014cb1ce9340f8fd3cd
ms.sourcegitcommit: c0fae34cd3a9c75a7cffcf9ae8e417ddde07a989
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/12/2022
ms.locfileid: "62783648"
---
# <a name="autolinkcomparison-element-datarecordset_type-complextype-visio-xml"></a>Élément AutoLinkComparison (DataRecordSet_Type complexType) (Visio XML)

Définit une règle qui compare une colonne de l’élément **DataRecordset** parent à un élément de données de forme de la dernière action de liaison automatique réussie effectuée dans l’interface utilisateur. 
  
## <a name="element-information"></a>Informations sur l’élément

|||
|:-----|:-----|
|**Type d’élément** <br/> |[AutoLinkComparison_Type](autolinkcomparison_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Fichier de schéma** <br/> |VisioSchema15.xsd  <br/> |
|**Composants de document** <br/> |recordsets.xml  <br/> |
   
## <a name="definition"></a>Définition

```XML
<xs:element name="AutoLinkComparison" type="AutoLinkComparison_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Éléments et attributs

Si le schéma définit des exigences spécifiques, telles que **séquence**, **minOccurs**, **maxOccurs** et **choix**, consultez la section définition. 
  
### <a name="parent-elements"></a>Éléments parents

|**Élément**|**Type (Type)**|**Description**|
|:-----|:-----|:-----|
|[DataRecordSet](datarecordset-element-datarecordsets_type-complextypevisio-xml.md) <br/> |[DataRecordSet_Type](datarecordset_type-complextypevisio-xml.md) <br/> |Spécifie un recordset et la liaison de données entre ce recordset et les formes dans les pages de dessin. |
   
### <a name="child-elements"></a>Éléments enfants

Aucun.
  
### <a name="attributes"></a>Attributs

|**Attribut**|**Type**|**Obligatoire**|**Description**|**Valeurs possibles**|
|:-----|:-----|:-----|:-----|:-----|
|ColumnName  <br/> |xsd:string  <br/> |obligatoire  <br/> |Correspond à un nom de colonne dans le recordset ADO. |Valeurs du type xsd:string. |
|ContextType  <br/> |xsd:unsignedInt  <br/> |obligatoire  <br/> |Spécifie les propriétés du groupe ou de la forme à utiliser pour la comparaison. Les valeurs possibles sont indiquées dans le tableau suivant. |Valeurs du type xsd:unsignedInt. |
|ContextTypeLabel  <br/> |xsd:string  <br/> |facultatif  <br/> |Si la valeur ContextType est 2 ou 3, cet attribut est requis pour définir une comparaison. Pour ContextType = 2, ContextTypeLabel doit être l’étiquette de l’élément de données de forme, et si **ContextType** = 3, ContextTypeLabel doit être le nom de ligne local. |Valeurs du type xsd:string. |
   

