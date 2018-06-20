---
title: Propriété canonique PidTagDeliveryPoint
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagDeliveryPoint
api_type:
- HeaderDef
ms.assetid: 715a9dbd-78f8-41e1-a76e-29448d06ec19
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 803481a71d505fc9f12e77b162a91200cac505d6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19785933"
---
# <a name="pidtagdeliverypoint-canonical-property"></a>Propriété canonique PidTagDeliveryPoint

  
  
**S’applique à**: Outlook 
  
Spécifie la nature de l’entité fonctionnelle par lequel le message a été ou serait ont été remis au destinataire. 
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_DELIVERY_POINT  <br/> |
|Identificateur :  <br/> |0x0C07  <br/> |
|Type de données :  <br/> |PT_LONG  <br/> |
|Zone :  <br/> |Destinataire MAPI  <br/> |
   
## <a name="remarks"></a>Remarques

Cette propriété peut avoir exactement une des valeurs suivantes : 
  
MAPI_MH_DP_ML 
  
> Remis à une liste de distribution, une remise point qui peut à son tour distribuer le message à plusieurs destinataires.
    
MAPI_MH_DP_MS 
  
> Remis à une banque de messages à la place de directement à un destinataire.
    
MAPI_MH_DP_OTHER_AU 
  
> Remis à une unité d’accès (UA) autre qu’une unité d’accès remise physique (PDAU), telles qu’un système de télécopie.
    
MAPI_MH_DP_PDAU 
  
> Remis à une unité d’accès remise physique, par exemple un opérateur postal humaine.
    
MAPI_MH_DP_PDS_PATRON 
  
> Remis à un patron remise physique du système, par exemple une boîte aux lettres postal classique.
    
MAPI_MH_DP_PRIVATE_UA 
  
> Remis à un agent utilisateur privés (UA), comme un client dans un système de messagerie en interne.
    
MAPI_MH_DP_PUBLIC_UA 
  
> Remis à un agent utilisateur public ou le fournisseur de services public.
    
La valeur par défaut est MAPI_MH_DP_PRIVATE_UA, autrement dit, un client MAPI. 
  
## <a name="related-resources"></a>Ressources connexes

### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
MAPITAGS.h
  
> Contient les définitions des propriétés répertoriées en tant que propriétés associées.
    
## <a name="see-also"></a>Voir aussi



[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage de noms de propriété canonique aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage de noms MAPI pour les noms de propriété canonique](mapping-mapi-names-to-canonical-property-names.md)

