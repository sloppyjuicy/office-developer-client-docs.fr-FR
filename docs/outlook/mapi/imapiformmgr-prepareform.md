---
title: IMAPIFormMgrPrepareForm
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormMgr.PrepareForm
api_type:
- COM
ms.assetid: 8f8ee2cb-1c2a-4958-b01e-2f4aab689f89
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: d0d5d8fe13a3c192dc0b0a8ddc0f5f945fa16f15
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32321811"
---
# <a name="imapiformmgrprepareform"></a>IMAPIFormMgr::PrepareForm

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Télécharge un formulaire à ouvrir.
  
```cpp
HRESULT PrepareForm(
  ULONG_PTR ulUIParam,
  ULONG ulFlags,
  LPMAPIFORMINFO pfrmiInfo
);
```

## <a name="parameters"></a>Paramètres

 _ulUIParam_
  
> dans Handle de la fenêtre parente de l'indicateur de progression qui est affiché pendant le téléchargement du formulaire. Le paramètre _ulUIParam_ est ignoré sauf si l'indicateur MAPI_DIALOG est défini dans le paramètre _ulFlags_ . 
    
 _ulFlags_
  
> dans Masque de des indicateurs qui contrôle le mode de téléchargement du formulaire. L'indicateur suivant peut être défini:
    
MAPI_DIALOG 
  
> Affiche une interface utilisateur pour fournir l'État ou inviter l'utilisateur à fournir des informations supplémentaires. Si cet indicateur n'est pas défini, aucune interface utilisateur n'est affichée.
    
 _pfrmiInfo_
  
> dans Pointeur vers un objet d'informations de formulaire pour le formulaire à télécharger.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.
    
## <a name="remarks"></a>Remarques

Les visionneuses de formulaires appellent la méthode **IMAPIFormMgr::P repareform** pour télécharger un formulaire à partir d'un conteneur de formulaire pour l'ouvrir. La plupart des visionneuses de formulaires n'ont pas besoin d'appeler **PrepareForm**, car les méthodes [IMAPIFormMgr:: CreateForm](imapiformmgr-createform.md) et [IMAPIFormMgr:: LoadForm](imapiformmgr-loadform.md) appellent **PrepareForm**, si nécessaire. 
  
Vous pouvez utiliser **PrepareForm** pour obtenir les bibliothèques de liens dynamiques (dll) et les autres fichiers associés à un formulaire afin de les modifier. Si le formulaire modifié est chargé à nouveau dans son conteneur de formulaire, il doit être réinstallé. 
  
## <a name="see-also"></a>Voir aussi



[IMAPIFormMgr::CreateForm](imapiformmgr-createform.md)
  
[IMAPIFormMgr::LoadForm](imapiformmgr-loadform.md)
  
[IMAPIFormMgr : IUnknown](imapiformmgriunknown.md)

