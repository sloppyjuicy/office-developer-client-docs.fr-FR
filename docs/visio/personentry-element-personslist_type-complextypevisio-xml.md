---
title: Élément PersonEntry (PersonsList_Type complexType) (Visio XML)
ms.date: 02/18/2022
description: Spécifie les propriétés utilisées pour identifier une personne mentionnée dans les commentaires d’un dessin.
ms.openlocfilehash: 66b9a771841ebf972bb70ccfff94c6fefd356944
ms.sourcegitcommit: 518845d053a009b11c8d907a33822161c0b6bc96
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/08/2022
ms.locfileid: "63371654"
---
# <a name="personentry-element-personslist_type-complextype-visio-xml"></a>Élément PersonEntry (PersonsList_Type complexType) (Visio XML)

Spécifie les propriétés utilisées pour identifier une personne mentionnée dans les commentaires d’un dessin.
  
## <a name="element-information"></a>Informations sur l’élément

|||
|:-----|:-----|
|**Type d’élément** <br/> |[PersonEntry_Type](personentry_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Fichier de schéma** <br/> |VisioSchema15.xsd  <br/> |
|**Composants de document** <br/> |persons.xml  <br/> |
   
## <a name="definition"></a>Définition

```XML
<xs:element name="PersonEntry" type="PersonEntry_Type" minOccurs="0" maxOccurs="unbounded" />
```

## <a name="elements-and-attributes"></a>Éléments et attributs

Si le schéma définit des exigences spécifiques, telles que **séquence**, **minOccurs**, **maxOccurs** et **choix**, consultez la section définition. 
  
### <a name="parent-elements"></a>Éléments parents

|**Élément**|**Type (Type)**|**Description**|
|:-----|:-----|:-----|
|[PersonsList](personslist-element-persons_type-complextypevisio-xml.md) <br/> |[PersonsList_Type](personslist_type-complextypevisio-xml.md) <br/> |Spécifie la liste des personnes mentionnées dans les commentaires d’un dessin. |
   
### <a name="child-elements"></a>Éléments enfants

Aucun.
  
### <a name="attributes"></a>Attributs

|**Attribut**|**Type**|**Obligatoire**|**Description**|**Valeurs possibles**|
|:-----|:-----|:-----|:-----|:-----|
|DisplayName  <br/> |xsd:string  <br/> |obligatoire  <br/> |Nom complet de la personne @mentioned |Valeurs du type xsd:string. |
|PersonID  <br/> |xsd:unsignedInt  <br/> |obligatoire  <br/> | Identificateur unique de la personne @mentioned|Valeurs du type xsd:unsignedInt. |
|ProviderID  <br/> |xsd:string  <br/> |facultatif  <br/> |ID du fournisseur|Valeurs du type xsd:string. |
|UserID  <br/> |xsd:string  <br/> |facultatif  <br/> |Identificateur du compte d’utilisateur|Valeurs du type xsd:string. |

