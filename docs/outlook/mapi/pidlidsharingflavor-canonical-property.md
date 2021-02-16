---
title: Propriété canonique PidLidSharingFlavor
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidSharingFlavor
api_type:
- COM
ms.assetid: c91ab5c7-82ac-4895-bf54-2863ca5e2410
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 21144af15e7a36f54af3032f735c391b3038305b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327481"
---
# <a name="pidlidsharingflavor-canonical-property"></a>Propriété canonique PidLidSharingFlavor

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Désigne comme propriété d’un message de partage.
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |dispidSharingFlavor  <br/> |
|Jeu de propriétés :  <br/> |PSETID_Sharing  <br/> |
|ID long (LID) :  <br/> |0x00008A18  <br/> |
|Type de données :  <br/> |PT_LONG  <br/> |
|Domaine :  <br/> |Partage  <br/> |
   
## <a name="remarks"></a>Remarques

La valeur de cette propriété doit être l’une des suivantes :
  
|**Valeur**|**Type d’objet Message de partage**|
|:-----|:-----|
|0x00020310  <br/> |Invitation de partage pour un dossier spécial.  <br/> |
|0x00000310  <br/> |Invitation de partage pour un dossier qui n’est pas un dossier spécial.  <br/> |
|0x00020500  <br/> |Demande de partage.  <br/> |
|0x00020710  <br/> |Invitation de partage pour un dossier spécial et demande de partage pour le dossier spécial équivalent du destinataire.  <br/> |
|0x00025100  <br/> |Réponse de partage refusant une demande.  <br/> |
|0x00023310  <br/> |Réponse de partage acceptant une demande (également un type d’invitation de partage).  <br/> |
   
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

