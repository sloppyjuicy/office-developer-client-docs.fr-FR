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
ms.openlocfilehash: 515061c6c208008c4752e5ff2f23933a4c259c00
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428017"
---
# <a name="imapiformmgrresolvemultiplemessageclasses"></a>IMAPIFormMgr::ResolveMultipleMessageClasses

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Résout un groupe de classes de message dans leurs formulaires dans un conteneur de formulaires et renvoie un tableau d’objets d’informations de formulaire pour ces formulaires.
  
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
  
> [in] Masque de bits d’indicateurs qui contrôle la façon dont les classes de message sont résolues. L’indicateur suivant peut être définie :
    
MAPIFORM_EXACTMATCH 
  
> Seules les chaînes de classe de message qui correspondent exactement doivent être résolues.
    
MAPIFORM_LOCALONLY
  
> N’incluez pas les formulaires mis en cache.
    
 _pFolderFocus_
  
> [in] Pointeur vers le dossier qui contient le formulaire dont la classe de message est en cours de résolution. Le  _paramètre pFolderFocus_ peut être NULL. 
    
 _ppfrminfoarray_
  
> [out] Pointeur vers un pointeur vers un tableau d’objets d’informations de formulaire. Si une visionneuse de formulaire transmet la valeur NULL dans le paramètre  _pMsgClasses,_ le paramètre  _ppfrminfoarray_ contient des objets d’informations de formulaire pour tous les formulaires dans le conteneur. 
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.
    
## <a name="remarks"></a>Remarques

Les visionneuses de formulaires appellent la méthode **IMAPIFormMgr::ResolveMultipleMessageClasses** pour résoudre un groupe de classes de message en formulaires dans un conteneur de formulaires. Le tableau des objets d’informations de formulaire renvoyés dans  _ppfrminfoarray_ fournit un accès supplémentaire à chacune des propriétés des formulaires. 
  
## <a name="notes-to-callers"></a>Remarques pour les appelants

Pour résoudre un groupe de classes de message en formulaires, une visionneuse de formulaires transmet un tableau de noms de classes de messages à résoudre. Pour forcer la résolution à être exacte (c’est-à-dire pour empêcher la résolution à une classe de base de la classe de message lorsqu’un serveur de formulaires correspondant exactement n’est pas disponible), l’indicateur MAPIFORM_EXACTMATCH peut être transmis dans le paramètre _ulFlags._ 
  
Les noms de classe de message sont toujours des chaînes ANSI, jamais Unicode.
  
Si une classe de message ne peut pas être résolue en formulaire, la valeur NULL est renvoyée pour cette classe de message dans le tableau d’informations du formulaire. Par conséquent, même si la méthode renvoie S_OK, les visionneuses de formulaires ne doivent pas fonctionner sur l’hypothèse que toutes les classes de message ont été correctement résolues. Au lieu de cela, les visionneuses de formulaire doivent vérifier les valeurs dans le tableau renvoyé.
  
## <a name="see-also"></a>Voir aussi



[IMAPIFormMgr::ResolveMessageClass](imapiformmgr-resolvemessageclass.md)
  
[IMAPIFormMgr : IUnknown](imapiformmgriunknown.md)

