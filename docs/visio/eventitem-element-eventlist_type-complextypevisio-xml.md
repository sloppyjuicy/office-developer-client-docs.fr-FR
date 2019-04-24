---
title: Élément EventItem (complexType EventList_Type) ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6b347117-a1c1-d090-0d71-ea8528ac70c6
description: EnCapsule un code d'événement.
ms.openlocfilehash: 6ed539bd6cb4524b2498b636295442bed917c72a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32337197"
---
# <a name="eventitem-element-eventlisttype-complextype-visio-xml"></a>Élément EventItem (complexType EventList_Type) ('Visio XML')

EnCapsule un code d'événement.
  
## <a name="element-information"></a>Informations sur l’élément

|||
|:-----|:-----|
|**Type d’élément** <br/> |[EventItem_Type](eventitem_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Fichier de schéma** <br/> |VisioSchema15. xsd  <br/> |
|**Parties de document** <br/> |document. Xml  <br/> |
   
## <a name="definition"></a>Définition

```XML
< xs:element name="EventItem" type="EventItem_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Éléments et attributs

Si le schéma définit des exigences spécifiques, telles que **Sequence**, **minOccurs**, **maxOccurs**et **Choice**, reportez-vous à la section définition. 
  
### <a name="parent-elements"></a>Éléments parents

|**Élément**|**Type**|**Description**|
|:-----|:-----|:-----|
|[EventList](eventlist-element-visiodocument_type-complextypevisio-xml.md) <br/> |[EventList_Type](eventlist_type-complextypevisio-xml.md) <br/> |Contient un élément **EventItem** pour chaque événement auquel un objet doit répondre.  <br/> |
   
### <a name="child-elements"></a>Éléments enfants

Aucun.
  
### <a name="attributes"></a>Attributs

|**Attribut**|**Type**|**Obligatoire**|**Description**|**Valeurs possibles**|
|:-----|:-----|:-----|:-----|:-----|
|Action  <br/> |xsd: unsignedShort  <br/> |obligatoire  <br/> |Spécifie le code d'action de l'élément **EventItem** parent.  <br/> |Valeurs du type xsd: unsignedShort.  <br/> |
|Activé  <br/> |xsd: Boolean  <br/> |facultatif  <br/> |Représente un indicateur qui indique si l'événement est activé ou désactivé.  <br/> |Valeurs du type xsd: Boolean.  <br/> |
|CodeÉvénement  <br/> |xsd: unsignedShort  <br/> |obligatoire  <br/> |Code indiquant l'événement qui déclenche le module complémentaire.  <br/> |Valeurs du type xsd: unsignedShort.  <br/> |
|ID  <br/> |xsd: unsignedInt  <br/> |obligatoire  <br/> |ID de l'événement.  <br/> |Valeurs du type xsd: unsignedInt.  <br/> |
|Target  <br/> |xsd: String  <br/> |obligatoire  <br/> |Spécifie la cible d'un événement.  <br/> |Valeurs du type xsd: String.  <br/> |
|TargetArgs  <br/> |xsd: String  <br/> |obligatoire  <br/> |Spécifie une chaîne contenant des arguments à envoyer à la cible d'un événement.  <br/> |Valeurs du type xsd: String.  <br/> |
   

