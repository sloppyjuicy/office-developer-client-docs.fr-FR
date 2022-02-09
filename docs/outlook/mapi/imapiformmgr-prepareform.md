---
title: IMAPIFormMgrPrepareForm
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPIFormMgr.PrepareForm
api_type:
- COM
ms.assetid: 8f8ee2cb-1c2a-4958-b01e-2f4aab689f89
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 138f2c0c2def4ef5682986e7c646309df2b25a0d
ms.sourcegitcommit: 5969c693475e22a3f5a4fdde3473ecc33013b76f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/09/2022
ms.locfileid: "62460949"
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
  
> [in] Handle vers la fenêtre parent de l’indicateur de progression qui s’affiche pendant le téléchargement du formulaire. Le  _paramètre ulUIParam_ est ignoré, sauf si l’MAPI_DIALOG est définie dans _le paramètre ulFlags_ . 
    
 _ulFlags_
  
> [in] Masque de bits d’indicateurs qui contrôle le mode de téléchargement du formulaire. L’indicateur suivant peut être définie :
    
MAPI_DIALOG 
  
> Affiche une interface utilisateur pour fournir un état ou invite l’utilisateur à fournir plus d’informations. Si cet indicateur n’est pas définie, aucune interface utilisateur n’est affichée.
    
 _pfinfo_
  
> [in] Pointeur vers un objet d’informations de formulaire pour le formulaire à télécharger.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.
    
## <a name="remarks"></a>Remarques

Les visionneuses de formulaire appellent **la méthode IMAPIFormMgr::P repareForm** pour télécharger un formulaire à partir d’un conteneur de formulaire à ouvrir. La plupart des visionneuses de formulaires n’ont pas besoin d’appeler **PrepareForm**, car les deux méthodes [IMAPIFormMgr::CreateForm](imapiformmgr-createform.md) [et IMAPIFormMgr::LoadForm](imapiformmgr-loadform.md) appellent **PrepareForm**, si nécessaire. 
  
Vous pouvez utiliser **PrepareForm** pour obtenir les bibliothèques de liens dynamiques (DLL) et d’autres fichiers associés à un formulaire pour les modifier. Si le formulaire modifié est chargé à nouveau dans son conteneur de formulaire, il doit être réinstallé. 
  
## <a name="see-also"></a>Voir aussi



[IMAPIFormMgr::CreateForm](imapiformmgr-createform.md)
  
[IMAPIFormMgr::LoadForm](imapiformmgr-loadform.md)
  
[IMAPIFormMgr : IUnknown](imapiformmgriunknown.md)

