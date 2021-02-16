---
title: IMAPIFormContainerResolveMessageClass
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormContainer.ResolveMessageClass
api_type:
- COM
ms.assetid: 9ce13f11-5787-4ea5-a84f-b1e3824529ee
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: c0954d6f8b14b4088ece2ac276b045b6c163ed98
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408550"
---
# <a name="imapiformcontainerresolvemessageclass"></a>IMAPIFormContainer::ResolveMessageClass

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Résout une classe de message dans son formulaire dans un conteneur de formulaires et renvoie un objet d’informations de formulaire pour ce formulaire.
  
```cpp
HRESULT ResolveMessageClass(
  LPCSTR szMessageClass,
  ULONG ulFlags,
  LPMAPIFORMINFO FAR * ppforminfo
);
```

## <a name="parameters"></a>Paramètres

 _szMessageClass_
  
> [in] Chaîne qui nomme la classe de message en cours de résolution. Les noms de classe de message sont toujours des chaînes ANSI, jamais Unicode.
    
 _ulFlags_
  
> [in] Masque de bits d’indicateurs qui contrôle la façon dont la classe de message est résolue. L’indicateur suivant peut être définie :
    
MAPIFORM_EXACTMATCH 
  
> Seules les chaînes de classe de message qui correspondent exactement doivent être résolues.
    
 _ppforminfo_
  
> [out] Pointeur vers un pointeur vers l’objet d’informations du formulaire renvoyé.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.
    
MAPI_E_NOT_FOUND 
  
> La classe de message transmise dans le  _paramètre szMessageClass_ ne correspond à la classe de message pour aucun formulaire dans le conteneur de formulaire. 
    
## <a name="remarks"></a>Remarques

Les applications clientes appellent la méthode **IMAPIFormContainer::ResolveMessageClass** pour résoudre une classe de message en formulaire dans un conteneur de formulaire. L’objet informations du formulaire renvoyé dans le  _paramètre ppforminfo_ fournit un accès supplémentaire aux propriétés du formulaire avec la classe de message donnée. 
  
## <a name="notes-to-callers"></a>Remarques pour les appelants

Pour résoudre une classe de message en formulaire, passez le nom de la classe de message à résoudre (par exemple,  `IPM.HelpDesk.Software` ). Pour forcer la résolution à être exacte (c’est-à-dire pour empêcher la résolution à une classe de base de la classe de message), l’indicateur MAPIFORM_EXACTMATCH peut être transmis dans le paramètre _ulFlags._ 
  
L’identificateur de classe pour la classe de message résolue est renvoyé dans le cadre de l’objet d’informations du formulaire. Ne supposez pas que l’identificateur de classe existe dans la bibliothèque OLE tant que vous n’avez pas appelé la méthode [IMAPIFormMgr::P repareForm](imapiformmgr-prepareform.md) ou [IMAPIFormMgr::CreateForm.](imapiformmgr-createform.md) 
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|FormContainerDlg.cpp  <br/> |CFormContainerDlg::OnResolveMessageClass  <br/> |MFCMAPI utilise la méthode **IMAPIFormContainer::ResolveMessageClass** pour localiser un formulaire associé à une classe de message.  <br/> |
   
## <a name="see-also"></a>Voir aussi



[IMAPIFormInfo : IMAPIProp](imapiforminfoimapiprop.md)
  
[IMAPIFormMgr::CreateForm](imapiformmgr-createform.md)
  
[IMAPIFormMgr::PrepareForm](imapiformmgr-prepareform.md)
  
[IMAPIFormContainer : IUnknown](imapiformcontaineriunknown.md)

