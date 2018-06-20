---
title: Propriété canonique PidTagHasAttachments
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagHasAttachments
api_type:
- HeaderDef
ms.assetid: fd236d74-2868-46a8-bb3d-17f8365931b6
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 3b618e5a79c3b7e3810ea541aa9b905dfa4188a2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19786046"
---
# <a name="pidtaghasattachments-canonical-property"></a>Propriété canonique PidTagHasAttachments

  
  
**S’applique à**: Outlook 
  
Contient la valeur TRUE si un message contient au moins une pièce jointe. 
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_HASATTACH  <br/> |
|Identificateur :  <br/> |0x0E1B  <br/> |
|Type de données :  <br/> |PT_BOOLEAN  <br/> |
|Zone :  <br/> |Pièce jointe du message  <br/> |
   
## <a name="remarks"></a>Remarques

La banque de messages copie cette propriété à partir de l’indicateur **MSGFLAG_HASATTACH** de la propriété **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)). Une application cliente pouvez ensuite utiliser **PR_HASATTACH** pour effectuer un tri sur les pièces jointes des messages dans l’Observateur d’un message. 
  
La valeur de que cette propriété est mis à jour avec la méthode [IMAPIProp::SaveChanges](imapiprop-savechanges.md) . 
  
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications du protocole

[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Spécifie les propriétés et les opérations qui sont autorisées pour les objets de message électronique.
    
### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
MAPITAGS.h
  
> Contient les définitions des propriétés répertoriées en tant que d’autres noms.
    
## <a name="see-also"></a>Voir aussi



[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage de noms de propriété canonique aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage de noms MAPI pour les noms de propriété canonique](mapping-mapi-names-to-canonical-property-names.md)

