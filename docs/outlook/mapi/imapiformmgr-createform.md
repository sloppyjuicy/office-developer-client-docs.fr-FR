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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: c6e18ee9f8ea1d7dc6592d576c5a1163db526639
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32321664"
---
# <a name="imapiformmgrcreateform"></a>IMAPIFormMgr::CreateForm

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Ouvre un formulaire pour créer un message basé sur la classe de message du formulaire.
  
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
  
> dans Handle de la fenêtre parente de l'indicateur de progression qui est affiché pendant l'ouverture du formulaire. Le paramètre _ulUIParam_ est ignoré sauf si l'indicateur MAPI_DIALOG est défini dans le paramètre _ulFlags_ . 
    
 _ulFlags_
  
> dans Masque de des indicateurs qui contrôle le mode d'ouverture du formulaire. L'indicateur suivant peut être défini:
    
MAPI_DIALOG 
  
> Affiche une interface utilisateur pour fournir l'État ou inviter l'utilisateur à fournir des informations supplémentaires. Si cet indicateur n'est pas défini, aucune interface utilisateur n'est affichée.
    
 _pfrminfoToActivate_
  
> dans Pointeur vers l'objet d'informations de formulaire qui est utilisé pour ouvrir le formulaire.
    
 _refiidToAsk_
  
> dans Pointeur vers l'identificateur d'interface (IID) de l'interface à renvoyer pour l'objet Form qui a été créé. Le paramètre _refiidToAsk_ ne doit pas être null. 
    
 _ppvObj_
  
> remarquer Pointeur vers un pointeur vers l'interface renvoyée.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.
    
MAPI_E_NO_INTERFACE 
  
> L'interface demandée n'est pas prise en charge par l'objet Form.
    
## <a name="remarks"></a>Remarques

Les visionneuses de formulaires appellent la méthode **IMAPIFormMgr:: CreateForm** pour ouvrir un formulaire afin de créer un nouveau message basé sur la classe de message du formulaire. **CreateForm** ouvre le formulaire en créant une instance du serveur de formulaires pour ce formulaire, comme décrit dans l'objet d'information de formulaire donné. Si nécessaire, **CreateForm** appelle la méthode [IMAPIFormMgr::P repareform](imapiformmgr-prepareform.md) pour télécharger le code du serveur de formulaire sur le disque de l'utilisateur. 
  
Le paramètre _pfrminfoToActivate_ doit pointer vers un objet d'informations de formulaire qui a été résolu correctement. 
  
Une fois le formulaire ouvert, l'afficheur de formulaire appelant doit configurer un message à l'aide de l'interface [IPersistMessage](ipersistmessageiunknown.md) et éventuellement configurer un contexte d'affichage pour le formulaire. Pour plus d'informations, reportez-vous à [la rubrique lancement d'un serveur de formulaires](launching-a-form-server.md). 
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|MAPIFormFunctions. cpp  <br/> |CreateAndDisplayNewMailInFolder  <br/> |MFCMAPI utilise la méthode **IMAPIFormMgr:: CreateForm** pour créer un formulaire avant de l'afficher.  <br/> |
   
## <a name="see-also"></a>Voir aussi



[IMAPIFormMgr::PrepareForm](imapiformmgr-prepareform.md)
  
[IPersistMessage : IUnknown](ipersistmessageiunknown.md)
  
[IMAPIFormMgr : IUnknown](imapiformmgriunknown.md)


[MFCMAPI comme un exemple de Code](mfcmapi-as-a-code-sample.md)
  
[Lancement d'un serveur de formulaire](launching-a-form-server.md)

