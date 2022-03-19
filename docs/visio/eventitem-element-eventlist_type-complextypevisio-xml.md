---
title: Élément EventItem (EventList_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 6b347117-a1c1-d090-0d71-ea8528ac70c6
description: Encapsule un code d’événement.
ms.openlocfilehash: b9527cd52268d94f7c6a8ee40742c8b9bbd57ccb
ms.sourcegitcommit: 241637561d21b7752ec690b5179e72b6703eaced
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/18/2022
ms.locfileid: "63633091"
---
# <a name="eventitem-element-eventlist_type-complextype-visio-xml"></a>Élément EventItem (EventList_Type complexType) (Visio XML)

Encapsule un code d’événement.
  
## <a name="element-information"></a>Informations sur l'élément

||Valeur |
|:-----|:-----|
|**Type d’élément** <br/> |[EventItem_Type](eventitem_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Fichier de schéma** <br/> |VisioSchema15.xsd  <br/> |
|**Composants de document** <br/> |document.xml  <br/> |
   
## <a name="definition"></a>Définition

```XML
< xs:element name="EventItem" type="EventItem_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Éléments et attributs

Si le schéma définit des exigences spécifiques, telles que **séquence**, **minOccurs**, **maxOccurs** et **choix**, consultez la section définition. 
  
### <a name="parent-elements"></a>Éléments parents

|**Élément**|**Type**|**Description**|
|:-----|:-----|:-----|
|[EventList](eventlist-element-visiodocument_type-complextypevisio-xml.md) <br/> |[EventList_Type](eventlist_type-complextypevisio-xml.md) <br/> |Contient un **élément EventItem** pour chaque événement auquel un objet doit répondre. |
   
### <a name="child-elements"></a>Éléments enfants

Aucun.
  
### <a name="attributes"></a>Attributs

|**Attribut**|**Type**|**Obligatoire**|**Description**|**Valeurs possibles**|
|:-----|:-----|:-----|:-----|:-----|
|Opération  <br/> |xsd:unsignedShort  <br/> |obligatoire  <br/> |Spécifie le code d’action de **l’élément EventItem** parent. |Valeurs du type xsd:unsignedShort. |
|Activé  <br/> |xsd:boolean  <br/> |facultatif  <br/> |Représente un indicateur indiquant si l’événement est activé ou désactivé. |Valeurs du type xsd:boolean. |
|EventCode  <br/> |xsd:unsignedShort  <br/> |obligatoire  <br/> |Code indiquant l’événement qui déclenche l’module. |Valeurs du type xsd:unsignedShort. |
|ID  <br/> |xsd:unsignedInt  <br/> |obligatoire  <br/> |ID de l’événement. |Valeurs du type xsd:unsignedInt. |
|Target  <br/> |xsd:string  <br/> |obligatoire  <br/> |Spécifie la cible d’un événement. |Valeurs du type xsd:string. |
|TargetArgs  <br/> |xsd:string  <br/> |obligatoire  <br/> |Spécifie une chaîne contenant des arguments à envoyer à la cible d’un événement. |Valeurs du type xsd:string. |
   

