---
title: Propriété canonique PidNameXSharingFlavor
description: Décrit la propriété canonique PidNameXSharingFlavor, qui représente la valeur de la propriété dispidSharingFlavor.
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidNameXSharingFlavor
api_type:
- COM
ms.assetid: 7757fde1-564b-4f3a-9b9e-f80a143690ea
ms.openlocfilehash: 14b63c87310b980e272630b8ac469afe4540fb3c
ms.sourcegitcommit: f872848fbeb5b2353179ad4bf4eab23f61f87666
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/01/2022
ms.locfileid: "65811941"
---
# <a name="pidnamexsharingflavor-canonical-property"></a>Propriété canonique PidNameXSharingFlavor

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Représente la valeur de la propriété **dispidSharingFlavor** ([PidLidSharingFlavor](pidlidsharingflavor-canonical-property.md)).
  
|Propriété |Valeur |
|:-----|:-----|
|Noms conviviaux :  <br/> |Aucun  <br/> |
|Jeu de propriétés :  <br/> |PS_INTERNET_HEADERS  <br/> |
|Nom de la propriété :  <br/> |X-Sharing-Flavor  <br/> |
|Type de données :  <br/> |PT_UNICODE  <br/> |
|Domaine :  <br/> |Partage  <br/> |
   
## <a name="remarks"></a>Remarques

La propriété **dispidSharingFlavor** doit être l’une des valeurs suivantes. 
  
|**Valeur**|**Type de message de partage**|
|:-----|:-----|
|0x00020310  <br/> |Invitation de partage pour un dossier spécial. |
|0x00000310  <br/> |Invitation de partage pour un dossier qui n’est pas un dossier spécial. |
|0x00020500  <br/> |Demande de partage. |
|0x00020710  <br/> |Une invitation de partage pour un dossier spécial et une demande de partage pour le dossier spécial équivalent du destinataire. |
|0x00025100  <br/> |Réponse de partage qui refuse une demande. |
|0x00023310  <br/> |Réponse de partage qui accepte une demande (également un type d’invitation de partage). |
   
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

