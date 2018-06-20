---
title: Élément EventItem (EventList_Type, complexType) (« Visio XML »)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6b347117-a1c1-d090-0d71-ea8528ac70c6
description: Encapsule un code d’événement.
ms.openlocfilehash: dcdd3aa264e8ddfb1aa6f2e908f1c43a0d470872
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19788572"
---
# <a name="eventitem-element-eventlisttype-complextype-visio-xml"></a>Élément EventItem (EventList_Type, complexType) (« Visio XML »)

Encapsule un code d’événement.
  
## <a name="element-information"></a>Informations sur l'élément

|||
|:-----|:-----|
|**Type d’élément** <br/> |[EventItem_Type](eventitem_type-complextypevisio-xml.md) <br/> |
|**Espace de noms** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Fichier de schéma** <br/> |VisioSchema15.xsd  <br/> |
|**Parties de document** <br/> |document.Xml  <br/> |
   
## <a name="definition"></a>Définition

```XML
< xs:element name="EventItem" type="EventItem_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Éléments et attributs

Si le schéma définit des exigences spécifiques, telles que **sequence**, **minOccurs**, **maxOccurs**et **choice**, voir la section Définition. 
  
### <a name="parent-elements"></a>Éléments parents

|**Élément**|**Type**|**Description**|
|:-----|:-----|:-----|
|[EventList](eventlist-element-visiodocument_type-complextypevisio-xml.md) <br/> |[EventList_Type](eventlist_type-complextypevisio-xml.md) <br/> |Contient un élément **EventItem** pour chaque événement auquel un objet doit répondre.  <br/> |
   
### <a name="child-elements"></a>Éléments enfants

Aucun.
  
### <a name="attributes"></a>Attributs

|**Attribut**|**Type**|**Obligatoire**|**Description**|**Valeurs possibles**|
|:-----|:-----|:-----|:-----|:-----|
|Action  <br/> |XSD:unsignedShort  <br/> |obligatoire  <br/> |Spécifie le code d’action de l’élément de **EventItem** parent.  <br/> |Valeurs du type xsd:unsignedShort.  <br/> |
|Activé  <br/> |type xsd : Boolean  <br/> |facultatif  <br/> |Représente un indicateur indiquant si l’événement est activé ou désactivé.  <br/> |Valeurs du type de type xsd : Boolean.  <br/> |
|EventCode  <br/> |XSD:unsignedShort  <br/> |obligatoire  <br/> |Un code indiquant l’événement qui déclenche le module complémentaire.  <br/> |Valeurs du type xsd:unsignedShort.  <br/> |
|ID  <br/> |XSD:unsignedInt  <br/> |obligatoire  <br/> |ID de l’événement.  <br/> |Valeurs du type xsd:unsignedInt.  <br/> |
|Cible  <br/> |XSD : String  <br/> |obligatoire  <br/> |Spécifie la cible d’un événement.  <br/> |Valeurs du type xsd : String.  <br/> |
|TargetArgs  <br/> |XSD : String  <br/> |obligatoire  <br/> |Spécifie une chaîne qui contient les arguments à envoyer à la cible d’un événement.  <br/> |Valeurs du type xsd : String.  <br/> |
   

