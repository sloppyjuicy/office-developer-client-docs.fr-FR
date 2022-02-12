---
title: IMAPIFormMgrCreateForm
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPIFormMgr.CreateForm
api_type:
- COM
ms.assetid: 7d4d50f8-3904-4e93-a535-ac7decceb1a3
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 1b1c98ddeaed876f29a3cc5bb32f5065d00d3dfe
ms.sourcegitcommit: c0fae34cd3a9c75a7cffcf9ae8e417ddde07a989
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/12/2022
ms.locfileid: "62784110"
---
# <a name="imapiformmgrcreateform"></a>IMAPIFormMgr::CreateForm

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Ouvre un formulaire pour créer un message en fonction de la classe de message du formulaire.
  
```cpp
HRESULT CreateForm(
  ULONG_PTR ulUIParam,
  ULONG ulFlags,
  IMAPIFormInfo pfrminfoToActivate,
  REFIID refiidToAsk,
  LPVOID FAR * ppvObj
);
```

## <a name="parameters"></a>Paramètres

 _ulUIParam_
  
> [in] Poignée vers la fenêtre parente de l’indicateur de progression qui s’affiche pendant l’ouverture du formulaire. Le  _paramètre ulUIParam_ est ignoré, sauf si l’MAPI_DIALOG est définie dans _le paramètre ulFlags_ . 
    
 _ulFlags_
  
> [in] Masque de bits d’indicateurs qui contrôle la façon dont le formulaire est ouvert. L’indicateur suivant peut être définie :
    
MAPI_DIALOG 
  
> Affiche une interface utilisateur pour fournir un état ou invite l’utilisateur à fournir plus d’informations. Si cet indicateur n’est pas définie, aucune interface utilisateur n’est affichée.
    
 _pfrminfoToActivate_
  
> [in] Pointeur vers l’objet d’informations du formulaire utilisé pour ouvrir le formulaire.
    
 _refiidToAsk_
  
> [in] Pointeur vers l’identificateur d’interface (IID) de l’interface à retourner pour l’objet de formulaire qui a été créé. Le  _paramètre refiidToAsk_ ne doit pas être NULL. 
    
 _ppvObj_
  
> [out] Pointeur vers un pointeur vers l’interface renvoyée.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.
    
MAPI_E_NO_INTERFACE 
  
> L’interface demandée n’est pas prise en charge par l’objet formulaire.
    
## <a name="remarks"></a>Remarques

Les visionneuses de formulaire appellent la méthode **IMAPIFormMgr::CreateForm** pour ouvrir un formulaire afin de créer un message en fonction de la classe de message du formulaire. **CreateForm** ouvre le formulaire en créant une instance du serveur de formulaire pour ce formulaire, comme décrit dans l’objet d’informations du formulaire donné. Si nécessaire, **CreateForm** appelle la méthode [IMAPIFormMgr::P repareForm](imapiformmgr-prepareform.md) pour télécharger le code du serveur de formulaire sur le disque de l’utilisateur. 
  
Le  _paramètre pfrminfoToActivate doit_ pointer vers un objet d’informations de formulaire qui a été correctement résolu. 
  
Une fois le formulaire ouvert, la visionneuse de formulaire appelant doit configurer un message à l’aide de l’interface [IPersistMessage](ipersistmessageiunknown.md) et peut éventuellement configurer un contexte d’affichage pour le formulaire. Pour plus d’informations, voir [Lancement d’un serveur de formulaires](launching-a-form-server.md). 
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|MAPIFormFunctions.cpp  <br/> |CreateAndDisplayNewMailInFolder  <br/> |MFCMAPI utilise la **méthode IMAPIFormMgr::CreateForm** pour créer un formulaire avant de l’afficher. |
   
## <a name="see-also"></a>Voir aussi



[IMAPIFormMgr::PrepareForm](imapiformmgr-prepareform.md)
  
[IPersistMessage : IUnknown](ipersistmessageiunknown.md)
  
[IMAPIFormMgr : IUnknown](imapiformmgriunknown.md)


[MFCMAPI comme un exemple de Code](mfcmapi-as-a-code-sample.md)
  
[Lancement d’un serveur de formulaires](launching-a-form-server.md)

