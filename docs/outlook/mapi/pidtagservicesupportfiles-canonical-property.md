---
title: Propriété canonique PidTagServiceSupportFiles
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagServiceSupportFiles
api_type:
- COM
ms.assetid: df4be986-62a8-49d6-8eca-25b55c74f830
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: 5165867e46d3d86d65932e7ae432b446efbd8fff
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22589125"
---
# <a name="pidtagservicesupportfiles-canonical-property"></a>Propriété canonique PidTagServiceSupportFiles

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Contient une liste des fichiers qui appartiennent au service de message.
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_SERVICE_SUPPORT_FILES, PR_SERVICE_SUPPORT_FILES_A, PR_SERVICE_SUPPORT_FILES_W  <br/> |
|Identificateur :  <br/> |0x3D0F  <br/> |
|Type de données :  <br/> |PT_MV_STRING8, PT_MV_UNICODE  <br/> |
|Domaine :  <br/> |Profil MAPI  <br/> |
   
## <a name="remarks"></a>Remarques

À l’aide d’une boîte de dialogue dans le panneau, un utilisateur peut obtenir la liste des fichiers qui appartiennent au service de message. Par exemple, l’utilisateur peut obtenir les noms de toutes les bibliothèques de liens dynamiques (DLL) qui appartiennent au service. L’utilisateur peut rechercher puis plus d’informations sur les fichiers spécifiés, tels que les noms et les numéros de version de toutes les DLL. MAPI utilise ces propriétés pour créer une liste de fichiers de prise en charge dans une boîte de dialogue de sélection de l’utilisateur de messagerie.
  
MAPI ne fonctionne qu’avec les noms de fichiers et autres chaînes passé, dans le jeu de caractères Active Directory Service Interfaces (ANSI). Les applications clientes qui utilisent des noms de fichiers dans un jeu de caractères OEM (OEM) doivent les convertir au format ANSI avant l’appel de MAPI.
  
## <a name="related-resources"></a>Ressources connexes

### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
MAPITAGS.h
  
> Contient les définitions des propriétés répertoriées en tant que d’autres noms.
    
## <a name="see-also"></a>Voir aussi



[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage des noms MAPI aux noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

