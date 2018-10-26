---
title: IMAPIFormMgrResolveMessageClass
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormMgr.ResolveMessageClass
api_type:
- COM
ms.assetid: c2af7516-3a97-4422-874d-b1e3a0d4f316
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 3cd84e4ddb6d722d9f3de11d65b100d86e69ecae
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22571814"
---
# <a name="imapiformmgrresolvemessageclass"></a>IMAPIFormMgr::ResolveMessageClass

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Associe une classe de message à sa forme au sein d’un conteneur de formulaire et renvoie un objet d’informations de formulaire pour ce formulaire.
  
```cpp
HRESULT ResolveMessageClass(
  LPCSTR szMsgClass,
  ULONG ulFlags,
  LPMAPIFOLDER pFolderFocus,
  LPMAPIFORMINFO FAR * ppResult
);
```

## <a name="parameters"></a>Paramètres

 _szMsgClass_
  
> [in] Chaîne qui nomme la classe de message en cours de résolution.
    
 _ulFlags_
  
> [in] Masque de bits d’indicateurs qui contrôle la façon dont la classe de message est résolue. Vous pouvez définir l’indicateur suivant :
    
MAPIFORM_EXACTMATCH 
  
> Seules les chaînes de classe de message qui sont une correspondance exacte doivent être résolus.
    
 _pFolderFocus_
  
> [in] Pointeur vers le dossier qui contient le message en cours de résolution. Le paramètre _pFolderFocus_ peut être NULL. 
    
 _ppResult_
  
> [out] Pointeur vers un pointeur vers un objet d’informations de formulaire renvoyé.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.
    
MAPI_E_NOT_FOUND 
  
> La classe de message transmise dans le paramètre _szMsgClass_ ne correspond pas à la classe de message pour n’importe quel formulaire dans la bibliothèque de formulaires. 
    
## <a name="remarks"></a>Remarques

Visionneuses de formulaire appellent la méthode **IMAPIFormMgr::ResolveMessageClass** pour résoudre une classe de message à sa forme au sein d’un conteneur de formulaire. L’écran informations objet renvoyé dans le paramètre _ppResult_ fournit plus accès aux propriétés du formulaire avec la classe de message donné. 
  
## <a name="notes-to-callers"></a>Notes aux appelants

Pour résoudre une classe de message à un formulaire, une visionneuse de formulaire transmet le nom de la classe de message pour être résolu, tels que « `IPM.HelpDesk.Software`». Pour forcer la résolution à être exact (autrement dit, pour empêcher la résolution à une classe de base de la classe de message lorsqu’un formulaire correspondant exactement serveur n'est pas disponible), l’indicateur MAPIFORM_EXACTMATCH peut être passé dans le paramètre _ulFlags_ . Si le paramètre _pFolderFocus_ est NULL, le processus de résolution de classe de message ne recherche pas un conteneur de dossiers. 
  
L’ordre des conteneurs recherché dépend de l’implémentation du fournisseur de bibliothèque de formulaires. Le fournisseur de bibliothèque de formulaires par défaut recherche tout d’abord le conteneur local, puis le conteneur de dossier pour le dossier dans le passé, le conteneur de formulaires personnels et, enfin, le conteneur de l’organisation.
  
Noms de classe de message sont toujours des chaînes ANSI, Unicode jamais.
  
L’identificateur de classe pour la classe de message résolu est renvoyée dans le cadre de l’objet d’informations de formulaire. Une visionneuse de formulaire ne doit pas fonctionner sur en partant du principe que l’identificateur de classe existe dans la bibliothèque OLE jusqu'à une fois la visionneuse de formulaire a appelé la méthode [IMAPIFormMgr::PrepareForm](imapiformmgr-prepareform.md) ou la méthode [IMAPIFormMgr::CreateForm](imapiformmgr-createform.md) . 
  
## <a name="see-also"></a>Voir aussi



[IMAPIFormInfo : IMAPIProp](imapiforminfoimapiprop.md)
  
[IMAPIFormMgr::CreateForm](imapiformmgr-createform.md)
  
[IMAPIFormMgr::PrepareForm](imapiformmgr-prepareform.md)
  
[IMAPIFormMgr : IUnknown](imapiformmgriunknown.md)

