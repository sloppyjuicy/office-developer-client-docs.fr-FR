---
title: Élément EventList (VisioDocument_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 40bb8c7c-89ef-22e1-5edf-e2423fc89660
description: Contient un élément EventItem pour chaque événement auquel un objet doit répondre.
ms.openlocfilehash: fa94457f4ce066e8162a40caeb76742852d16894
ms.sourcegitcommit: c0fae34cd3a9c75a7cffcf9ae8e417ddde07a989
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/12/2022
ms.locfileid: "62771572"
---
# <a name="eventlist-element-visiodocument_type-complextype-visio-xml"></a>Élément EventList (VisioDocument_Type complexType) (Visio XML)

Contient un **élément EventItem** pour chaque événement auquel un objet doit répondre. 
  
## <a name="element-information"></a>Informations sur l’élément

|||
|:-----|:-----|
|**Type d’élément** <br/> |[EventList_Type](eventlist_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Fichier de schéma** <br/> |VisioSchema15.xsd  <br/> |
|**Composants de document** <br/> |document.xml  <br/> |
   
## <a name="definition"></a>Définition

```XML
< xs:element name="EventList" type="EventList_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Éléments et attributs

Si le schéma définit des exigences spécifiques, telles que **séquence**, **minOccurs**, **maxOccurs** et **choix**, consultez la section définition. 
  
### <a name="parent-elements"></a>Éléments parents

|**Élément**|**Type (Type)**|**Description**|
|:-----|:-----|:-----|
|[VisioDocument](visiodocument-elementvisio-xml.md) <br/> |[VisioDocument_Type](visiodocument_type-complextypevisio-xml.md) <br/> |Élément racine d’un document Microsoft Visio document. |
   
### <a name="child-elements"></a>Éléments enfants

|**Élément**|**Type (Type)**|**Description**|
|:-----|:-----|:-----|
|[EventItem](eventitem-element-eventlist_type-complextypevisio-xml.md) <br/> |[EventItem_Type](eventitem_type-complextypevisio-xml.md) <br/> |Encapsule un code d’événement. |
   
### <a name="attributes"></a>Attributs

Aucun.
  

