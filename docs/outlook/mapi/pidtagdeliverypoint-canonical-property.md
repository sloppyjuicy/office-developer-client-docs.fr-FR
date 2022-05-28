---
title: Propriété canonique PidTagDeliveryPoint
description: Décrit la propriété canonique PidTagDeliveryPoint, qui spécifie la nature de l’entité fonctionnelle au moyen de laquelle un message a été remis.
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidTagDeliveryPoint
api_type:
- HeaderDef
ms.assetid: 715a9dbd-78f8-41e1-a76e-29448d06ec19
ms.openlocfilehash: 07c81831ec078dbb845767b226e4071c9936fb9e
ms.sourcegitcommit: 8c8e4ac05a6612dd5c815ab18ba40e56a6ba839d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/28/2022
ms.locfileid: "65769451"
---
# <a name="pidtagdeliverypoint-canonical-property"></a>Propriété canonique PidTagDeliveryPoint

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Spécifie la nature de l’entité fonctionnelle au moyen de laquelle un message a été ou aurait été remis au destinataire. 
  
|Propriété |Valeur |
|:-----|:-----|
|Propriétés associées :  <br/> |PR_DELIVERY_POINT  <br/> |
|Identificateur :  <br/> |0x0C07  <br/> |
|Type de données :  <br/> |PT_LONG  <br/> |
|Domaine :  <br/> |Destinataire MAPI  <br/> |
   
## <a name="remarks"></a>Remarques

Cette propriété peut avoir exactement l’une des valeurs suivantes : 
  
MAPI_MH_DP_ML 
  
> Remis à une liste de distribution, point de remise qui à son tour peut distribuer le message à de nombreux destinataires.
    
MAPI_MH_DP_MS 
  
> Remis à un magasin de messages au lieu d’être directement envoyé à un destinataire.
    
MAPI_MH_DP_OTHER_AU 
  
> Remis à une unité d’accès (AU) autre qu’une unité d’accès de remise physique (PDAU), telle qu’un système FAX.
    
MAPI_MH_DP_PDAU 
  
> Livré à une unité d’accès à la livraison physique, telle qu’un transporteur postal humain.
    
MAPI_MH_DP_PDS_PATRON 
  
> Remis à un client de système de livraison physique, tel qu’une boîte aux lettres postale classique.
    
MAPI_MH_DP_PRIVATE_UA 
  
> Remis à un agent d’utilisateur privé (UA), tel qu’un client dans un système de messagerie interne.
    
MAPI_MH_DP_PUBLIC_UA 
  
> Remis à un agent d’utilisateur public ou à un fournisseur de services publics.
    
La valeur par défaut est MAPI_MH_DP_PRIVATE_UA, c’est-à-dire un client MAPI. 
  
## <a name="related-resources"></a>Ressources connexes

### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
Mapitags.h
  
> Contient des définitions de propriétés répertoriées en tant que propriétés associées.
    
## <a name="see-also"></a>Voir aussi



[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage de noms MAPI à des noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

