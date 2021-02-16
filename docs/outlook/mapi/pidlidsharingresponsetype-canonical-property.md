---
title: Propriété canonique PidLidSharingResponseType
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidSharingResponseType
api_type:
- COM
ms.assetid: c27b1239-3612-4bb3-9f22-4b89ee9900cd
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 34e8a3c73715a75b8007646e5ba3b0dc3e1ae919
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32331191"
---
# <a name="pidlidsharingresponsetype-canonical-property"></a>Propriété canonique PidLidSharingResponseType

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Spécifie le type de réponse auquel le destinataire de la demande de partage a répondu. Il s’agit d’une propriété d’un message de partage.
  
|||
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
|0x00000002  <br/> |Refusé  <br/> |
   
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications de protocole

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des définitions de jeu de propriétés et des références aux spécifications Exchange Server protocole.
    
[[MS-OXSHARE]](https://msdn.microsoft.com/library/e4e5bd27-d5e0-43f9-a6ea-550876724f3d%28Office.15%29.aspx)
  
> Partage des dossiers de boîte aux lettres entre clients.
    
### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
## <a name="see-also"></a>Voir aussi



[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage des noms MAPI aux noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

