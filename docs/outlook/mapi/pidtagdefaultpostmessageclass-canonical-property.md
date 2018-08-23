---
title: Propriété canonique PidTagDefaultPostMessageClass
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagDefaultPostMessageClass
api_type:
- HeaderDef
ms.assetid: 231c288f-547b-4463-9442-1499661b925e
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: 2b4013b311289816f778d7559ee3bcc7dc061538
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22574334"
---
# <a name="pidtagdefaultpostmessageclass-canonical-property"></a>Propriété canonique PidTagDefaultPostMessageClass

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Contient le nom d’une classe de Message du formulaire personnalisé.
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_DEF_POST_MSGCLASS  <br/> |
|Identificateur :  <br/> |0x36E5  <br/> |
|Type de données :  <br/> |PT_STRING8  <br/> |
|Domaine :  <br/> |Conteneur MAPI  <br/> |
   
## <a name="remarks"></a>Remarques

Si cette propriété est définie sur un dossier, soit de la valeur doit contenir exactement la classe de message de base (par exemple, « IPM. Contact » pour un dossier de contacts ou un « IPM. Rendez-vous » pour un dossier de calendrier), ou commencer par la classe de message de base (par exemple, « IPM. Contact.MyContact »).
  
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications du protocole

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des références aux spécifications du protocole Exchange Server associées.
    
[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)
  
> Spécifie les propriétés et opérations pour un rendez-vous, une demande de réunion et les messages de réponse.
    
### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
MAPITAGS.h
  
> Contient les définitions des propriétés répertoriées en tant que d’autres noms.
    
## <a name="see-also"></a>Voir aussi



[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage des noms MAPI aux noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

