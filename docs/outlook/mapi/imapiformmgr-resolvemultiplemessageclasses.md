---
title: IMAPIFormMgrResolveMultipleMessageClasses
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormMgr.ResolveMultipleMessageClasses
api_type:
- COM
ms.assetid: d3cc6658-e46d-42dd-b1ac-65c88cfef8ca
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 968be38e794793405aac15340a92ccd6d680498d
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22571695"
---
# <a name="imapiformmgrresolvemultiplemessageclasses"></a>IMAPIFormMgr::ResolveMultipleMessageClasses

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Résout un groupe de classes de message à leurs formulaires dans un conteneur de formulaire et renvoie un tableau de formulaire objets des informations pour les formulaires.
  
```cpp
HRESULT ResolveMultipleMessageClasses(
  LPSMESSAGECLASSARRAY pMsgClasses,
  ULONG ulFlags,
  LPMAPIFOLDER pFolderFocus,
  LPSMAPIFORMINFOARRAY FAR * ppfrminfoarray
);
```

## <a name="parameters"></a>Paramètres

 _pMsgClasses_
  
> [in] Pointeur vers un tableau qui contient les noms des classes de message à résoudre.
    
 _ulFlags_
  
> [in] Masque de bits d’indicateurs qui contrôle la façon dont les classes de message sont résolus. Vous pouvez définir l’indicateur suivant :
    
MAPIFORM_EXACTMATCH 
  
> Seules les chaînes de classe de message qui sont une correspondance exacte doivent être résolus.
    
MAPIFORM_LOCALONLY
  
> N’incluez pas de formulaires mis en cache.
    
 _pFolderFocus_
  
> [in] Pointeur vers le dossier qui contient le formulaire dont la classe de message est résolue. Le paramètre _pFolderFocus_ peut être NULL. 
    
 _ppfrminfoarray_
  
> [out] Pointeur vers un pointeur vers un tableau d’objets d’informations de formulaire. Si une visionneuse de formulaire passe NULL dans le paramètre _pMsgClasses_ , le paramètre _ppfrminfoarray_ contient des objets d’informations de formulaire pour tous les formulaires dans le conteneur. 
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.
    
## <a name="remarks"></a>Remarques

Visionneuses de formulaire appellent la méthode **IMAPIFormMgr::ResolveMultipleMessageClasses** pour résoudre un groupe de classes de message pour des formulaires dans un conteneur de formulaire. Le tableau d’objets formulaire renvoyé dans _ppfrminfoarray_ fournit davantage l’accès à chacune des propriétés des formulaires. 
  
## <a name="notes-to-callers"></a>Notes aux appelants

Pour résoudre un groupe de classes de message aux formulaires, une visionneuse de formulaire transmet dans un tableau de résolution des noms de classe de message. Pour forcer la résolution à être exact (autrement dit, pour empêcher la résolution à une classe de base de la classe de message lorsqu’un formulaire correspondant exactement serveur n'est pas disponible) l’indicateur MAPIFORM_EXACTMATCH peut être passé dans le paramètre _ulFlags_ . 
  
Noms de classe de message sont toujours des chaînes ANSI, Unicode jamais.
  
Si une classe de message ne peut pas être résolue à un formulaire, NULL est renvoyé pour cette classe de message dans le tableau d’informations de formulaire. Par conséquent, même si la méthode renvoie S_OK, les visionneuses de formulaire devraient fonctionner pas sur l’hypothèse que toutes les classes de message ont été correctement résolus. Au lieu de cela, les visionneuses de formulaire doivent vérifier les valeurs dans le tableau retourné.
  
## <a name="see-also"></a>Voir aussi



[IMAPIFormMgr::ResolveMessageClass](imapiformmgr-resolvemessageclass.md)
  
[IMAPIFormMgr : IUnknown](imapiformmgriunknown.md)

