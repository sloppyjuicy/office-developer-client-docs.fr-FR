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
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 6e8ea7230ae86dee99cc4413715055fc53afa900
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22579724"
---
# <a name="imapiformmgrprepareform"></a>IMAPIFormMgr::PrepareForm

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Télécharge un formulaire d’ouverture.
  
```cpp
HRESULT PrepareForm(
  ULONG_PTR ulUIParam,
  ULONG ulFlags,
  LPMAPIFORMINFO pfrmiInfo
);
```

## <a name="parameters"></a>Paramètres

 _ulUIParam_
  
> [in] Un handle vers la fenêtre parent de l’indicateur de progression est affichée pendant que le formulaire est téléchargé. Le paramètre _ulUIParam_ est ignoré à moins que l’indicateur MAPI_DIALOG est défini dans le paramètre _ulFlags_ . 
    
 _ulFlags_
  
> [in] Masque de bits d’indicateurs qui contrôle la façon dont le formulaire est téléchargé. Vous pouvez définir l’indicateur suivant :
    
MAPI_DIALOG 
  
> Affiche une interface utilisateur pour fournir l’état ou demandez à l’utilisateur pour plus d’informations. Si cet indicateur n’est pas défini, aucune interface utilisateur est affichée.
    
 _pfrmiInfo_
  
> [in] Pointeur vers un objet d’informations de formulaire pour le formulaire à télécharger.
    
## <a name="return-value"></a>Valeur renvoy�e

S_OK 
  
> L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.
    
## <a name="remarks"></a>Remarques

Visionneuses de formulaire appeler la méthode **IMAPIFormMgr::PrepareForm** pour télécharger un formulaire à partir d’un conteneur de formulaire pour l’ouverture. La plupart des utilisateurs du formulaire est inutile d’appeler **PrepareForm**, car les [IMAPIFormMgr::CreateForm](imapiformmgr-createform.md) [IMAPIFormMgr::LoadForm](imapiformmgr-loadform.md) méthodes et appellent **PrepareForm**, si nécessaire. 
  
Vous pouvez utiliser **PrepareForm** pour obtenir les bibliothèques de liens dynamiques (DLL) et les autres fichiers associés à un formulaire pour les modifier. Si le formulaire modifié est chargé dans son conteneur de formulaire, il doit être réinstallé. 
  
## <a name="see-also"></a>Voir aussi



[IMAPIFormMgr::CreateForm](imapiformmgr-createform.md)
  
[IMAPIFormMgr::LoadForm](imapiformmgr-loadform.md)
  
[IMAPIFormMgr : IUnknown](imapiformmgriunknown.md)

