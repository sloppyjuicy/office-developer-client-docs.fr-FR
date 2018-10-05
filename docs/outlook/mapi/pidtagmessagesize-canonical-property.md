---
title: Propriété canonique PidTagMessageSize
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagMessageSize
api_type:
- HeaderDef
ms.assetid: c67fb54b-8cc7-4fbc-8204-36fcddfa6192
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 3a49c6d70cc47ff726a7a99860b5e81a400be0bf
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25387306"
---
# <a name="pidtagmessagesize-canonical-property"></a>Propriété canonique PidTagMessageSize

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient les fonctions sum, en octets, des tailles de toutes les propriétés sur un objet de message. 
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_MESSAGE_SIZE  <br/> |
|Identificateur :  <br/> |0x0E08  <br/> |
|Type de données :  <br/> |PT_LONG  <br/> |
|Domaine :  <br/> |Général de messagerie  <br/> |
   
## <a name="remarks"></a>Remarques

Il est recommandé que les objets message exposent cette propriété. La taille du message indique le nombre approximatif d’octets qui sont transférées lorsque le message est déplacé à partir d’une banque d’informations à un autre. En cours de la somme des tailles de toutes les propriétés de l’objet du message, il est généralement beaucoup plu nombreuses que seul le texte du message. 
  
La base de la plupart des messages fournisseurs compute cette propriété pour les messages qu’ils gèrent. Toutefois, certains fournisseurs de banque de messages ne prennent pas en charge cette propriété. Dans tous les cas, cette propriété n’est pas disponible jusqu'à ce que la méthode [IMAPIProp::SaveChanges](imapiprop-savechanges.md) ou [IMessage::SubmitMessage](imessage-submitmessage.md) a été appelée. 
  
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications du protocole

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des références aux spécifications du protocole Exchange Server associées.
    
[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Gère les objets de message et la pièce jointe.
    
[[MS-OXCFOLD]](https://msdn.microsoft.com/library/c0f31b95-c07f-486c-98d9-535ed9705fbf%28Office.15%29.aspx)
  
> Gère les opérations de dossier.
    
[[MS-OXCSTOR]](https://msdn.microsoft.com/library/d42ed1e0-3e77-4264-bd59-7afc583510e2%28Office.15%29.aspx)
  
> Spécifie les opérations autorisées pour les objets de banque de messages principale.
    
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

