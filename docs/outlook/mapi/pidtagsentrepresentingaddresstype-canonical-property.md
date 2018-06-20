---
title: Propriété canonique PidTagSentRepresentingAddressType
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagSentRepresentingAddressType
api_type:
- COM
ms.assetid: 6ecbf653-1faf-47bd-81a4-20157859fdfd
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: a58ae878ba13415823e61db3b1717e3cf07f29c0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19786764"
---
# <a name="pidtagsentrepresentingaddresstype-canonical-property"></a>Propriété canonique PidTagSentRepresentingAddressType

  
  
**S’applique à**: Outlook 
  
Contient le type d’adresse de l’utilisateur de messagerie qui est représenté par l’expéditeur.
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_SENT_REPRESENTING_ADDRTYPE, PR_SENT_REPRESENTING_ADDRTYPE_A, PR_SENT_REPRESENTING_ADDRTYPE_W  <br/> |
|Identificateur :  <br/> |0x0064  <br/> |
|Type de données :  <br/> |PT_UNICODE, PT_STRING8  <br/> |
|Zone :  <br/> |Address  <br/> |
   
## <a name="remarks"></a>Remarques

Ces propriétés sont des exemples de propriétés d’adresse de l’utilisateur de messagerie est représenté par l’expéditeur. Lorsqu’une application cliente envoie un message de la part d’un autre client, il doit définir toutes les propriétés de l’expéditeur représenté aux valeurs pour que le client. Un utilisateur de messagerie envoi généralement sur son propre compte conserve les propriétés de l’expéditeur représenté non définie.
  
Le fournisseur de transport sortant doit toujours laissez cette propriété inchangée si elle a été définie par le client d’envoi. Si elle n’est pas définie, le fournisseur de transport doit définir la propriété **PR_SENDER_ADDRTYPE** ([PidTagSenderAddressType](pidtagsenderaddresstype-canonical-property.md)) sur la copie du message sortante et laissez non définies sur la copie locale.
  
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications du protocole

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des références aux spécifications du protocole Exchange Server associées.
    
[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)
  
> Gère l’ordre et le flux pour les transferts de données entre un client et le serveur.
    
[[MS-OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)
  
> La conversion entre IETF RFC2445, RFC2446, RFC2447 et rendez-vous et des objets de la conférence.
    
[[MS-OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)
  
> Convertit des conventions de messagerie standard Internet aux objets de message.
    
[[MS-OXODLGT]](http://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)
  
> Spécifie les méthodes pour la connexion et configurer des boîtes aux lettres en tant que les délégués et les interactions avec les objets de messagerie et de calendrier lorsqu’ils agissent au nom d’un autre utilisateur.
    
[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> Spécifie les propriétés et les opérations qui sont autorisées pour les objets de message électronique.
    
[[MS-OXOPOST]](http://msdn.microsoft.com/library/9b18fdab-aacd-4d73-9534-be9b6ba2f115%28Office.15%29.aspx)
  
> Spécifie les propriétés et les opérations qui sont autorisées pour publier des objets.
    
[[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)
  
> Spécifie les propriétés et les opérations qui sont autorisées pour les contacts et les listes de distribution personnelles.
    
[[MS-OXTNEF]](http://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)
  
> Code et décode des objets message et la pièce jointe à une représentation sous forme de flux efficace.
    
### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
MAPITAGS.h
  
> Contient les définitions des propriétés répertoriées en tant que propriétés associées.
    
## <a name="see-also"></a>Voir aussi



[Propriété canonique PidTagAddressType](pidtagaddresstype-canonical-property.md)


[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage de noms de propriété canonique aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage de noms MAPI pour les noms de propriété canonique](mapping-mapi-names-to-canonical-property-names.md)

