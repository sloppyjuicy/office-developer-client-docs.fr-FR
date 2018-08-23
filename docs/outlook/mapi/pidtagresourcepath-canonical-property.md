---
title: Propriété canonique PidTagResourcePath
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagResourcePath
api_type:
- COM
ms.assetid: ac49538e-6ee8-4ab4-9d79-88a83c7d0149
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: a00abec7627eb12e23e7b76f5d0900514d710ffb
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22593094"
---
# <a name="pidtagresourcepath-canonical-property"></a>Propriété canonique PidTagResourcePath

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Contient un chemin d’accès au serveur du fournisseur de services.
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_RESOURCE_PATH, PR_RESOURCE_PATH_A, PR_RESOURCE_PATH_W  <br/> |
|Identificateur :  <br/> |0x3E07  <br/> |
|Type de données :  <br/> |PT_STRING8, PT_UNICODE  <br/> |
|Domaine :  <br/> |État MAPI  <br/> |
   
## <a name="remarks"></a>Remarques

Le chemin d’accès contenue dans ces propriétés représente le chemin d’accès suggéré dans laquelle l’utilisateur peut trouver des ressources. La définition de ces propriétés est spécifique au fournisseur. Par exemple, une application de planification utilise ces propriétés pour spécifier l’emplacement proposé pour ses fichiers d’application de planification.
  
Le profil utilisateur de messagerie fournit ces propriétés commodité afin qu’une application cliente n’a pas demander à l’utilisateur de messagerie pour un chemin d’accès réseau ou d’une lettre de lecteur réseau.
  
MAPI ne fonctionne qu’avec les noms de fichiers dans le jeu de caractères National Institute ANSI (American Standards). Les applications qui utilisent des noms de fichiers dans un jeu de caractères OEM (OEM) doivent les convertir au format ANSI avant l’appel de MAPI.
  
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

