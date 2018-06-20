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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 0333f0c309d89436c50a58124500f1b359584954
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19785400"
---
# <a name="pidlidsharingflavor-canonical-property"></a>Propriété canonique PidLidSharingFlavor

  
  
**S’applique à**: Outlook 
  
Désigne comme une propriété d’un message de partage.
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |dispidSharingFlavor  <br/> |
|Jeu de propriétés :  <br/> |PSETID_Sharing  <br/> |
|ID de type long (capot) :  <br/> |0x00008A18  <br/> |
|Type de données :  <br/> |PT_LONG  <br/> |
|Zone :  <br/> |Partage  <br/> |
   
## <a name="remarks"></a>Remarques

La valeur de cette propriété doit être une des options suivantes :
  
|**Valeur**|**Type d’objet du Message de partage**|
|:-----|:-----|
|0x00020310  <br/> |Une invitation de partage pour un dossier spécial.  <br/> |
|0x00000310  <br/> |Une invitation de partage pour un dossier qui n’est pas un dossier spécial.  <br/> |
|0x00020500  <br/> |Une demande de partage.  <br/> |
|0x00020710  <br/> |Les deux une invitation de partage pour un dossier spécial et une demande de partage pour un dossier spécial équivalente du destinataire.  <br/> |
|0x00025100  <br/> |Le refus d’une demande d’une réponse de partage.  <br/> |
|0x00023310  <br/> |Acceptation d’une demande (également un type d’invitation de partage) une réponse de partage.  <br/> |
   
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
  
[Mappage de noms de propriété canonique aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage de noms MAPI pour les noms de propriété canonique](mapping-mapi-names-to-canonical-property-names.md)

