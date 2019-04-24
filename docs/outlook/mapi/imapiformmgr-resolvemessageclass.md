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
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: e99cff77fe872018722395c53c605e4d8fabfdde
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32321608"
---
# <a name="imapiformmgrresolvemessageclass"></a>IMAPIFormMgr::ResolveMessageClass

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Résout une classe de message sous sa forme dans un conteneur de formulaire et renvoie un objet d'informations de formulaire pour ce formulaire.
  
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
  
> dans Chaîne qui nomme la classe de message en cours de résolution.
    
 _ulFlags_
  
> dans Masque de des indicateurs qui contrôle la manière dont la classe de message est résolue. L'indicateur suivant peut être défini:
    
MAPIFORM_EXACTMATCH 
  
> Seules les chaînes de classe de message correspondant à une correspondance exacte doivent être résolues.
    
 _pFolderFocus_
  
> dans Pointeur vers le dossier qui contient le message en cours de résolution. Le paramètre _pFolderFocus_ peut être null. 
    
 _ppResult_
  
> remarquer Pointeur vers un pointeur vers un objet d'informations de formulaire renvoyé.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.
    
MAPI_E_NOT_FOUND 
  
> La classe de message passée dans le paramètre _szMsgClass_ ne correspond pas à la classe de message d'un formulaire de la bibliothèque de formulaires. 
    
## <a name="remarks"></a>Remarques

Les visionneuses de formulaires appellent la méthode **IMAPIFormMgr:: ResolveMessageClass** pour résoudre une classe de message en son formulaire dans un conteneur de formulaire. L'objet d'informations de formulaire renvoyé dans le paramètre _ppResult_ fournit un accès supplémentaire aux propriétés du formulaire qui a la classe de message donnée. 
  
## <a name="notes-to-callers"></a>Remarques pour les appelants

Pour résoudre une classe de message en formulaire, une visionneuse de formulaires transmet le nom de la classe de message à résoudre, par exemple `IPM.HelpDesk.Software`«». Pour forcer l'exactitude de la résolution (autrement dit, pour empêcher la résolution d'une classe de base de la classe de message lorsqu'un serveur de formulaires exactement correspondant n'est pas disponible), l'indicateur MAPIFORM_EXACTMATCH peut être passé dans le paramètre _ulFlags_ . Si le paramètre _pFolderFocus_ est null, le processus de résolution de classe de message n'effectue pas une recherche dans un conteneur de dossier. 
  
L'ordre des conteneurs recherchés dépend de l'implémentation du fournisseur de bibliothèque de formulaires. Le fournisseur de bibliothèque de formulaires par défaut recherche d'abord le conteneur local, puis le conteneur de dossier pour le dossier transmis, le conteneur de formulaire personnel et, enfin, le conteneur de l'organisation.
  
Les noms de classe de message sont toujours des chaînes ANSI, jamais Unicode.
  
L'identificateur de classe pour la classe de message résolue est renvoyé dans le cadre de l'objet d'informations de formulaire. Une visionneuse de formulaires ne doit pas agir en supposant que l'identificateur de classe existe dans la bibliothèque OLE jusqu'à ce que la visionneuse de formulaires ait appelé la méthode [IMAPIFormMgr::P repareform](imapiformmgr-prepareform.md) ou [IMAPIFormMgr:: CreateForm](imapiformmgr-createform.md) . 
  
## <a name="see-also"></a>Voir aussi



[IMAPIFormInfo : IMAPIProp](imapiforminfoimapiprop.md)
  
[IMAPIFormMgr::CreateForm](imapiformmgr-createform.md)
  
[IMAPIFormMgr::PrepareForm](imapiformmgr-prepareform.md)
  
[IMAPIFormMgr : IUnknown](imapiformmgriunknown.md)

