---
title: Propriété canonique PidTagServiceSupportFiles
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.PidTagServiceSupportFiles
api_type:
- COM
ms.assetid: df4be986-62a8-49d6-8eca-25b55c74f830
description: Contient une liste des fichiers qui appartiennent au service de message. MAPI fonctionne uniquement avec les noms de fichiers et les autres chaînes qui lui sont passées, dans le jeu de caractères ANSI.
ms.openlocfilehash: fb1efaa09f823c4bb717c10661c106d8e7b33bc4
ms.sourcegitcommit: 331e2bc18fb14cc9868d28ca29cb5eda85c8f154
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/25/2022
ms.locfileid: "64455572"
---
# <a name="pidtagservicesupportfiles-canonical-property"></a>Propriété canonique PidTagServiceSupportFiles

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient une liste des fichiers qui appartiennent au service de message.
  
|Propriété |Valeur |
|:-----|:-----|
|Propriétés associées :  <br/> |PR_SERVICE_SUPPORT_FILES, PR_SERVICE_SUPPORT_FILES_A, PR_SERVICE_SUPPORT_FILES_W  <br/> |
|Identificateur :  <br/> |0x3D0F  <br/> |
|Type de données :  <br/> |PT_MV_STRING8, PT_MV_UNICODE  <br/> |
|Domaine :  <br/> |Profil MAPI  <br/> |
   
## <a name="remarks"></a>Remarques

À l’aide d’une boîte de dialogue dans l’applet du panneau de contrôle, un utilisateur peut obtenir la liste des fichiers qui appartiennent au service de message. Par exemple, l’utilisateur peut obtenir les noms de toutes les bibliothèques de liens dynamiques (DLL) qui appartiennent au service. L’utilisateur peut ensuite rechercher des détails supplémentaires sur les fichiers spécifiés, tels que les noms et numéros de version de toutes les DLL. MAPI utilise ces propriétés pour créer une liste de fichiers de prise en charge dans une boîte de dialogue pour la sélection de l’utilisateur de messagerie.
  
MAPI fonctionne uniquement avec les noms de fichiers et les autres chaînes qui lui sont passées, dans le jeu de caractères ANSI (Active Directory Service Interfaces). Les applications clientes qui utilisent des noms de fichiers dans un jeu de caractères OEM (Original Equipment Manufacturer) doivent les convertir en ANSI avant d’appeler MAPI.
  
## <a name="related-resources"></a>Ressources connexes

### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
Mapitags.h
  
> Contient les définitions des propriétés répertoriées en tant que noms de remplacement.
    
## <a name="see-also"></a>Voir aussi



[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage des noms MAPI aux noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

