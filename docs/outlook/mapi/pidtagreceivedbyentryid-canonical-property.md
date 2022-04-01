---
title: Propriété canonique PidTagReceivedByEntryId
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.PidTagReceivedByEntryId
api_type:
- COM
ms.assetid: 737f8584-fc52-4324-ac40-2fc554a3095d
description: Contient l’identificateur d’entrée de l’utilisateur de messagerie qui reçoit réellement le message. Cette propriété est définie par le fournisseur de transport entrant.
ms.openlocfilehash: 9396e2841c1ff6f51ece1a0055dece7ba3495425
ms.sourcegitcommit: 1f8a789204b2498101d24fb5136e8ed6ad026c13
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/29/2022
ms.locfileid: "64524421"
---
# <a name="pidtagreceivedbyentryid-canonical-property"></a>Propriété canonique PidTagReceivedByEntryId

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient l’identificateur d’entrée de l’utilisateur de messagerie qui reçoit réellement le message.
  
|Propriété |Valeur |
|:-----|:-----|
|Propriétés associées :  <br/> |PR_RECEIVED_BY_ENTRYID  <br/> |
|Identificateur :  <br/> |0x003F  <br/> |
|Type de données :  <br/> |PT_BINARY  <br/> |
|Domaine :  <br/> |Carnet d’adresses  <br/> |
   
## <a name="remarks"></a>Remarques

Cette propriété est l’une des propriétés d’adresse de l’utilisateur de messagerie qui reçoit le message. Elle doit être définie par le fournisseur de transport entrant.
  
Cette propriété correspond à une enveloppe de remise X.400 par attribut MH_T_ message.
  
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications de protocole

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des références aux spécifications Exchange Server protocole associés.
    
[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> Spécifie les propriétés et opérations autorisées pour les objets de message électronique.
    
[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)
  
> Gère l’ordre et le flux des transferts de données entre un client et un serveur.
    
[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)
  
> Convertit les éléments RFC2445, RFC2446 et RFC2447 de l’IETF, ainsi que les éléments de rendez-vous et de réunion.
    
[[MS-OXODLGT]](https://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)
  
> Spécifie les méthodes de connexion et de configuration des boîtes aux lettres en tant que délégués, ainsi que les interactions avec les objets de message et de calendrier lorsqu’ils agissent pour le compte d’un autre utilisateur.
    
[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)
  
> Code et décode les objets de message et de pièce jointe dans une représentation de flux efficace.
    
### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
Mapitags.h
  
> Contient les définitions des propriétés répertoriées en tant que propriétés associées.
    
## <a name="see-also"></a>Voir aussi



[Propriété canonique PidTagEntryId](pidtagentryid-canonical-property.md)


[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage des noms MAPI aux noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

