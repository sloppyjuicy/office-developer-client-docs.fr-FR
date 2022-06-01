---
title: IMAPIFormMgrSelectFormContainer
description: IMAPIFormMgrSelectFormContainer présente une boîte de dialogue qui permet à l’utilisateur de sélectionner un conteneur de formulaires et retourne une interface pour l’objet conteneur.
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPIFolder.CopyMessages
api_type:
- COM
ms.assetid: c33daad6-52c4-4968-ac56-415178c9bf12
ms.openlocfilehash: 271e4de62cf84975c8307a6b6207ebb1c9e8c49d
ms.sourcegitcommit: f872848fbeb5b2353179ad4bf4eab23f61f87666
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/01/2022
ms.locfileid: "65816331"
---
# <a name="imapiformmgrselectformcontainer"></a>IMAPIFormMgr::SelectFormContainer

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Présente une boîte de dialogue qui permet à l’utilisateur de sélectionner un conteneur de formulaires et retourne une interface pour l’objet conteneur sélectionné par l’utilisateur.
  
```cpp
HRESULT SelectFormContainer(
  ULONG_PTR ulUIParam,
  ULONG ulFlags,
  LPMAPIFORMCONTAINER FAR * lppfcnt
);
```

## <a name="parameters"></a>Paramètres

 _ulUIParam_
  
> [in] Handle de la fenêtre parente de la boîte de dialogue affichée. 
    
 _ulFlags_
  
> [in] Masque de bits des indicateurs qui contrôle la façon dont la bibliothèque de formulaires est sélectionnée (autrement dit, la façon dont le conteneur de formulaires est sélectionné). Les indicateurs suivants peuvent être définis :
    
MAPIFORM_SELECT_ALL_REGISTRIES 
  
> La sélection peut être effectuée à partir de tous les conteneurs. Il s’agit du type de sélection par défaut. 
    
MAPIFORM_SELECT_FOLDER_REGISTRY_ONLY 
  
> La sélection ne peut être effectuée qu’à partir de conteneurs de dossiers.
    
MAPIFORM_SELECT_NON_FOLDER_REGISTRY_ONLY 
  
> La sélection ne peut être effectuée qu’à partir de conteneurs qui ne sont pas associés à des dossiers.
    
 _lppfcnt_
  
> [out] Pointeur vers un pointeur vers l’interface retournée. Cette interface est destinée à l’objet conteneur sélectionné par l’utilisateur.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.
    
## <a name="remarks"></a>Remarques

Les visionneuses de formulaires appellent généralement la méthode **IMAPIFormMgr::SelectFormContainer** pour sélectionner un conteneur de formulaires dans lequel un formulaire est installé. **SelectFormContainer** ne peut pas être utilisé pour sélectionner le conteneur de formulaires local, qui a la valeur HFRMREG_LOCAL. 
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|MainDlg.cpp  <br/> |CMainDlg::OnSelectFormContainer  <br/> |MFCMAPI utilise la méthode **IMAPIFormMgr::SelectFormContainer** pour sélectionner un conteneur de formulaires avant de restituer son contenu. |
   
## <a name="see-also"></a>Voir aussi



[IMAPIFormMgr : IUnknown](imapiformmgriunknown.md)


[MFCMAPI comme un exemple de Code](mfcmapi-as-a-code-sample.md)

