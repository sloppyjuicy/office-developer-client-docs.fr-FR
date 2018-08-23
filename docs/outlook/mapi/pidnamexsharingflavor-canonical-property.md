---
title: Propriété canonique PidNameXSharingFlavor
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidNameXSharingFlavor
api_type:
- COM
ms.assetid: 7757fde1-564b-4f3a-9b9e-f80a143690ea
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: bcdca783778e1a310be638ce376d408acf0b247f
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22580039"
---
# <a name="pidnamexsharingflavor-canonical-property"></a>Propriété canonique PidNameXSharingFlavor

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Représente la valeur de la propriété **dispidSharingFlavor** ([PidLidSharingFlavor](pidlidsharingflavor-canonical-property.md)).
  
|||
|:-----|:-----|
|Noms conviviaux :  <br/> |Aucun  <br/> |
|Jeu de propriétés :  <br/> |PS_INTERNET_HEADERS  <br/> |
|Nom de la propriété :  <br/> |Version X partage  <br/> |
|Type de données :  <br/> |PT_UNICODE  <br/> |
|Domaine :  <br/> |Partage  <br/> |
   
## <a name="remarks"></a>Remarques

La propriété **dispidSharingFlavor** doit être une des valeurs suivantes. 
  
|**Valeur**|**Type de Message de partage**|
|:-----|:-----|
|0x00020310  <br/> |Une invitation de partage pour un dossier spécial.  <br/> |
|0x00000310  <br/> |Une invitation de partage pour un dossier qui n’est pas un dossier spécial.  <br/> |
|0x00020500  <br/> |Une demande de partage.  <br/> |
|0x00020710  <br/> |Les deux une invitation de partage pour un dossier spécial et une demande de partage pour un dossier spécial équivalente du destinataire.  <br/> |
|0x00025100  <br/> |Une réponse de partage qui refuse une demande.  <br/> |
|0x00023310  <br/> |Une réponse de partage qui accepte une demande (également un type d’invitation de partage).  <br/> |
   
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications du protocole

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des définitions de jeu de propriétés et des références aux spécifications du protocole Exchange Server connexes.
    
[[MS-OXSHARE]](http://msdn.microsoft.com/library/e4e5bd27-d5e0-43f9-a6ea-550876724f3d%28Office.15%29.aspx)
  
> Partage des dossiers de boîte aux lettres entre des clients.
    
### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
## <a name="see-also"></a>Voir aussi



[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage des noms MAPI aux noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

