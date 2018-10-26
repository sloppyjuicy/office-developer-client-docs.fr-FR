---
title: IMAPIFormMgrCreateForm
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormMgr.CreateForm
api_type:
- COM
ms.assetid: 7d4d50f8-3904-4e93-a535-ac7decceb1a3
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: e86c3d9678739c09024c0655cbbbb702749a53f0
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22586164"
---
# <a name="imapiformmgrcreateform"></a>IMAPIFormMgr::CreateForm

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Ouvre un formulaire pour créer un nouveau message en fonction de la classe de message du formulaire.
  
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
  
> [in] Un handle vers la fenêtre parent pour l’indicateur de progression est affichée pendant que le formulaire est ouvert. Le paramètre _ulUIParam_ est ignoré à moins que l’indicateur MAPI_DIALOG est défini dans le paramètre _ulFlags_ . 
    
 _ulFlags_
  
> [in] Masque de bits d’indicateurs qui contrôle la façon dont le formulaire est ouvert. Vous pouvez définir l’indicateur suivant :
    
MAPI_DIALOG 
  
> Affiche une interface utilisateur pour fournir l’état ou demandez à l’utilisateur pour plus d’informations. Si cet indicateur n’est pas défini, aucune interface utilisateur est affichée.
    
 _pfrminfoToActivate_
  
> [in] Pointeur vers l’objet d’informations de formulaire qui est utilisée pour ouvrir le formulaire.
    
 _refiidToAsk_
  
> [in] Pointeur vers l’identificateur d’interface (IID) pour l’interface à renvoyer à partir de l’objet de formulaire qui a été créé. Le paramètre _refiidToAsk_ ne doit pas être NULL. 
    
 _ppvObj_
  
> [out] Pointeur vers un pointeur vers l’interface retournée.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.
    
MAPI_E_NO_INTERFACE 
  
> L’interface demandée n’est pas pris en charge par l’objet de formulaire.
    
## <a name="remarks"></a>Remarques

Visionneuses de formulaire appeler la méthode **IMAPIFormMgr::CreateForm** pour ouvrir un formulaire pour créer un nouveau message en fonction de la classe de message du formulaire. **CreateForm** ouvre le formulaire en créant une instance du serveur de formulaire pour ce formulaire comme décrit dans l’objet d’informations de formulaire donné. Si nécessaire, **CreateForm** appelle la méthode [IMAPIFormMgr::PrepareForm](imapiformmgr-prepareform.md) pour télécharger le code du formulaire sur le disque de l’utilisateur. 
  
Le paramètre _pfrminfoToActivate_ doit pointer sur un objet d’informations de formulaire qui a été correctement résolu. 
  
Une fois que le formulaire a été ouvert, la visionneuse de formulaire appelant doit configurer un message à l’aide de l’interface [IPersistMessage](ipersistmessageiunknown.md) et permettre éventuellement configurer un contexte de vue pour le formulaire. Pour plus d’informations, voir [lancement d’un serveur de formulaire](launching-a-form-server.md). 
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|MAPIFormFunctions.cpp  <br/> |CreateAndDisplayNewMailInFolder  <br/> |MFCMAPI utilise la méthode **IMAPIFormMgr::CreateForm** pour créer un formulaire avant de les afficher.  <br/> |
   
## <a name="see-also"></a>Voir aussi



[IMAPIFormMgr::PrepareForm](imapiformmgr-prepareform.md)
  
[IPersistMessage : IUnknown](ipersistmessageiunknown.md)
  
[IMAPIFormMgr : IUnknown](imapiformmgriunknown.md)


[MFCMAPI en tant qu’exemple de code](mfcmapi-as-a-code-sample.md)
  
[Lancement d’un serveur de formulaire](launching-a-form-server.md)

