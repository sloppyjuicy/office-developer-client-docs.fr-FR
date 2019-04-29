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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 32d150e508f5c208e15d5ee5f0b8c800a1e597f9
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429858"
---
# <a name="pidtagresourcepath-canonical-property"></a>Propriété canonique PidTagResourcePath

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient un chemin d'accès au serveur du fournisseur de services.
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_RESOURCE_PATH, PR_RESOURCE_PATH_A, PR_RESOURCE_PATH_W  <br/> |
|Identificateur :  <br/> |0x3E07  <br/> |
|Type de données :  <br/> |PT_STRING8, PT_UNICODE  <br/> |
|Domaine :  <br/> |État MAPI  <br/> |
   
## <a name="remarks"></a>Remarques

Le chemin d'accès contenu dans ces propriétés représente le chemin d'accès suggéré dans lequel l'utilisateur peut trouver des ressources. La définition de ces propriétés est spécifique au fournisseur. Par exemple, une application de planification utilise ces propriétés pour spécifier l'emplacement suggéré pour ses fichiers d'application de planification.
  
Le profil utilisateur de messagerie fournit ces propriétés pour qu'une application cliente n'ait pas besoin d'inviter l'utilisateur de messagerie à indiquer un chemin d'accès réseau ou une lettre de lecteur réseau.
  
MAPI ne fonctionne qu'avec les noms de fichier dans le jeu de caractères ANSI (American National Standards Institute). Les applications qui utilisent des noms de fichier dans un jeu de caractères OEM (Original Equipment Manufacturer) doivent les convertir en ANSI avant d'appeler MAPI.
  
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

