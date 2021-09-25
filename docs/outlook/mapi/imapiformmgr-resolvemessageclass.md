---
title: IMAPIFormMgrResolveMessageClass
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPIFormMgr.ResolveMessageClass
api_type:
- COM
ms.assetid: c2af7516-3a97-4422-874d-b1e3a0d4f316
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 8ea8a07c8b299c254fbbb8fd914838c916c5684f
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59596205"
---
# <a name="imapiformmgrresolvemessageclass"></a>IMAPIFormMgr::ResolveMessageClass

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Résout une classe de message dans son formulaire dans un conteneur de formulaire et renvoie un objet d’informations de formulaire pour ce formulaire.
  
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
  
> [in] Masque de bits d’indicateurs qui contrôle la façon dont la classe de message est résolue. L’indicateur suivant peut être définie :
    
MAPIFORM_EXACTMATCH 
  
> Seules les chaînes de classe de message qui correspondent exactement doivent être résolues.
    
 _pFolderFocus_
  
> [in] Pointeur vers le dossier qui contient le message en cours de résolution. Le  _paramètre pFolderFocus_ peut être NULL. 
    
 _ppResult_
  
> [out] Pointeur vers un pointeur vers un objet d’informations de formulaire renvoyé.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.
    
MAPI_E_NOT_FOUND 
  
> La classe de message transmise dans le paramètre  _szMsgClass_ ne correspond à la classe de message pour aucun formulaire de la bibliothèque de formulaires. 
    
## <a name="remarks"></a>Remarques

Les visionneuses de formulaire appellent la méthode **IMAPIFormMgr::ResolveMessageClass** pour résoudre une classe de message dans son formulaire dans un conteneur de formulaire. L’objet informations du formulaire renvoyé dans le  _paramètre ppResult_ fournit un accès supplémentaire aux propriétés du formulaire qui possède la classe de message donnée. 
  
## <a name="notes-to-callers"></a>Remarques pour les appelants

Pour résoudre une classe de message en formulaire, une visionneuse de formulaire transmet le nom de la classe de message à résoudre, tel que « `IPM.HelpDesk.Software` ». Pour forcer la résolution à être exacte (c’est-à-dire pour empêcher la résolution à une classe de base de la classe de message lorsqu’un serveur de formulaires correspondant exactement n’est pas disponible), l’indicateur MAPIFORM_EXACTMATCH peut être transmis dans le paramètre _ulFlags._ Si le  _paramètre pFolderFocus_ est NULL, le processus de résolution de classe de message ne recherche pas un conteneur de dossiers. 
  
L’ordre des conteneurs recherchés dépend de l’implémentation du fournisseur de bibliothèque de formulaires. Le fournisseur de bibliothèque de formulaires par défaut recherche d’abord le conteneur local, puis le conteneur de dossiers pour le dossier transmis, le conteneur de formulaire personnel et, enfin, le conteneur d’organisation.
  
Les noms de classe de message sont toujours des chaînes ANSI, jamais Unicode.
  
L’identificateur de classe de la classe de message résolue est renvoyé dans le cadre de l’objet d’informations du formulaire. Une visionneuse de formulaire ne doit pas fonctionner sur l’hypothèse que l’identificateur de classe existe dans la bibliothèque OLE tant que la visionneuse n’a pas appelé la méthode [IMAPIFormMgr::P repareForm](imapiformmgr-prepareform.md) ou [IMAPIFormMgr::CreateForm.](imapiformmgr-createform.md) 
  
## <a name="see-also"></a>Voir aussi



[IMAPIFormInfo : IMAPIProp](imapiforminfoimapiprop.md)
  
[IMAPIFormMgr::CreateForm](imapiformmgr-createform.md)
  
[IMAPIFormMgr::PrepareForm](imapiformmgr-prepareform.md)
  
[IMAPIFormMgr : IUnknown](imapiformmgriunknown.md)

