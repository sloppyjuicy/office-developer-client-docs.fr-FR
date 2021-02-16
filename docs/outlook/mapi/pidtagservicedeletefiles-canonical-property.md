---
title: Propriété canonique PidTagServiceDeleteFiles
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagServiceDeleteFiles
api_type:
- COM
ms.assetid: 9ec80a93-9e8f-46be-a1d4-7648aae47fec
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: da01385f83d9af9ad02eeb2fed08e3bc22d4df84
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436824"
---
# <a name="pidtagservicedeletefiles-canonical-property"></a>Propriété canonique PidTagServiceDeleteFiles

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient une liste de noms de fichiers qui doivent être supprimés lorsque le service de message est désinstallé.
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_SERVICE_DELETE_FILES, PR_SERVICE_DELETE_FILES_A, PR_SERVICE_DELETE_FILES_W  <br/> |
|Identificateur :  <br/> |0x3D10  <br/> |
|Type de données :  <br/> |PT_MV_STRING8, PT_MV_UNICODE  <br/> |
|Domaine :  <br/> |Profil MAPI  <br/> |
   
## <a name="remarks"></a>Remarques

Les noms de fichiers de la liste contenue dans ces propriétés sont supprimés de l’ordinateur lors de l’utilisation du panneau de contrôle pour désinstaller le service de message. N’incluez dans la liste aucune DLL qui prend en charge plusieurs services de message, ou des services de message supplémentaires peuvent être supprimés par inadvertance.
  
MAPI fonctionne uniquement avec les noms de fichiers et les autres chaînes qui lui sont passées, dans le jeu de caractères ANSI. Les applications qui utilisent des noms de fichiers dans un jeu de caractères OEM doivent les convertir en ANSI avant d’appeler MAPI.
  
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

