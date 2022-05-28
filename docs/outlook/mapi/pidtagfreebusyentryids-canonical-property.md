---
title: Propriété canonique PidTagFreeBusyEntryIds
description: Décrit la propriété canonique PidTagFreeBusyEntryIds, qui s’applique à Outlook 2013 et Outlook 2016.
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidTagFreeBusyEntryIds
api_type:
- HeaderDef
ms.assetid: 8bc40ebf-76f2-49dd-af4b-4095bc07c639
ms.openlocfilehash: d9119d7c29f758c5fe431c93540e29eeb207e060
ms.sourcegitcommit: 8c8e4ac05a6612dd5c815ab18ba40e56a6ba839d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/28/2022
ms.locfileid: "65770242"
---
# <a name="pidtagfreebusyentryids-canonical-property"></a>Propriété canonique PidTagFreeBusyEntryIds

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient les **entryID** pour le message d’informations du délégué, le message de disponibilité de l’utilisateur connecté et le dossier dont **le PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) est égal à « FreeBusy Data ».
  
|Propriété|Valeur|
|:-----|:-----|
|Propriétés associées :  <br/> |PR_FREEBUSY_ENTRYIDS  <br/> |
|Identificateur :  <br/> |0x36E4  <br/> |
|Type de données :  <br/> |PT_MV_BINARY  <br/> |
|Domaine :  <br/> |Conteneur MAPI  <br/> |
   
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications de protocole

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des références aux spécifications de protocole Exchange Server associées.
    
[[MS-OXOPFFB]](https://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)
  
> Publie la disponibilité d’un utilisateur ou d’une ressource.
    
[[MS-OXODLGT]](https://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)
  
> Spécifie les méthodes de connexion et de configuration des boîtes aux lettres en tant que délégués, ainsi que les interactions avec les éléments de message et de calendrier lorsqu’ils agissent pour le compte d’un autre utilisateur.
    
[[MS-OXOSFLD]](https://msdn.microsoft.com/library/a60e9c16-2ba8-424b-b60c-385a8a2837cb%28Office.15%29.aspx)
  
> Spécifie les propriétés et les opérations de création et de localisation des dossiers spéciaux dans une boîte aux lettres.
    
### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
Mapitags.h
  
> Contient des définitions de propriétés répertoriées en tant que noms secondaires.
    
## <a name="see-also"></a>Voir aussi



[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage de noms MAPI à des noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

