---
title: Propriété canonique PidTagSenderEmailAddress
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagSenderEmailAddress
api_type:
- COM
ms.assetid: 6e1531ac-489b-4224-921a-8fd13ace9497
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 82c0e386ab9231d1066dbdc4456c31031d2409c1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359163"
---
# <a name="pidtagsenderemailaddress-canonical-property"></a>Propriété canonique PidTagSenderEmailAddress

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient l'adresse de messagerie de l'expéditeur du message.
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_SENDER_EMAIL_ADDRESS, PR_SENDER_EMAIL_ADDRESS_A, PR_SENDER_EMAIL_ADDRESS_W  <br/> |
|Identificateur :  <br/> |0x0C1F  <br/> |
|Type de données :  <br/> |PT_UNICOIDE, PT_STRING8  <br/> |
|Domaine :  <br/> |Address  <br/> |
   
## <a name="remarks"></a>Remarques

Ces propriétés sont des exemples de propriétés d'adresse pour l'expéditeur du message. Elles doivent être définies par le fournisseur de transport sortant, qui ne doit jamais propager de valeurs précédemment existantes.
  
Si aucun fournisseur de transport n'a fourni de propriétés d'adresse d'expéditeur, le spouleur MAPI tente de les remplir en appelant la méthode [IMAPISession:: QueryIdentity](imapisession-queryidentity.md) pour un identificateur d'entrée. Si aucun identificateur d'entrée n'a été fourni, le spouleur MAPI stocke «inconnu» dans toutes les propriétés d'adresse de l'expéditeur de type PT_TSTRING. 
  
## <a name="related-resources"></a>Ressources associées

### <a name="protocol-specifications"></a>Spécifications de protocole

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des références à des spécifications de protocole Exchange Server connexes.
    
[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> Spécifie les propriétés et les opérations qui sont autorisées pour les objets message électronique.
    
[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)
  
> Gère l'ordre et le flux de transfert de données entre un client et un serveur.
    
[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)
  
> Effectue une conversion entre l'IETF RFC2445, RFC2446 et RFC2447, et les objets de rendez-vous et de réunion.
    
[[MS-OXOPOST]](https://msdn.microsoft.com/library/9b18fdab-aacd-4d73-9534-be9b6ba2f115%28Office.15%29.aspx)
  
> Spécifie les propriétés et les opérations qui sont autorisées pour les objets post.
    
[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)
  
> Spécifie les propriétés et les opérations qui sont autorisées pour les objets de liste de distribution personnelle et de contact.
    
[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)
  
> Encode et décode les objets message et Attachment en une représentation de flux efficace.
    
### <a name="header-files"></a>Fichiers d'en-tête

Mapidefs. h
  
> Fournit des définitions de type de données.
    
Mapitags. h
  
> Contient les définitions des propriétés indiquées en tant que propriétés associées.
    
## <a name="see-also"></a>Voir aussi



[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage des noms MAPI aux noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

