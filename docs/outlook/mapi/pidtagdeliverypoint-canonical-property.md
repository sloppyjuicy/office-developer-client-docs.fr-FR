---
title: Propriété canonique PidTagDeliveryPoint
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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 102018803466acbcaefb4dca4f5180f2e03f0a9a
ms.sourcegitcommit: a355e6b8898e9a1d66ca1bc808fe106e78dcb68f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2022
ms.locfileid: "63724440"
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
  
> Remis à une liste de distribution, un point de remise qui à son tour peut distribuer le message à de nombreux destinataires.
    
MAPI_MH_DP_MS 
  
> Remis à une magasin de messages au lieu d’être directement remis à un destinataire.
    
MAPI_MH_DP_OTHER_AU 
  
> Remis à une unité d’accès (AU) autre qu’une unité d’accès de remise physique (PDAU), telle qu’un système de télécopie.
    
MAPI_MH_DP_PDAU 
  
> Remis à une unité d’accès de remise physique, telle qu’un opérateur postal humain.
    
MAPI_MH_DP_PDS_PATRON 
  
> Remis à un protecteur de système de remise physique, tel qu’une boîte aux lettres postale conventionnelle.
    
MAPI_MH_DP_PRIVATE_UA 
  
> Remis à un agent utilisateur privé (UA), tel qu’un client dans un système de messagerie interne.
    
MAPI_MH_DP_PUBLIC_UA 
  
> Remis à un agent utilisateur public ou à un fournisseur de services publics.
    
La valeur par défaut est MAPI_MH_DP_PRIVATE_UA, c’est-à-dire, un client MAPI. 
  
## <a name="related-resources"></a>Ressources connexes

### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
Mapitags.h
  
> Contient les définitions des propriétés répertoriées en tant que propriétés associées.
    
## <a name="see-also"></a>Voir aussi



[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage des noms MAPI aux noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

