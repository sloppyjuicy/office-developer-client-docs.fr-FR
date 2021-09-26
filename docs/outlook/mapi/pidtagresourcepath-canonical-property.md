---
title: Propriété canonique PidTagResourcePath
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.PidTagResourcePath
api_type:
- COM
ms.assetid: ac49538e-6ee8-4ab4-9d79-88a83c7d0149
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 04ecec1e220af4afcf40fe37fe5e3d90cf943720
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59599599"
---
# <a name="pidtagresourcepath-canonical-property"></a>Propriété canonique PidTagResourcePath

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient un chemin d’accès au serveur du fournisseur de services.
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_RESOURCE_PATH, PR_RESOURCE_PATH_A, PR_RESOURCE_PATH_W  <br/> |
|Identificateur :  <br/> |0x3E07  <br/> |
|Type de données :  <br/> |PT_STRING8, PT_UNICODE  <br/> |
|Domaine :  <br/> |État MAPI  <br/> |
   
## <a name="remarks"></a>Remarques

Le chemin d’accès contenu dans ces propriétés représente le chemin d’accès suggéré où l’utilisateur peut trouver des ressources. La définition de ces propriétés est spécifique au fournisseur. Par exemple, une application de planification utilise ces propriétés pour spécifier l’emplacement suggéré pour ses fichiers d’application de planification.
  
Le profil utilisateur de messagerie fournit ces propriétés par commodité afin qu’une application cliente n’a pas besoin d’inviter l’utilisateur de messagerie pour un chemin d’accès réseau ou une lettre de lecteur réseau.
  
MAPI fonctionne uniquement avec les noms de fichiers dans le jeu de caractères ANSI (American National Standards Institute). Les applications qui utilisent des noms de fichiers dans un jeu de caractères OEM (Original Equipment Manufacturer) doivent les convertir en ANSI avant d’appeler MAPI.
  
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

