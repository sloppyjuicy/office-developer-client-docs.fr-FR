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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 3753177552d45e32e53ae192a9dfae15b601afcc
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417041"
---
# <a name="pidtagservicesupportfiles-canonical-property"></a>Propriété canonique PidTagServiceSupportFiles

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient une liste des fichiers qui appartiennent au service de messagerie.
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_SERVICE_SUPPORT_FILES, PR_SERVICE_SUPPORT_FILES_A, PR_SERVICE_SUPPORT_FILES_W  <br/> |
|Identificateur :  <br/> |0x3D0F  <br/> |
|Type de données :  <br/> |PT_MV_STRING8, PT_MV_UNICODE  <br/> |
|Domaine :  <br/> |Profil MAPI  <br/> |
   
## <a name="remarks"></a>Remarques

À l'aide d'une boîte de dialogue de l'applet du panneau de configuration, un utilisateur peut obtenir la liste des fichiers qui appartiennent au service de messagerie. Par exemple, l'utilisateur peut obtenir les noms de toutes les bibliothèques de liens dynamiques (dll) qui appartiennent au service. L'utilisateur peut ensuite Rechercher des détails supplémentaires sur les fichiers spécifiés, tels que les noms et les numéros de version de toutes les dll. MAPI utilise les propriétés suivantes pour créer une liste de fichiers de prise en charge dans une boîte de dialogue pour la sélection de l'utilisateur de messagerie.
  
MAPI fonctionne uniquement avec les noms de fichier et les autres chaînes qui lui sont transmises, dans le jeu de caractères ANSI (Active Directory Service Interfaces). Les applications clientes qui utilisent des noms de fichier dans un jeu de caractères OEM (Original Equipment Manufacturer) doivent les convertir en ANSI avant d'appeler MAPI.
  
## <a name="related-resources"></a>Ressources connexes

### <a name="header-files"></a>Fichiers d'en-tête

Mapidefs. h
  
> Fournit des définitions de type de données.
    
Mapitags. h
  
> Contient les définitions des propriétés figurant en tant que noms de substitution.
    
## <a name="see-also"></a>Voir aussi



[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage des noms MAPI aux noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

