---
title: Propriété canonique PidTagSentRepresentingEmailAddress
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagSentRepresentingEmailAddress
api_type:
- COM
ms.assetid: 5fa4edde-475c-4568-946b-73eb08f97a61
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 1b82e1e96a5ffbb5c17dd919e78a9f07342194c5
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25397378"
---
# <a name="pidtagsentrepresentingemailaddress-canonical-property"></a>Propriété canonique PidTagSentRepresentingEmailAddress

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient l’adresse de messagerie de l’utilisateur de messagerie qui est représenté par l’expéditeur.
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_SENT_REPRESENTING_EMAIL_ADDRESS, PR_SENT_REPRESENTING_EMAIL_ADDRESS_A, PR_SENT_REPRESENTING_EMAIL_ADDRESS_W  <br/> |
|Identificateur :  <br/> |0 x 0065  <br/> |
|Type de données :  <br/> |PT_UNICODE, PT_STRING8  <br/> |
|Domaine :  <br/> |Address  <br/> |
   
## <a name="remarks"></a>Remarques

Ces propriétés sont des exemples de propriétés d’adresse de l’utilisateur de messagerie est représenté par l’expéditeur. Lorsqu’une application cliente envoie un message de la part d’un autre client, il doit définir toutes les propriétés de l’expéditeur représenté aux valeurs pour que le client. Un utilisateur de messagerie envoi généralement sur son propre compte conserve les propriétés de l’expéditeur représenté non définie.
  
Le fournisseur de transport sortant doit laisser toujours ces propriétés si elle a été définie par le client d’envoi. Si elle n’est pas définie, le fournisseur de transport doit définir la propriété **PR_SENDER_EMAIL_ADDRESS** ([PidTagSenderEmailAddress](pidtagsenderemailaddress-canonical-property.md)) sur la copie du message sortante et laissez non définies sur la copie locale.
  
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications du protocole

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des références aux spécifications du protocole Exchange Server associées.
    
[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> Spécifie les propriétés et les opérations qui sont autorisées pour les objets de message électronique.
    
[[MS-OXORSS]](https://msdn.microsoft.com/library/53bc9634-0040-4b5a-aecd-29781d826009%28Office.15%29.aspx)
  
> Spécifie les propriétés et les opérations qui représentent les éléments RSS.
    
[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)
  
> Gère l’ordre et le flux pour les transferts de données entre un client et le serveur.
    
[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)
  
> La conversion entre IETF RFC2445, RFC2446, RFC2447 et rendez-vous et des objets de la conférence.
    
[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)
  
> Convertit des conventions de messagerie standard Internet aux objets de message.
    
[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)
  
> Spécifie les propriétés et les opérations qui sont autorisées pour les contacts et les listes de distribution personnelles.
    
[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)
  
> Code et décode des objets message et la pièce jointe à une représentation sous forme de flux efficace.
    
### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
MAPITAGS.h
  
> Contient les définitions des propriétés répertoriées en tant que propriétés associées.
    
## <a name="see-also"></a>Voir aussi



[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage des noms MAPI aux noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

