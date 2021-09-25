---
title: Propriété canonique PidTagMessageSize
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidTagMessageSize
api_type:
- HeaderDef
ms.assetid: c67fb54b-8cc7-4fbc-8204-36fcddfa6192
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: edebd29dfc8a6ecbc13c2982a290ece0b02e7fc9
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59629752"
---
# <a name="pidtagmessagesize-canonical-property"></a>Propriété canonique PidTagMessageSize

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient la somme, en octets, de la taille de toutes les propriétés d’un objet message. 
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_MESSAGE_SIZE  <br/> |
|Identificateur :  <br/> |0x0E08  <br/> |
|Type de données :  <br/> |PT_LONG  <br/> |
|Domaine :  <br/> |Messagerie générale  <br/> |
   
## <a name="remarks"></a>Remarques

Il est recommandé que les objets de message exposent cette propriété. La taille du message indique le nombre approximatif d’octets transférés lorsque le message est déplacé d’une magasin de messages vers une autre. Étant la somme des tailles de toutes les propriétés de l’objet de message, elle est généralement beaucoup plus grande que le texte du message uniquement. 
  
La plupart des fournisseurs de magasins de messages calculent cette propriété pour les messages qu’ils gèrent. Toutefois, certains fournisseurs de magasins de messages ne la prise en charge de cette propriété. Dans tous les cas, cette propriété n’est pas disponible tant que la méthode [IMAPIProp::SaveChanges ou](imapiprop-savechanges.md) [IMessage::SubmitMessage](imessage-submitmessage.md) n’a pas été appelée. 
  
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications de protocole

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des références aux spécifications Exchange Server protocole.
    
[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Gère les objets message et pièce jointe.
    
[[MS-OXCFOLD]](https://msdn.microsoft.com/library/c0f31b95-c07f-486c-98d9-535ed9705fbf%28Office.15%29.aspx)
  
> Gère les opérations de dossier.
    
[[MS-OXCSTOR]](https://msdn.microsoft.com/library/d42ed1e0-3e77-4264-bd59-7afc583510e2%28Office.15%29.aspx)
  
> Spécifie les opérations autorisées pour les objets principaux de la boutique de messages.
    
### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
Mapitags.h
  
> Contient les définitions des propriétés répertoriées en tant que noms de remplacement.
    
## <a name="see-also"></a>Voir aussi



[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage des noms MAPI aux noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

