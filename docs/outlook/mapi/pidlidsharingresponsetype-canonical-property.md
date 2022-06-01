---
title: Propriété canonique PidLidSharingResponseType
description: Décrit la propriété canonique PidLidSharingResponseType, qui spécifie le type de réponse auquel le destinataire de la demande de partage a répondu.
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidLidSharingResponseType
api_type:
- COM
ms.assetid: c27b1239-3612-4bb3-9f22-4b89ee9900cd
ms.openlocfilehash: 2c3c7ba1eb1bcfbd615687f52f35c62247f92af8
ms.sourcegitcommit: f872848fbeb5b2353179ad4bf4eab23f61f87666
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/01/2022
ms.locfileid: "65816072"
---
# <a name="pidlidsharingresponsetype-canonical-property"></a>Propriété canonique PidLidSharingResponseType

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Spécifie le type de réponse auquel le destinataire de la demande de partage a répondu. Il s’agit d’une propriété d’un message de partage.
  
|Propriété |Valeur |
|:-----|:-----|
|Propriétés associées :  <br/> |dispidSharingResponseType  <br/> |
|Jeu de propriétés :  <br/> |PSETID_Sharing  <br/> |
|ID long (LID) :  <br/> |0x00008A27  <br/> |
|Type de données :  <br/> |PT_LONG  <br/> |
|Domaine :  <br/> |Partage  <br/> |
   
## <a name="remarks"></a>Remarques

La valeur de cette propriété doit être définie sur l’une des valeurs suivantes :
  
|**Valeur**|**Description**|
|:-----|:-----|
|0x00000000  <br/> |Aucune réponse  <br/> |
|0x00000001  <br/> |Accepted  <br/> |
|0x00000002  <br/> |Denied  <br/> |
   
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications de protocole

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des définitions de jeu de propriétés et des références aux spécifications de protocole Exchange Server associées.
    
[[MS-OXSHARE]](https://msdn.microsoft.com/library/e4e5bd27-d5e0-43f9-a6ea-550876724f3d%28Office.15%29.aspx)
  
> Partage des dossiers de boîte aux lettres entre les clients.
    
### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
## <a name="see-also"></a>Voir aussi



[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage de noms MAPI à des noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

