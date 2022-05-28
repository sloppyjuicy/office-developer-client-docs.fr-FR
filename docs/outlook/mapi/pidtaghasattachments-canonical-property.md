---
title: Propriété canonique PidTagHasAttachments
description: Décrit la propriété canonique PidTagHasAttachments, qui contient TRUE si un message contient au moins une pièce jointe.
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidTagHasAttachments
api_type:
- HeaderDef
ms.assetid: fd236d74-2868-46a8-bb3d-17f8365931b6
ms.openlocfilehash: b5e9ae78d1ff76fe97f0e07e64a232fba24add7d
ms.sourcegitcommit: 8c8e4ac05a6612dd5c815ab18ba40e56a6ba839d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/28/2022
ms.locfileid: "65770410"
---
# <a name="pidtaghasattachments-canonical-property"></a>Propriété canonique PidTagHasAttachments

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient TRUE si un message contient au moins une pièce jointe. 
  
|Propriété|Valeur|
|:-----|:-----|
|Propriétés associées :  <br/> |PR_HASATTACH  <br/> |
|Identificateur :  <br/> |0x0E1B  <br/> |
|Type de données :  <br/> |PT_BOOLEAN  <br/> |
|Domaine :  <br/> |Pièce jointe de message  <br/> |
   
## <a name="remarks"></a>Remarques

Le magasin de messages copie cette propriété à partir de l’indicateur **MSGFLAG_HASATTACH** de la propriété **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)). Une application cliente peut ensuite utiliser **PR_HASATTACH** pour trier les pièces jointes de message dans une visionneuse de messages. 
  
Valeur mise à jour par cette propriété avec la méthode [IMAPIProp::SaveChanges](imapiprop-savechanges.md) . 
  
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications de protocole

[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Spécifie les propriétés et les opérations autorisées pour les objets de courrier électronique.
    
### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
Mapitags.h
  
> Contient des définitions de propriétés répertoriées en tant que noms secondaires.
    
## <a name="see-also"></a>Voir aussi



[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage de noms MAPI à des noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

