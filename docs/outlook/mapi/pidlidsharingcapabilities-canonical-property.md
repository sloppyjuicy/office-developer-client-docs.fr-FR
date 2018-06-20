---
title: Propriété canonique PidLidSharingCapabilities
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidSharingCapabilities
api_type:
- COM
ms.assetid: 86b3eab2-2594-4204-aedf-8ce2ee3b81ce
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 73f39c0b97ebcd5c84bb908b62f758eaacd4eabf
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19785396"
---
# <a name="pidlidsharingcapabilities-canonical-property"></a>Propriété canonique PidLidSharingCapabilities

  
  
**S’applique à**: Outlook 
  
Désigne comme une propriété d’un message de partage.
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |dispidSharingCaps  <br/> |
|Jeu de propriétés :  <br/> |PSETID_Sharing  <br/> |
|ID de type long (capot) :  <br/> |0x00008A17  <br/> |
|Type de données :  <br/> |PT_LONG  <br/> |
|Zone :  <br/> |Partage  <br/> |
   
## <a name="remarks"></a>Remarques

Cette propriété doit être définie sur une des valeurs suivantes :
  
|**Valeur**|**Scénario**|
|:-----|:-----|
|0x00040290  <br/> |Cet objet de Message de partage est lié à un dossier spécial.  <br/> |
|0x000402B0  <br/> |Cet objet de Message de partage n’est pas relié à un dossier spécial.  <br/> |
   
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

