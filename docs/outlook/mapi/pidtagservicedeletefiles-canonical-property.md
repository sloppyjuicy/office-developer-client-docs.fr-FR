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
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: 236349a6b53eeb2f5c18c841c05cfb80a3fce824
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22580221"
---
# <a name="pidtagservicedeletefiles-canonical-property"></a>Propriété canonique PidTagServiceDeleteFiles

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Contient une liste des noms de fichiers qui doivent être supprimées lors de la désinstallation du service de message.
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_SERVICE_DELETE_FILES, PR_SERVICE_DELETE_FILES_A, PR_SERVICE_DELETE_FILES_W  <br/> |
|Identificateur :  <br/> |0x3D10  <br/> |
|Type de données :  <br/> |PT_MV_STRING8, PT_MV_UNICODE  <br/> |
|Domaine :  <br/> |Profil MAPI  <br/> |
   
## <a name="remarks"></a>Remarques

Les noms de fichiers dans la liste contenue dans ces propriétés sont supprimés de l’ordinateur lorsque vous utilisez le panneau de configuration pour désinstaller le service de message. N’incluez pas dans la liste des DLL qui prend en charge de plusieurs services de messagerie ou services de messagerie supplémentaires peuvent être supprimés par inadvertance.
  
MAPI ne fonctionne qu’avec les noms de fichiers et autres chaînes passé, dans le jeu de caractères ANSI. Les applications qui utilisent des noms de fichiers dans un jeu de caractères OEM doivent les convertir au format ANSI avant l’appel de MAPI.
  
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

